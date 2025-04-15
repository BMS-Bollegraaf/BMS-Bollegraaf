---
{"dg-publish":true,"permalink":"/city-html/"}
---



<!DOCTYPE html>
<html>
<head>
  <title>3D City Simulation</title>
  <style>
    body { 
      margin: 0;
      overflow: hidden;
      font-family: Arial, sans-serif;
    }
    canvas { 
      display: block;
    }
    #controls {
      position: absolute;
      top: 10px;
      left: 10px;
      background: rgba(0,0,0,0.7);
      color: white;
      padding: 10px;
      border-radius: 5px;
      width: 250px;
    }
    .slider-container {
      margin-bottom: 10px;
    }
    label {
      display: inline-block;
      width: 100px;
    }
    button {
      margin-top: 10px;
      padding: 5px 10px;
      background: #4CAF50;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    button:hover {
      background: #45a049;
    }
  </style>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
</head>
<body>
  <div id="controls">
    <h2>City Controls</h2>
    
    <div class="slider-container">
      <label for="buildingHeight">Building Height:</label>
      <input type="range" id="buildingHeight" min="1" max="20" value="10" step="1">
    </div>
    
    <div class="slider-container">
      <label for="buildingDensity">Building Density:</label>
      <input type="range" id="buildingDensity" min="5" max="30" value="15" step="1">
    </div>
    
    <div class="slider-container">
      <label for="timeOfDay">Time of Day:</label>
      <input type="range" id="timeOfDay" min="0" max="24" value="12" step="0.5">
      <span id="timeValue">12:00</span>
    </div>
    
    <div class="slider-container">
      <label for="trafficAmount">Traffic:</label>
      <input type="range" id="trafficAmount" min="0" max="100" value="50">
    </div>
    
    <div class="slider-container">
      <label for="parkSize">Parks Size:</label>
      <input type="range" id="parkSize" min="0" max="100" value="30">
    </div>
    
    <button id="regenerateCity">Regenerate City</button>
    
    <p>Controls: WASD to move, Space/Shift for up/down, Mouse to look</p>
  </div>

  <script>
    // Scene setup
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
    const renderer = new THREE.WebGLRenderer();
    renderer.setSize(window.innerWidth, window.innerHeight);
    document.body.appendChild(renderer.domElement);
    
    // Camera starting position
    camera.position.set(0, 30, 60);
    camera.lookAt(0, 0, 0);
    
    // Lighting
    const ambientLight = new THREE.AmbientLight(0xffffff, 0.4);
    scene.add(ambientLight);
    
    const directionalLight = new THREE.DirectionalLight(0xffffff, 0.8);
    directionalLight.position.set(50, 100, 50);
    directionalLight.castShadow = true;
    scene.add(directionalLight);
    
    // Create ground
    const groundGeometry = new THREE.PlaneGeometry(500, 500);
    const groundMaterial = new THREE.MeshStandardMaterial({ 
      color: 0x333333,
      roughness: 0.8,
    });
    const ground = new THREE.Mesh(groundGeometry, groundMaterial);
    ground.rotation.x = -Math.PI / 2;
    scene.add(ground);
    
    // City elements
    const cityGroup = new THREE.Group();
    scene.add(cityGroup);
    
    // Traffic elements
    const trafficGroup = new THREE.Group();
    scene.add(trafficGroup);
    
    // Parks elements
    const parksGroup = new THREE.Group();
    scene.add(parksGroup);
    
    // Building materials
    const buildingMaterials = [
      new THREE.MeshStandardMaterial({ color: 0x888888 }),
      new THREE.MeshStandardMaterial({ color: 0x8899AA }),
      new THREE.MeshStandardMaterial({ color: 0xAA8866 }),
      new THREE.MeshStandardMaterial({ color: 0x334455 })
    ];
    
    // Build the city
    function generateCity() {
      // Clear existing city
      while(cityGroup.children.length > 0) {
        cityGroup.remove(cityGroup.children[0]);
      }
      
      while(trafficGroup.children.length > 0) {
        trafficGroup.remove(trafficGroup.children[0]);
      }
      
      while(parksGroup.children.length > 0) {
        parksGroup.remove(parksGroup.children[0]);
      }
      
      const buildingDensity = parseInt(document.getElementById('buildingDensity').value);
      const maxHeight = parseInt(document.getElementById('buildingHeight').value);
      const parkSize = parseInt(document.getElementById('parkSize').value) / 100;
      
      // Create a grid of buildings
      const gridSize = buildingDensity;
      const spacing = 200 / gridSize;
      
      // Generate road grid
      const roadWidth = spacing * 0.3;
      const blockSize = spacing - roadWidth;
      
      // Create roads
      for (let x = -100; x <= 100; x += spacing) {
        // Horizontal roads
        const roadH = new THREE.Mesh(
          new THREE.PlaneGeometry(200, roadWidth),
          new THREE.MeshStandardMaterial({ color: 0x222222 })
        );
        roadH.rotation.x = -Math.PI / 2;
        roadH.position.set(0, 0.1, x);
        cityGroup.add(roadH);
        
        // Vertical roads
        const roadV = new THREE.Mesh(
          new THREE.PlaneGeometry(roadWidth, 200),
          new THREE.MeshStandardMaterial({ color: 0x222222 })
        );
        roadV.rotation.x = -Math.PI / 2;
        roadV.position.set(x, 0.1, 0);
        cityGroup.add(roadV);
      }
      
      // Generate traffic
      const trafficAmount = parseInt(document.getElementById('trafficAmount').value);
      const trafficCount = Math.floor(trafficAmount / 10) * gridSize;
      
      for (let i = 0; i < trafficCount; i++) {
        const isHorizontal = Math.random() > 0.5;
        const carSize = 1.5;
        
        const car = new THREE.Mesh(
          new THREE.BoxGeometry(isHorizontal ? carSize * 2 : carSize, carSize, isHorizontal ? carSize : carSize * 2),
          new THREE.MeshStandardMaterial({ 
            color: new THREE.Color().setHSL(Math.random(), 0.8, 0.5) 
          })
        );
        
        if (isHorizontal) {
          // Horizontal road
          const roadIndex = Math.floor(Math.random() * gridSize) - gridSize/2;
          const roadZ = roadIndex * spacing;
          const laneOffset = (Math.random() > 0.5 ? 1 : -1) * (roadWidth / 4);
          car.position.set(
            (Math.random() * 180) - 90,
            carSize / 2 + 0.2,
            roadZ + laneOffset
          );
          car.userData = { 
            direction: Math.random() > 0.5 ? 1 : -1,
            speed: 0.1 + Math.random() * 0.2,
            horizontal: true
          };
        } else {
          // Vertical road
          const roadIndex = Math.floor(Math.random() * gridSize) - gridSize/2;
          const roadX = roadIndex * spacing;
          const laneOffset = (Math.random() > 0.5 ? 1 : -1) * (roadWidth / 4);
          car.position.set(
            roadX + laneOffset,
            carSize / 2 + 0.2,
            (Math.random() * 180) - 90
          );
          car.userData = { 
            direction: Math.random() > 0.5 ? 1 : -1,
            speed: 0.1 + Math.random() * 0.2,
            horizontal: false
          };
        }
        
        trafficGroup.add(car);
      }
      
      // Create buildings and parks
      for (let x = -gridSize/2; x < gridSize/2; x++) {
        for (let z = -gridSize/2; z < gridSize/2; z++) {
          // Determine block usage (building or park)
          const isPark = Math.random() < parkSize;
          
          if (isPark) {
            createPark(x * spacing, z * spacing, blockSize);
          } else {
            // Create 1-4 buildings per block
            const buildingsPerBlock = Math.floor(Math.random() * 3) + 1;
            
            for (let b = 0; b < buildingsPerBlock; b++) {
              // Building dimensions
              const width = blockSize * (0.3 + Math.random() * 0.4);
              const depth = blockSize * (0.3 + Math.random() * 0.4);
              const height = (2 + Math.random() * maxHeight) * 2;
              
              // Building position within block
              const offsetX = (Math.random() - 0.5) * (blockSize - width) * 0.8;
              const offsetZ = (Math.random() - 0.5) * (blockSize - depth) * 0.8;
              
              const building = new THREE.Mesh(
                new THREE.BoxGeometry(width, height, depth),
                buildingMaterials[Math.floor(Math.random() * buildingMaterials.length)]
              );
              
              building.position.set(
                x * spacing + offsetX,
                height / 2,
                z * spacing + offsetZ
              );
              
              // Add windows
              addWindowsToBuilding(building);
              
              cityGroup.add(building);
            }
          }
        }
      }
    }
    
    function createPark(x, z, size) {
      // Park ground
      const parkGround = new THREE.Mesh(
        new THREE.PlaneGeometry(size * 0.8, size * 0.8),
        new THREE.MeshStandardMaterial({ color: 0x228833 })
      );
      parkGround.rotation.x = -Math.PI / 2;
      parkGround.position.set(x, 0.2, z);
      parksGroup.add(parkGround);
      
      // Add trees
      const treeCount = Math.floor(Math.random() * 8) + 3;
      for (let i = 0; i < treeCount; i++) {
        const tree = createTree();
        const treeX = x + (Math.random() - 0.5) * size * 0.7;
        const treeZ = z + (Math.random() - 0.5) * size * 0.7;
        tree.position.set(treeX, 0, treeZ);
        parksGroup.add(tree);
      }
      
      // Add a pond sometimes
      if (Math.random() < 0.3) {
        const pond = new THREE.Mesh(
          new THREE.CircleGeometry(size * 0.15, 16),
          new THREE.MeshStandardMaterial({ color: 0x3388cc })
        );
        pond.rotation.x = -Math.PI / 2;
        pond.position.set(x, 0.3, z);
        parksGroup.add(pond);
      }
    }
    
    function createTree() {
      const treeGroup = new THREE.Group();
      
      // Trunk
      const trunk = new THREE.Mesh(
        new THREE.CylinderGeometry(0.2, 0.4, 2, 6),
        new THREE.MeshStandardMaterial({ color: 0x8B4513 })
      );
      trunk.position.y = 1;
      treeGroup.add(trunk);
      
      // Leaves
      const leaves = new THREE.Mesh(
        new THREE.ConeGeometry(2, 4, 6),
        new THREE.MeshStandardMaterial({ color: 0x00AA22 })
      );
      leaves.position.y = 4;
      treeGroup.add(leaves);
      
      return treeGroup;
    }
    
    function addWindowsToBuilding(building) {
      const width = building.geometry.parameters.width;
      const height = building.geometry.parameters.height;
      const depth = building.geometry.parameters.depth;
      
      // Number of window rows and columns
      const rows = Math.floor(height / 3);
      const colsX = Math.floor(width / 2);
      const colsZ = Math.floor(depth / 2);
      
      for (let row = 0; row < rows; row++) {
        const y = -height/2 + 1.5 + row * 3;
        
        // Windows on X sides
        for (let i = 0; i < colsX; i++) {
          const windowGeom = new THREE.PlaneGeometry(0.8, 1.2);
          
          // Random window state (lit or dark)
          const isLit = Math.random() < 0.6;
          const windowMat = new THREE.MeshStandardMaterial({ 
            color: isLit ? 0xFFFF88 : 0x444444,
            emissive: isLit ? 0xFFFF88 : 0x000000,
            emissiveIntensity: isLit ? 0.5 : 0
          });
          
          const windowMesh1 = new THREE.Mesh(windowGeom, windowMat);
          const windowMesh2 = new THREE.Mesh(windowGeom, windowMat.clone());
          
          const x = -width/2 + 1 + i * (width / colsX);
          
          windowMesh1.position.set(x, y, depth/2 + 0.01);
          windowMesh2.position.set(x, y, -depth/2 - 0.01);
          windowMesh2.rotation.y = Math.PI;
          
          building.add(windowMesh1);
          building.add(windowMesh2);
        }
        
        // Windows on Z sides
        for (let i = 0; i < colsZ; i++) {
          const windowGeom = new THREE.PlaneGeometry(0.8, 1.2);
          
          // Random window state (lit or dark)
          const isLit = Math.random() < 0.6;
          const windowMat = new THREE.MeshStandardMaterial({ 
            color: isLit ? 0xFFFF88 : 0x444444,
            emissive: isLit ? 0xFFFF88 : 0x000000,
            emissiveIntensity: isLit ? 0.5 : 0
          });
          
          const windowMesh1 = new THREE.Mesh(windowGeom, windowMat);
          const windowMesh2 = new THREE.Mesh(windowGeom, windowMat.clone());
          
          const z = -depth/2 + 1 + i * (depth / colsZ);
          
          windowMesh1.position.set(width/2 + 0.01, y, z);
          windowMesh1.rotation.y = Math.PI / 2;
          
          windowMesh2.position.set(-width/2 - 0.01, y, z);
          windowMesh2.rotation.y = -Math.PI / 2;
          
          building.add(windowMesh1);
          building.add(windowMesh2);
        }
      }
    }
    
    // Movement controls
    const keys = {};
    const moveSpeed = 0.5;
    const flySpeed = 0.3;
    
    let moveForward = false;
    let moveBackward = false;
    let moveLeft = false;
    let moveRight = false;
    let moveUp = false;
    let moveDown = false;
    
    document.addEventListener('keydown', (event) => {
      keys[event.key.toLowerCase()] = true;
      
      moveForward = keys['w'] || false;
      moveBackward = keys['s'] || false;
      moveLeft = keys['a'] || false;
      moveRight = keys['d'] || false;
      moveUp = keys[' '] || false;
      moveDown = keys['shift'] || false;
    });
    
    document.addEventListener('keyup', (event) => {
      keys[event.key.toLowerCase()] = false;
      
      moveForward = keys['w'] || false;
      moveBackward = keys['s'] || false;
      moveLeft = keys['a'] || false;
      moveRight = keys['d'] || false;
      moveUp = keys[' '] || false;
      moveDown = keys['shift'] || false;
    });
    
    // Mouse look controls
    let mouseX = 0;
    let mouseY = 0;
    let mouseDragging = false;
    
    document.addEventListener('mousedown', () => {
      mouseDragging = true;
    });
    
    document.addEventListener('mouseup', () => {
      mouseDragging = false;
    });
    
    document.addEventListener('mousemove', (event) => {
      if (mouseDragging) {
        mouseX = (event.clientX / window.innerWidth) * 2 - 1;
        mouseY = -(event.clientY / window.innerHeight) * 2 + 1;
        
        camera.rotation.y -= event.movementX * 0.01;
        camera.rotation.x -= event.movementY * 0.01;
        
        // Limit vertical rotation
        camera.rotation.x = Math.max(-Math.PI / 2, Math.min(Math.PI / 2, camera.rotation.x));
      }
    });
    
    // Update time of day
    function updateTimeOfDay() {
      const timeOfDay = parseFloat(document.getElementById('timeOfDay').value);
      document.getElementById('timeValue').textContent = formatTime(timeOfDay);
      
      // Calculate sun position
      const sunAngle = (timeOfDay - 6) / 12 * Math.PI; // 6am to 6pm
      
      if (timeOfDay >= 6 && timeOfDay <= 18) {
        // Day time
        const intensity = Math.sin(sunAngle);
        const sunX = 50 * Math.cos(sunAngle);
        const sunY = 100 * Math.sin(sunAngle);
        const sunZ = 50;
        
        directionalLight.position.set(sunX, sunY, sunZ);
        directionalLight.intensity = Math.max(0.1, intensity);
        
        // Sky color
        const skyHue = 0.6; // Blue
        const skySat = 0.7;
        const skyLightness = 0.4 + 0.4 * intensity;
        
        const skyColor = new THREE.Color().setHSL(skyHue, skySat, skyLightness);
        scene.background = skyColor;
        
        // Ambient light
        ambientLight.intensity = 0.2 + 0.2 * intensity;
      } else {
        // Night time
        directionalLight.intensity = 0.1;
        
        // Night sky
        const nightSkyColor = new THREE.Color().setHSL(0.7, 0.8, 0.05);
        scene.background = nightSkyColor;
        
        // Ambient light at night
        ambientLight.intensity = 0.15;
      }
    }
    
    function formatTime(timeValue) {
      const hours = Math.floor(timeValue);
      const minutes = Math.floor((timeValue - hours) * 60);
      return `${hours}:${minutes < 10 ? '0' + minutes : minutes}`;
    }
    
    // Update traffic
    function updateTraffic() {
      trafficGroup.children.forEach(car => {
        if (car.userData.horizontal) {
          car.position.x += car.userData.direction * car.userData.speed;
          
          // Loop around when reaching the edge
          if (car.position.x > 100) {
            car.position.x = -100;
          } else if (car.position.x < -100) {
            car.position.x = 100;
          }
        } else {
          car.position.z += car.userData.direction * car.userData.speed;
          
          // Loop around when reaching the edge
          if (car.position.z > 100) {
            car.position.z = -100;
          } else if (car.position.z < -100) {
            car.position.z = 100;
          }
        }
      });
    }
    
    // Handle window resize
    window.addEventListener('resize', () => {
      camera.aspect = window.innerWidth / window.innerHeight;
      camera.updateProjectionMatrix();
      renderer.setSize(window.innerWidth, window.innerHeight);
    });
    
    // Add event listeners for controls
    document.getElementById('timeOfDay').addEventListener('input', updateTimeOfDay);
    document.getElementById('regenerateCity').addEventListener('click', generateCity);
    
    // Initial city generation
    generateCity();
    updateTimeOfDay();
    
    // Animation loop
    function animate() {
      requestAnimationFrame(animate);
      
      // Movement
      const moveVector = new THREE.Vector3(0, 0, 0);
      
      // Forward/backward movement
      if (moveForward) {
        moveVector.z -= moveSpeed;
      }
      if (moveBackward) {
        moveVector.z += moveSpeed;
      }
      
      // Left/right movement
      if (moveLeft) {
        moveVector.x -= moveSpeed;
      }
      if (moveRight) {
        moveVector.x += moveSpeed;
      }
      
      // Up/down movement
      if (moveUp) {
        moveVector.y += flySpeed;
      }
      if (moveDown) {
        moveVector.y -= flySpeed;
      }
      
      // Apply movement in camera's local space
      moveVector.applyQuaternion(camera.quaternion);
      camera.position.add(moveVector);
      
      // Keep camera above ground
      if (camera.position.y < 1) {
        camera.position.y = 1;
      }
      
      // Update traffic
      updateTraffic();
      
      renderer.render(scene, camera);
    }
    
    animate();
  </script>
</body>
</html>
