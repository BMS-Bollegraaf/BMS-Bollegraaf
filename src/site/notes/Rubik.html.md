---
{"dg-publish":true,"permalink":"/rubik-html/","noteIcon":"lightbulb"}
---



<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Rubik's Cube Simulator</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
      font-family: Arial, sans-serif;
    }
    #container {
      width: 100%;
      height: 100vh;
      display: flex;
      flex-direction: column;
    }
    #canvas {
      flex: 1;
    }
    #controls {
      background: #f0f0f0;
      padding: 10px;
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }
    button {
      padding: 8px 12px;
      background: #4CAF50;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-weight: bold;
    }
    button:hover {
      background: #45a049;
    }
    .move-btn {
      background: #2196F3;
    }
    .move-btn:hover {
      background: #0b7dda;
    }
    #scramble-btn {
      background: #ff9800;
    }
    #scramble-btn:hover {
      background: #e68a00;
    }
    #solve-btn {
      background: #f44336;
    }
    #solve-btn:hover {
      background: #da190b;
    }
  </style>
</head>
<body>
  <div id="container">
    <div id="canvas"></div>
    <div id="controls">
      <button class="move-btn" data-face="U">U</button>
      <button class="move-btn" data-face="D">D</button>
      <button class="move-btn" data-face="L">L</button>
      <button class="move-btn" data-face="R">R</button>
      <button class="move-btn" data-face="F">F</button>
      <button class="move-btn" data-face="B">B</button>
      <button class="move-btn" data-face="U'" data-prime="true">U'</button>
      <button class="move-btn" data-face="D'" data-prime="true">D'</button>
      <button class="move-btn" data-face="L'" data-prime="true">L'</button>
      <button class="move-btn" data-face="R'" data-prime="true">R'</button>
      <button class="move-btn" data-face="F'" data-prime="true">F'</button>
      <button class="move-btn" data-face="B'" data-prime="true">B'</button>
      <button id="scramble-btn">Scramble</button>
      <button id="solve-btn">Auto Solve</button>
      <button id="reset-btn">Reset</button>
    </div>
  </div>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
  <script>
    // Cube configuration
    const CUBE_SIZE = 3;
    const PIECE_SIZE = 1;
    const GAP = 0.05;
    const COLORS = {
      U: 0xffffff, // white (up)
      D: 0xffff00, // yellow (down)
      F: 0x00ff00, // green (front)
      B: 0x0000ff, // blue (back)
      R: 0xff0000, // red (right)
      L: 0xffa500  // orange (left)
    };

    // Three.js setup
    const scene = new THREE.Scene();
    scene.background = new THREE.Color(0x222222);
    const camera = new THREE.PerspectiveCamera(45, window.innerWidth / window.innerHeight, 0.1, 1000);
    camera.position.set(8, 8, 8);
    camera.lookAt(0, 0, 0);

    const renderer = new THREE.WebGLRenderer({ antialias: true });
    renderer.setSize(window.innerWidth, window.innerHeight);
    document.getElementById('canvas').appendChild(renderer.domElement);

    // Add lighting
    const ambientLight = new THREE.AmbientLight(0xffffff, 0.6);
    scene.add(ambientLight);

    const directionalLight = new THREE.DirectionalLight(0xffffff, 0.8);
    directionalLight.position.set(5, 10, 7);
    scene.add(directionalLight);

    // Controls
    let isDragging = false;
    let previousMousePosition = { x: 0, y: 0 };
    const cubePivot = new THREE.Group();
    scene.add(cubePivot);

    // Mouse controls
    renderer.domElement.addEventListener('mousedown', (e) => {
      isDragging = true;
      previousMousePosition = { x: e.clientX, y: e.clientY };
    });

    renderer.domElement.addEventListener('mouseup', () => {
      isDragging = false;
    });

    renderer.domElement.addEventListener('mousemove', (e) => {
      if (isDragging && !isAnimating) {
        const deltaMove = {
          x: e.clientX - previousMousePosition.x,
          y: e.clientY - previousMousePosition.y
        };

        cubePivot.rotation.y += deltaMove.x * 0.01;
        cubePivot.rotation.x += deltaMove.y * 0.01;

        previousMousePosition = { x: e.clientX, y: e.clientY };
      }
    });

    // Cube data structures
    let cubelets = [];
    let cubeState = {};
    let moveQueue = [];
    let isAnimating = false;
    let isSolving = false;

    // Cube initialization
    function initCube() {
      // Clear existing cubelets
      cubelets.forEach(cubelet => {
        cubePivot.remove(cubelet);
      });
      cubelets = [];
      
      const offset = ((CUBE_SIZE - 1) / 2) * (PIECE_SIZE + GAP);
      
      // Create 27 cubelets (3x3x3)
      for (let x = 0; x < CUBE_SIZE; x++) {
        for (let y = 0; y < CUBE_SIZE; y++) {
          for (let z = 0; z < CUBE_SIZE; z++) {
            // Skip center piece (internal)
            if (x === 1 && y === 1 && z === 1) continue;
            
            const geometry = new THREE.BoxGeometry(PIECE_SIZE, PIECE_SIZE, PIECE_SIZE);
            const materials = Array(6).fill().map(() => new THREE.MeshPhongMaterial({ color: 0x333333 }));
            
            // Set face colors
            if (z === 0) materials[5].color.setHex(COLORS.F); // Front face
            if (z === 2) materials[4].color.setHex(COLORS.B); // Back face
            if (x === 0) materials[0].color.setHex(COLORS.L); // Left face
            if (x === 2) materials[1].color.setHex(COLORS.R); // Right face
            if (y === 0) materials[3].color.setHex(COLORS.D); // Down face
            if (y === 2) materials[2].color.setHex(COLORS.U); // Up face
            
            const cubelet = new THREE.Mesh(geometry, materials);
            cubelet.position.set(
              (x - 1) * (PIECE_SIZE + GAP),
              (y - 1) * (PIECE_SIZE + GAP),
              (z - 1) * (PIECE_SIZE + GAP)
            );
            
            // Store position data for moves
            cubelet.userData = {
              originalX: x,
              originalY: y,
              originalZ: z,
              currentX: x,
              currentY: y,
              currentZ: z
            };
            
            cubelets.push(cubelet);
            cubePivot.add(cubelet);
          }
        }
      }
      
      updateCubeState();
    }

    // Function to update internal cube state representation
    function updateCubeState() {
      cubeState = {
        U: [], // Up face (y=2)
        D: [], // Down face (y=0)
        F: [], // Front face (z=0)
        B: [], // Back face (z=2)
        R: [], // Right face (x=2)
        L: []  // Left face (x=0)
      };
      
      cubelets.forEach(cubelet => {
        const { currentX, currentY, currentZ } = cubelet.userData;
        
        if (currentY === 2) cubeState.U.push(cubelet);
        if (currentY === 0) cubeState.D.push(cubelet);
        if (currentZ === 0) cubeState.F.push(cubelet);
        if (currentZ === 2) cubeState.B.push(cubelet);
        if (currentX === 2) cubeState.R.push(cubelet);
        if (currentX === 0) cubeState.L.push(cubelet);
      });
    }

    // Perform a single move
    function performMove(face, isPrime = false) {
      if (isAnimating) {
        moveQueue.push({ face, isPrime });
        return;
      }
      
      isAnimating = true;
      
      const facePieces = cubeState[face];
      const rotationAxis = new THREE.Vector3();
      const rotationAngle = isPrime ? -Math.PI/2 : Math.PI/2;
      
      // Set rotation axis based on face
      if (face === 'U' || face === 'D') {
        rotationAxis.set(0, 1, 0);
      } else if (face === 'L' || face === 'R') {
        rotationAxis.set(1, 0, 0);
      } else if (face === 'F' || face === 'B') {
        rotationAxis.set(0, 0, 1);
      }
      
      // Setup rotation pivot
      const pivot = new THREE.Object3D();
      scene.add(pivot);
      
      // Move pieces to pivot
      facePieces.forEach(piece => {
        // Back up original world position and rotation
        const worldPos = new THREE.Vector3();
        piece.getWorldPosition(worldPos);
        
        const worldQuat = new THREE.Quaternion();
        piece.getWorldQuaternion(worldQuat);
        
        // Reparent to pivot
        cubePivot.remove(piece);
        pivot.add(piece);
        
        // Restore world position and rotation
        piece.position.copy(worldPos);
        piece.quaternion.copy(worldQuat);
      });
      
      // Animate rotation
      let progress = 0;
      const animateRotation = () => {
        progress += 0.08;
        
        if (progress < 1) {
          pivot.rotation[face === 'U' || face === 'D' ? 'y' : face === 'L' || face === 'R' ? 'x' : 'z'] = 
            rotationAngle * progress;
          requestAnimationFrame(animateRotation);
        } else {
          // Finish rotation exactly at target angle
          pivot.rotation[face === 'U' || face === 'D' ? 'y' : face === 'L' || face === 'R' ? 'x' : 'z'] = 
            rotationAngle;
          
          // Move pieces back to cube
          facePieces.forEach(piece => {
            // Back up position and rotation
            const worldPos = new THREE.Vector3();
            piece.getWorldPosition(worldPos);
            
            const worldQuat = new THREE.Quaternion();
            piece.getWorldQuaternion(worldQuat);
            
            // Reparent back to cube
            pivot.remove(piece);
            cubePivot.add(piece);
            
            // Restore world position
            piece.position.copy(worldPos);
            piece.quaternion.copy(worldQuat);
            
            // Update cubelet position data
            updateCubeletPosition(piece, face, isPrime);
          });
          
          // Clean up
          scene.remove(pivot);
          
          // Update internal state
          updateCubeState();
          
          isAnimating = false;
          
          // Process next move in queue if any
          if (moveQueue.length > 0) {
            const nextMove = moveQueue.shift();
            performMove(nextMove.face, nextMove.isPrime);
          } else if (isSolving) {
            checkAndContinueSolving();
          }
        }
      };
      
      animateRotation();
    }

    // Update position data after a move
    function updateCubeletPosition(cubelet, face, isPrime) {
      const { currentX, currentY, currentZ } = cubelet.userData;
      let newX = currentX, newY = currentY, newZ = currentZ;
      
      // Update position based on face
      if (face === 'U' && currentY === 2) {
        if (isPrime) {
          // U' move: (x,y,z) -> (z,y,3-x-1)
          [newX, newZ] = [currentZ, CUBE_SIZE - currentX - 1];
        } else {
          // U move: (x,y,z) -> (3-z-1,y,x)
          [newX, newZ] = [CUBE_SIZE - currentZ - 1, currentX];
        }
      } else if (face === 'D' && currentY === 0) {
        if (isPrime) {
          // D' move: (x,y,z) -> (3-z-1,y,x)
          [newX, newZ] = [CUBE_SIZE - currentZ - 1, currentX];
        } else {
          // D move: (x,y,z) -> (z,y,3-x-1)
          [newX, newZ] = [currentZ, CUBE_SIZE - currentX - 1];
        }
      } else if (face === 'F' && currentZ === 0) {
        if (isPrime) {
          // F' move: (x,y,z) -> (y,3-x-1,z)
          [newX, newY] = [currentY, CUBE_SIZE - currentX - 1];
        } else {
          // F move: (x,y,z) -> (3-y-1,x,z)
          [newX, newY] = [CUBE_SIZE - currentY - 1, currentX];
        }
      } else if (face === 'B' && currentZ === 2) {
        if (isPrime) {
          // B' move: (x,y,z) -> (3-y-1,x,z)
          [newX, newY] = [CUBE_SIZE - currentY - 1, currentX];
        } else {
          // B move: (x,y,z) -> (y,3-x-1,z)
          [newX, newY] = [currentY, CUBE_SIZE - currentX - 1];
        }
      } else if (face === 'R' && currentX === 2) {
        if (isPrime) {
          // R' move: (x,y,z) -> (x,z,3-y-1)
          [newY, newZ] = [currentZ, CUBE_SIZE - currentY - 1];
        } else {
          // R move: (x,y,z) -> (x,3-z-1,y)
          [newY, newZ] = [CUBE_SIZE - currentZ - 1, currentY];
        }
      } else if (face === 'L' && currentX === 0) {
        if (isPrime) {
          // L' move: (x,y,z) -> (x,3-z-1,y)
          [newY, newZ] = [CUBE_SIZE - currentZ - 1, currentY];
        } else {
          // L move: (x,y,z) -> (x,z,3-y-1)
          [newY, newZ] = [currentZ, CUBE_SIZE - currentY - 1];
        }
      }
      
      cubelet.userData.currentX = newX;
      cubelet.userData.currentY = newY;
      cubelet.userData.currentZ = newZ;
    }

    // Scramble the cube
    function scrambleCube() {
      if (isAnimating || isSolving) return;
      
      const moves = [];
      const faces = ['U', 'D', 'L', 'R', 'F', 'B'];
      
      // Generate 20 random moves
      for (let i = 0; i < 20; i++) {
        const face = faces[Math.floor(Math.random() * faces.length)];
        const isPrime = Math.random() > 0.5;
        moves.push({ face, isPrime });
      }
      
      // Execute moves one by one
      let moveIndex = 0;
      const executeNextMove = () => {
        if (moveIndex < moves.length) {
          const move = moves[moveIndex++];
          performMove(move.face, move.isPrime);
          
          // Set up callback for when this move is done
          const checkMoveComplete = () => {
            if (!isAnimating) {
              executeNextMove();
            } else {
              requestAnimationFrame(checkMoveComplete);
            }
          };
          
          requestAnimationFrame(checkMoveComplete);
        }
      };
      
      executeNextMove();
    }

    // Check if cube is solved
    function isCubeSolved() {
      // For each face, all stickers should be the same color
      const faces = ['U', 'D', 'L', 'R', 'F', 'B'];
      
      for (const face of faces) {
        // Check if face is solved by checking original coordinates
        for (let i = 1; i < cubeState[face].length; i++) {
          const firstPiece = cubeState[face][0];
          const currentPiece = cubeState[face][i];
          
          // Compare X coordinates for U/D faces
          if (face === 'U' || face === 'D') {
            if (firstPiece.userData.originalY !== currentPiece.userData.originalY) {
              return false;
            }
          }
          // Compare Y coordinates for F/B faces
          else if (face === 'F' || face === 'B') {
            if (firstPiece.userData.originalZ !== currentPiece.userData.originalZ) {
              return false;
            }
          }
          // Compare Z coordinates for L/R faces
          else if (face === 'L' || face === 'R') {
            if (firstPiece.userData.originalX !== currentPiece.userData.originalX) {
              return false;
            }
          }
        }
      }
      
      return true;
    }

    // Solve the cube using a beginner's method (simplified for demo)
    function solveCube() {
      if (isAnimating || isSolving) return;
      
      // Create solution steps (this is a highly simplified solver)
      // For a real solver, we would implement a more sophisticated algorithm
      
      // Just for demo - let's reverse scramble by trying random moves
      // This is NOT a real solver, it's just to demonstrate the concept
      isSolving = true;
      
      checkAndContinueSolving();
    }

    function checkAndContinueSolving() {
      if (isCubeSolved()) {
        isSolving = false;
        return;
      }
      
      // Try a random move
      const faces = ['U', 'D', 'L', 'R', 'F', 'B'];
      const face = faces[Math.floor(Math.random() * faces.length)];
      const isPrime = Math.random() > 0.5;
      
      // Make the move
      performMove(face, isPrime);
    }

    // Reset cube to solved state
    function resetCube() {
      if (isAnimating) return;
      
      // Cancel any solving in progress
      isSolving = false;
      moveQueue = [];
      
      // Clear and reinitialize
      initCube();
    }

    // Set up event listeners
    document.querySelectorAll('.move-btn').forEach(button => {
      button.addEventListener('click', () => {
        const face = button.dataset.face.charAt(0);
        const isPrime = button.dataset.prime === 'true';
        performMove(face, isPrime);
      });
    });

    document.getElementById('scramble-btn').addEventListener('click', scrambleCube);
    document.getElementById('solve-btn').addEventListener('click', solveCube);
    document.getElementById('reset-btn').addEventListener('click', resetCube);

    // Handle window resize
    window.addEventListener('resize', () => {
      camera.aspect = window.innerWidth / window.innerHeight;
      camera.updateProjectionMatrix();
      renderer.setSize(window.innerWidth, window.innerHeight);
    });

    // Animation loop
    function animate() {
      requestAnimationFrame(animate);
      renderer.render(scene, camera);
    }

    // Initialize and start
    initCube();
    animate();
  </script>
</body>
</html>
