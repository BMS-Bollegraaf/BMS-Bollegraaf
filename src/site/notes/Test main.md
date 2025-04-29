---
{"dg-publish":true,"permalink":"/test-main/","tags":["gardenEntry"],"noteIcon":"default"}
---

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Digital Garden</title>
    <style>
        :root {
            --primary-color: #2a9d8f;
            --secondary-color: #264653;
            --accent-color: #e9c46a;
            --text-color: #333;
            --bg-color: #f8f9fa;
            --card-bg: #ffffff;
            --card-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --border-radius: 8px;
            --transition: all 0.3s ease;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--bg-color);
            margin: 0;
            padding: 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        /* Header Section */
        .header {
            text-align: center;
            margin-bottom: 2rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid #eaeaea;
        }

        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            color: var(--secondary-color);
        }

        .header p {
            font-size: 1.1rem;
            color: #666;
            max-width: 800px;
            margin: 0 auto;
        }

        /* Search Box */
        .search-container {
            margin: 2rem 0;
            text-align: center;
        }

        .search-box {
            width: 60%;
            padding: 0.8rem 1.5rem;
            font-size: 1rem;
            border: 2px solid #ddd;
            border-radius: 30px;
            outline: none;
            transition: var(--transition);
        }

        .search-box:focus {
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(42, 157, 143, 0.2);
        }

        /* Navigation Cards */
        .nav-cards {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .card {
            background-color: var(--card-bg);
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            padding: 1.5rem;
            transition: var(--transition);
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }

        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background-color: var(--primary-color);
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.3s ease;
        }

        .card:hover::before {
            transform: scaleX(1);
        }

        .card h3 {
            margin-top: 0;
            color: var(--secondary-color);
            font-size: 1.25rem;
        }

        .card p {
            margin-bottom: 0;
            color: #666;
            font-size: 0.9rem;
        }

        .card-icon {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }

        /* Recent Items */
        .recent-section {
            margin-bottom: 3rem;
        }

        .recent-section h2 {
            color: var(--secondary-color);
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .recent-items {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1rem;
        }

        .recent-item {
            background-color: var(--card-bg);
            border-radius: var(--border-radius);
            padding: 1rem;
            box-shadow: var(--card-shadow);
            transition: var(--transition);
        }

        .recent-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
        }

        .recent-item h4 {
            margin-top: 0;
            margin-bottom: 0.5rem;
            color: var(--secondary-color);
        }

        .recent-item p {
            margin-bottom: 0;
            font-size: 0.85rem;
            color: #777;
        }

        /* Random Note */
        .random-note {
            background-color: var(--card-bg);
            border-radius: var(--border-radius);
            padding: 1.5rem;
            box-shadow: var(--card-shadow);
            margin-bottom: 2rem;
            border-left: 4px solid var(--accent-color);
        }

        .random-note h3 {
            margin-top: 0;
            color: var(--secondary-color);
        }

        .random-note p {
            margin-bottom: 0.5rem;
        }

        .random-note-btn {
            background-color: var(--accent-color);
            color: #333;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.9rem;
            transition: var(--transition);
        }

        .random-note-btn:hover {
            background-color: #f4a261;
        }

        /* Footer */
        .footer {
            text-align: center;
            margin-top: 3rem;
            padding-top: 1.5rem;
            border-top: 1px solid #eaeaea;
            color: #666;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }

            .header h1 {
                font-size: 2rem;
            }

            .nav-cards {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }

            .search-box {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <h1>My Digital Garden</h1>
            <p>Welcome to my personal knowledge system - a place where I capture thoughts, projects, and discoveries.</p>
        </div>

        <!-- Search Box -->
        <div class="search-container">
            <input type="text" class="search-box" placeholder="Search my digital garden...">
        </div>

        <!-- Navigation Cards -->
        <div class="nav-cards">
            <!-- Projects Card -->
            <div class="card" onclick="window.location.href='./projects'">
                <div class="card-icon">📁</div>
                <h3>Projects</h3>
                <p>All my current and past projects with documentation, progress, and learnings.</p>
            </div>

            <!-- AI Tools Card -->
            <div class="card" onclick="window.location.href='./ai-tools'">
                <div class="card-icon">🤖</div>
                <h3>AI Tools</h3>
                <p>Documentation of all the AI tools I use and what they're useful for.</p>
            </div>

            <!-- Music Card -->
            <div class="card" onclick="window.location.href='./music'">
                <div class="card-icon">🎵</div>
                <h3>Music</h3>
                <p>Artists, albums, playlists, and musical discoveries I enjoy.</p>
            </div>

            <!-- Zettelkasten Card -->
            <div class="card" onclick="window.location.href='./zettelkasten'">
                <div class="card-icon">🧠</div>
                <h3>Zettelkasten</h3>
                <p>My interconnected thought system following the Zettelkasten method.</p>
            </div>

            <!-- Resources Card -->
            <div class="card" onclick="window.location.href='./resources'">
                <div class="card-icon">📚</div>
                <h3>Resources</h3>
                <p>Useful resources, references, and materials I've collected.</p>
            </div>

            <!-- Journal Card -->
            <div class="card" onclick="window.location.href='./journal'">
                <div class="card-icon">📔</div>
                <h3>Journal</h3>
                <p>Daily thoughts, reflections, and observations.</p>
            </div>
        </div>

        <!-- Random Note Section -->
        <div class="random-note">
            <h3>Random Thought</h3>
            <p id="random-note-content">Loading a random note from your garden...</p>
            <button class="random-note-btn" onclick="loadRandomNote()">Show me another</button>
        </div>

        <!-- Recent Items Section -->
        <div class="recent-section">
            <h2>Recently Updated</h2>
            <div class="recent-items" id="recent-items-container">
                <!-- These will be populated dynamically -->
                <div class="recent-item">
                    <h4>Sample Note Title</h4>
                    <p>Last updated: April 28, 2025</p>
                </div>
                <div class="recent-item">
                    <h4>Another Note Title</h4>
                    <p>Last updated: April 27, 2025</p>
                </div>
                <div class="recent-item">
                    <h4>Third Note Title</h4>
                    <p>Last updated: April 26, 2025</p>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p>Last updated: <span id="last-updated">April 29, 2025</span></p>
        </div>
    </div>

    <script>
        // Function to load a random note (placeholder)
        function loadRandomNote() {
            // This would normally fetch a random note from your system
            // For now, we'll just simulate it with some placeholder content
            const randomThoughts = [
                "The best way to predict the future is to invent it.",
                "Knowledge is like a garden: if it is not cultivated, it cannot be harvested.",
                "The more I learn, the more I realize how much I don't know.",
                "Everything is connected in ways we're just beginning to understand.",
                "Creativity is intelligence having fun."
            ];
            
            const randomIndex = Math.floor(Math.random() * randomThoughts.length);
            document.getElementById('random-note-content').textContent = randomThoughts[randomIndex];
        }

        // Initialize random note on page load
        document.addEventListener('DOMContentLoaded', loadRandomNote);

        // Update the last updated date
        document.getElementById('last-updated').textContent = new Date().toLocaleDateString();

        // This would normally be replaced with actual code to fetch your recent items
        // For now, it's just a placeholder
    </script>
</body>
</html>
