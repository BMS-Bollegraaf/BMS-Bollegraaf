---
{"dg-publish":true,"permalink":"/test-main/","tags":["gardenEntry"],"noteIcon":"default"}
---

<!DOCTYPE html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Digital Garden</title>
    <style>
        :root {
            /* Modern, vibrant color scheme */
            --primary-color: #6366f1;
            --primary-light: #818cf8;
            --primary-dark: #4f46e5;
            --secondary-color: #10b981;
            --accent-color: #f59e0b;
            --dark-color: #1f2937;
            --light-color: #f3f4f6;
            --card-bg: #ffffff;
            --card-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            --border-radius: 12px;
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        body {
            font-family: 'Inter', system-ui, -apple-system, sans-serif;
            line-height: 1.7;
            color: var(--dark-color);
            background-color: var(--light-color);
            margin: 0;
            padding: 0;
            background-image: 
                radial-gradient(circle at 85% 15%, rgba(99, 102, 241, 0.1) 0%, transparent 40%),
                radial-gradient(circle at 15% 85%, rgba(16, 185, 129, 0.1) 0%, transparent 40%);
            background-attachment: fixed;
            overflow-x: hidden;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 2rem;
        }

        /* Header Section with parallax effect */
        .header {
            position: relative;
            min-height: 250px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 3rem 2rem;
            margin-bottom: 3rem;
            overflow: hidden;
            border-radius: var(--border-radius);
            background: linear-gradient(135deg, var(--primary-light) 0%, var(--primary-dark) 100%);
            color: white;
            box-shadow: var(--card-shadow);
        }

        .header-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
        }

        .header h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            font-weight: 800;
            background: linear-gradient(to right, #ffffff, #e0e7ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: -0.025em;
        }

        .header p {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto;
            opacity: 0.9;
        }

        .header-shapes {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
            overflow: hidden;
        }

        .shape {
            position: absolute;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
        }

        .shape-1 {
            width: 150px;
            height: 150px;
            top: -20px;
            left: 10%;
        }

        .shape-2 {
            width: 100px;
            height: 100px;
            bottom: 20px;
            right: 15%;
        }

        .shape-3 {
            width: 120px;
            height: 120px;
            top: 30%;
            right: 5%;
        }

        /* Modern Search Box */
        .search-container {
            position: relative;
            margin: 0 auto 3rem;
            max-width: 700px;
        }

        .search-box {
            width: 100%;
            padding: 1.2rem 1.5rem 1.2rem 3.5rem;
            font-size: 1.1rem;
            border: none;
            border-radius: 50px;
            background-color: white;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            outline: none;
            transition: var(--transition);
        }

        .search-box:focus {
            box-shadow: 0 0 0 3px rgba(99, 102, 241, 0.3), 0 4px 12px rgba(0, 0, 0, 0.08);
        }

        .search-icon {
            position: absolute;
            left: 1.5rem;
            top: 50%;
            transform: translateY(-50%);
            color: #6b7280;
            pointer-events: none;
        }

        /* Dashboard Layout */
        .dashboard {
            display: grid;
            grid-template-columns: 1fr 350px;
            gap: 2rem;
        }

        .main-content {
            display: grid;
            gap: 2rem;
        }

        .sidebar {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        /* Hub Section Styling */
        .hub-section {
            position: relative;
            background-color: white;
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            padding: 1.5rem;
            transition: var(--transition);
            overflow: hidden;
        }

        .hub-section:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }

        .hub-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .hub-header h2 {
            margin: 0;
            font-size: 1.5rem;
            color: var(--dark-color);
            font-weight: 700;
        }

        .hub-content {
            position: relative;
            z-index: 2;
        }

        /* Project Hub Styling */
        .project-hub {
            border-top: 4px solid var(--primary-color);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 1rem;
        }

        .project-card {
            background-color: #f9fafb;
            border-radius: 8px;
            padding: 1.2rem;
            transition: var(--transition);
            cursor: pointer;
            position: relative;
            overflow: hidden;
            border: 1px solid #e5e7eb;
        }

        .project-card:hover {
            background-color: #f3f4f6;
            border-color: #d1d5db;
        }

        .project-card h4 {
            margin-top: 0;
            margin-bottom: 0.5rem;
            font-size: 1rem;
            color: var(--dark-color);
        }

        .project-card p {
            margin: 0;
            font-size: 0.85rem;
            color: #6b7280;
        }

        .project-status {
            position: absolute;
            top: 0.5rem;
            right: 0.5rem;
            width: 10px;
            height: 10px;
            border-radius: 50%;
        }

        .status-active {
            background-color: #10b981;
        }

        .status-paused {
            background-color: #f59e0b;
        }

        .status-completed {
            background-color: #6366f1;
        }

        /* Knowledge Hub Styling */
        .knowledge-hub {
            border-top: 4px solid var(--secondary-color);
        }

        .knowledge-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1rem;
        }

        .knowledge-card {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: #f9fafb;
            border-radius: 8px;
            padding: 2rem 1rem;
            text-align: center;
            transition: var(--transition);
            cursor: pointer;
            border: 1px solid #e5e7eb;
        }

        .knowledge-card:hover {
            background-color: #f3f4f6;
            border-color: #d1d5db;
        }

        .knowledge-icon {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: var(--secondary-color);
        }

        .knowledge-card h4 {
            margin: 0;
            font-size: 1rem;
            color: var(--dark-color);
        }

        /* Music Hub Styling */
        .music-hub {
            border-top: 4px solid var(--accent-color);
        }

        .music-scroll {
            position: relative;
            display: flex;
            overflow-x: auto;
            gap: 1rem;
            padding: 0.5rem 0;
            scrollbar-width: thin;
            scrollbar-color: var(--accent-color) #f1f1f1;
        }

        .music-scroll::-webkit-scrollbar {
            height: 5px;
        }

        .music-scroll::-webkit-scrollbar-track {
            background: #f1f1f1;
            border-radius: 10px;
        }

        .music-scroll::-webkit-scrollbar-thumb {
            background: var(--accent-color);
            border-radius: 10px;
        }

        .album-card {
            flex: 0 0 auto;
            width: 120px;
            text-align: center;
            transition: var(--transition);
            cursor: pointer;
        }

        .album-card:hover {
            transform: translateY(-5px);
        }

        .album-art {
            width: 120px;
            height: 120px;
            object-fit: cover;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            margin-bottom: 0.5rem;
        }

        .album-name {
            font-size: 0.85rem;
            color: var(--dark-color);
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin: 0.5rem 0 0.25rem;
        }

        .artist-name {
            font-size: 0.75rem;
            color: #6b7280;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin: 0;
        }

        /* Thought Map Styling */
        .thought-map {
            position: relative;
            min-height: 300px;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: white;
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            padding: 1.5rem;
            transition: var(--transition);
            overflow: hidden;
            border-top: 4px solid #8b5cf6;
        }

        .thought-map:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }

        .map-container {
            width: 100%;
            height: 300px;
            position: relative;
        }

        .node {
            position: absolute;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background-color: #8b5cf6;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.5rem;
            cursor: pointer;
            z-index: 2;
            transition: var(--transition);
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .node:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 8px rgba(0, 0, 0, 0.15);
        }

        .node-1 {
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #8b5cf6;
            width: 80px;
            height: 80px;
        }

        .node-2 {
            top: 20%;
            left: 30%;
            background-color: #ec4899;
        }

        .node-3 {
            top: 70%;
            left: 25%;
            background-color: #10b981;
        }

        .node-4 {
            top: 30%;
            left: 70%;
            background-color: #f59e0b;
        }

        .node-5 {
            top: 65%;
            left: 75%;
            background-color: #3b82f6;
        }

        .connector {
            position: absolute;
            background-color: #e5e7eb;
            height: 2px;
            transform-origin: left center;
            z-index: 1;
        }

        /* Sidebar Widgets */
        .widget {
            background-color: white;
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            padding: 1.5rem;
            transition: var(--transition);
        }

        .widget:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }

        .widget-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
        }

        .widget-header h3 {
            margin: 0;
            font-size: 1.2rem;
            color: var(--dark-color);
            font-weight: 600;
        }

        /* Random Note Widget */
        .random-note-widget {
            border-left: 4px solid #8b5cf6;
        }

        .random-note-content {
            font-size: 0.95rem;
            line-height: 1.6;
            color: #4b5563;
            margin-bottom: 1rem;
            font-style: italic;
        }

        .random-note-btn {
            background-color: #8b5cf6;
            color: white;
            border: none;
            padding: 0.6rem 1.2rem;
            border-radius: 6px;
            cursor: pointer;
            font-size: 0.9rem;
            transition: var(--transition);
            display: block;
            width: 100%;
        }

        .random-note-btn:hover {
            background-color: #7c3aed;
        }

        /* Recent Activity Widget */
        .recent-activity-widget {
            border-left: 4px solid #3b82f6;
        }

        .activity-list {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .activity-item {
            padding: 0.8rem 0;
            border-bottom: 1px solid #e5e7eb;
            font-size: 0.9rem;
        }

        .activity-item:last-child {
            border-bottom: none;
            padding-bottom: 0;
        }

        .activity-title {
            color: var(--dark-color);
            font-weight: 500;
            margin: 0 0 0.3rem;
            display: block;
        }

        .activity-meta {
            color: #6b7280;
            font-size: 0.8rem;
        }

        /* Quick Actions Widget */
        .quick-actions-widget {
            border-left: 4px solid #ef4444;
        }

        .actions-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 0.8rem;
        }

        .action-btn {
            background-color: #f3f4f6;
            border: 1px solid #e5e7eb;
            border-radius: 6px;
            padding: 0.8rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            cursor: pointer;
            transition: var(--transition);
        }

        .action-btn:hover {
            background-color: #e5e7eb;
            border-color: #d1d5db;
        }

        .action-icon {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: #ef4444;
        }

        .action-label {
            font-size: 0.8rem;
            color: var(--dark-color);
            margin: 0;
        }

        /* Footer */
        .footer {
            text-align: center;
            margin-top: 3rem;
            padding-top: 1.5rem;
            border-top: 1px solid #e5e7eb;
            color: #6b7280;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .dashboard {
                grid-template-columns: 1fr;
            }
            
            .sidebar {
                display: grid;
                grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            }
            
            .knowledge-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }
            
            .header h1 {
                font-size: 2.5rem;
            }
            
            .projects-grid {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
            
            .knowledge-grid {
                grid-template-columns: 1fr;
            }
            
            .sidebar {
                grid-template-columns: 1fr;
            }
        }

        /* Keyframe Animations */
        @keyframes float {
            0% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-10px);
            }
            100% {
                transform: translateY(0px);
            }
        }

        .float-animation {
            animation: float 6s ease-in-out infinite;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Dynamic Header Section -->
        <div class="header">
            <div class="header-shapes">
                <div class="shape shape-1"></div>
                <div class="shape shape-2"></div>
                <div class="shape shape-3"></div>
            </div>
            <div class="header-content">
                <h1>My Digital Garden</h1>
                <p>A living collection of ideas, projects, and discoveries — my second brain in digital form.</p>
            </div>
        </div>

        <!-- Enhanced Search Box -->
        <div class="search-container">
            <input type="text" class="search-box" placeholder="Search across my digital garden...">
            <div class="search-icon">🔍</div>
        </div>

        <!-- Dashboard Layout -->
        <div class="dashboard">
            <div class="main-content">
                <!-- Projects Hub -->
                <div class="hub-section project-hub">
                    <div class="hub-header">
                        <h2>Projects</h2>
                        <a href="./projects" style="color: var(--primary-color); text-decoration: none; font-size: 0.9rem;">View All →</a>
                    </div>
                    <div class="hub-content">
                        <div class="projects-grid">
                            <div class="project-card" onclick="window.location.href='./projects/project1'">
                                <div class="project-status status-active"></div>
                                <h4>Personal Website</h4>
                                <p>Portfolio and blog redesign</p>
                            </div>
                            <div class="project-card" onclick="window.location.href='./projects/project2'">
                                <div class="project-status status-active"></div>
                                <h4>AI Research</h4>
                                <p>Exploring LLM capabilities</p>
                            </div>
                            <div class="project-card" onclick="window.location.href='./projects/project3'">
                                <div class="project-status status-paused"></div>
                                <h4>Smart Home</h4>
                                <p>Home automation setup</p>
                            </div>
                            <div class="project-card" onclick="window.location.href='./projects/project4'">
                                <div class="project-status status-completed"></div>
                                <h4>Reading List</h4>
                                <p>Book tracking system</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Knowledge Hub -->
                <div class="hub-section knowledge-hub">
                    <div class="hub-header">
                        <h2>Knowledge</h2>
                        <a href="./knowledge" style="color: var(--secondary-color); text-decoration: none; font-size: 0.9rem;">Explore More →</a>
                    </div>  
                    <div class="hub-content">
                        <div class="knowledge-grid">
                            <div class="knowledge-card" onclick="window.location.href='./ai-tools'">
                                <div class="knowledge-icon">🤖</div>
                                <h4>AI Tools</h4>
                            </div>
                            <div class="knowledge-card" onclick="window.location.href='./programming'">
                                <div class="knowledge-icon">💻</div>
                                <h4>Programming</h4>
                            </div>
                            <div class="knowledge-card" onclick="window.location.href='./resources'">
                                <div class="knowledge-icon">📚</div>
                                <h4>Resources</h4>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Music Hub -->
                <div class="hub-section music-hub">
                    <div class="hub-header">
                        <h2>Music</h2>
                        <a href="./music" style="color: var(--accent-color); text-decoration: none; font-size: 0.9rem;">Full Library →</a>
                    </div>
                    <div class="hub-content">
                        <div class="music-scroll">
                            <div class="album-card" onclick="window.location.href='./music/album1'">
                                <img src="/api/placeholder/120/120" alt="Album Art" class="album-art">
                                <p class="album-name">Album Name</p>
                                <p class="artist-name">Artist</p>
                            </div>
                            <div class="album-card" onclick="window.location.href='./music/album2'">
                                <img src="/api/placeholder/120/120" alt="Album Art" class="album-art">
                                <p class="album-name">Another Album</p>
                                <p class="artist-name">Another Artist</p>
                            </div>
                            <div class="album-card" onclick="window.location.href='./music/album3'">
                                <img src="/api/placeholder/120/120" alt="Album Art" class="album-art">
                                <p class="album-name">Third Album</p>
                                <p class="artist-name">Third Artist</p>
                            </div>
                            <div class="album-card" onclick="window.location.href='./music/album4'">
                                <img src="/api/placeholder/120/120" alt="Album Art" class="album-art">
                                <p class="album-name">Fourth Album</p>
                                <p class="artist-name">Fourth Artist</p>
                            </div>
                            <div class="album-card" onclick="window.location.href='./music/album5'">
                                <img src="/api/placeholder/120/120" alt="Album Art" class="album-art">
                                <p class="album-name">Fifth Album</p>
                                <p class="artist-name">Fifth Artist</p>
                            </div>
                            <div class="album-card" onclick="window.location.href='./music/album6'">
                                <img src="/api/placeholder/120/120" alt="Album Art" class="album-art">
                                <p class="album-name">Sixth Album</p>
                                <p class="artist-name">Sixth Artist</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Thought Map (Zettelkasten Visualization) -->
                <div class="thought-map">
                    <div class="hub-header">
                        <h2>Thought Map</h2>
                        <a href="./zettelkasten" style="color: #8b5cf6; text-decoration: none; font-size: 0.9rem;">Enter Zettelkasten →</a>
                    </div>
                    <div class="map-container">
                        <div class="node node-1 float-animation" onclick="window.location.href='./zettelkasten/main'">🧠</div>
                        <div class="node node-2" onclick="window.location.href='./zettelkasten/topic1'">📝</div>
                        <div class="node node-3" onclick="window.location.href='./zettelkasten/topic2'">💡</div>
                        <div class="node node-4" onclick="window.location.href='./zettelkasten/topic3'">🔍</div>
                        <div class="node node-5" onclick="window.location.href='./zettelkasten/topic4'">📊</div>
                        <!-- Connectors between nodes -->
                        <div id="connector1" class="connector"></div>
                        <div id="connector2" class="connector"></div>
                        <div id="connector3" class="connector"></div>
                        <div id="connector4" class="connector"></div>
                    </div>
                </div>
            </div>

            <div class="sidebar">
                <!-- Random Note Widget -->
                <div class="widget random-note-widget">
                    <div class="widget-header">
                        <h3>Random Note</h3>
                    </div>
                    <p id="random-note-content" class="random-note-content">The best way to predict the future is to invent it.</p>
                    <button class="random-note-btn" onclick="loadRandomNote()">Show Another</button>
                </div>

                <!-- Recent Activity Widget -->
                <div class="widget recent-activity-widget">
                    <div class="widget-header">
                        <h3>Recent Activity</h3>
                    </div>
                    <ul class="activity-list">
                        <li class="activity-item">
                            <span class="activity-title">Updated AI Tools Collection</span>
                            <span class="activity-meta">April 28, 2025</span>
                        </li>
                        <li class="activity-item">
                            <span class="activity-title">Added new Zettelkasten note</span>
                            <span class="activity-meta">April 27, 2025</span>
                        </li>
                        <li class="activity-item">
                            <span class="activity-title">Added new music albums</span>
                            <span class="activity-meta">April 25, 2025</span>
                        </li>
                        <li class="activity-item">
                            <span class="activity-title">Updated Project Status</span>
                            <span class="activity-meta">April 24, 2025</span>
                        </li>
                    </ul>
                </div>

                <!-- Quick Actions Widget -->
                <div class="widget quick-actions-widget">
                    <div class="widget-header">
                        <h3>Quick Actions</h3>
                    </div>
                    <div class="actions-grid">
                        <div class="action-btn" onclick="window.location.href='./new-note'">
                            <div class="action-icon">📝</div>
                            <p class="action-label">New Note</p>
                        </div>
                        <div class="action-btn" onclick="window.location.href='./journal/new'">
                            <div class="action-icon">📔</div>
                            <p class="action-label">Journal</p>
                        </div>
                        <div class="action-btn" onclick="window.location.href='./todo'">
                            <div class="action-icon">✅</div>
                            <p class="action-label">Todo</p>
                        </div>
                        <div class="action-btn" onclick="window.location.href='./settings'">
                            <div class="action-icon">⚙️</div>
                            <p class="action-label">Settings</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p>Last updated: <span id="last-updated">April 29, 2025</span> • Digital Garden v2.0</p>
        </div>
    </div>

    <script>
        // Function to draw connectors between nodes
        function


