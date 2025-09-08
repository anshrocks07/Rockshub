<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GameTutorHub - Share Your Gaming Knowledge</title>
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #0f0f1a;
            color: #f0f0f0;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: #1a1a2e;
            padding: 20px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .logo {
            font-size: 28px;
            font-weight: 700;
            color: #6c5ce7;
            display: inline-block;
        }
        
        .logo span {
            color: #a29bfe;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: #f0f0f0;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: #6c5ce7;
        }
        
        .btn {
            display: inline-block;
            background-color: #6c5ce7;
            color: white;
            padding: 10px 20px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: #5d4ae0;
            transform: translateY(-2px);
        }
        
        /* Hero Section */
        .hero {
            padding: 80px 0;
            text-align: center;
            background: linear-gradient(to bottom, #1a1a2e, #0f0f1a);
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #6c5ce7, #a29bfe);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .hero p {
            font-size: 20px;
            max-width: 700px;
            margin: 0 auto 30px;
            color: #b2b2b2;
        }
        
        /* Content Sections */
        .section-title {
            text-align: center;
            margin: 60px 0 40px;
            font-size: 32px;
            color: #6c5ce7;
        }
        
        .content-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }
        
        .content-card {
            background-color: #1a1a2e;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .content-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        .card-img {
            height: 180px;
            background-color: #2d2d4b;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #6c5ce7;
            font-size: 50px;
        }
        
        .card-content {
            padding: 20px;
        }
        
        .card-content h3 {
            margin-bottom: 10px;
            font-size: 20px;
        }
        
        .card-content p {
            color: #b2b2b2;
            margin-bottom: 15px;
            font-size: 14px;
        }
        
        .card-meta {
            display: flex;
            justify-content: space-between;
            color: #777;
            font-size: 12px;
        }
        
        /* Upload Section */
        .upload-section {
            background-color: #1a1a2e;
            padding: 60px 0;
            text-align: center;
        }
        
        .upload-form {
            max-width: 600px;
            margin: 0 auto;
            background-color: #23233d;
            padding: 30px;
            border-radius: 10px;
            text-align: left;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            background-color: #2d2d4b;
            border: 1px solid #3d3d5c;
            border-radius: 5px;
            color: white;
            font-size: 16px;
        }
        
        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background-color: #1a1a2e;
            padding: 40px 0;
            text-align: center;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            list-style: none;
            margin: 20px 0;
        }
        
        .footer-links li {
            margin: 0 15px;
        }
        
        .footer-links a {
            color: #b2b2b2;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: #6c5ce7;
        }
        
        .copyright {
            color: #777;
            margin-top: 20px;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .content-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">Game<span>Tutor</span>Hub</a>
                <ul class="nav-links">
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Tutorials</a></li>
                    <li><a href="#">Apps</a></li>
                    <li><a href="#">Community</a></li>
                    <li><a href="#">About</a></li>
                </ul>
                <a href="#" class="btn">Login/Signup</a>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Share Your Gaming Expertise</h1>
            <p>Upload tutorials, share gaming content, and distribute apps to help fellow gamers level up their skills.</p>
            <a href="#upload" class="btn">Upload Content</a>
        </div>
    </section>

    <!-- Featured Tutorials -->
    <section class="container">
        <h2 class="section-title">Featured Tutorials</h2>
        <div class="content-grid">
            <div class="content-card">
                <div class="card-img">🎮</div>
                <div class="card-content">
                    <h3>Advanced Apex Legends Movement</h3>
                    <p>Learn how to master movement techniques in Apex Legends to outmaneuver your opponents.</p>
                    <div class="card-meta">
                        <span>By: ProGamer92</span>
                        <span>2 days ago</span>
                    </div>
                </div>
            </div>
            
            <div class="content-card">
                <div class="card-img">🕹️</div>
                <div class="card-content">
                    <h3>Elden Ring Boss Strategies</h3>
                    <p>Complete guide to defeating all major bosses in Elden Ring with minimal equipment.</p>
                    <div class="card-meta">
                        <span>By: SoulMaster</span>
                        <span>1 week ago</span>
                    </div>
                </div>
            </div>
            
            <div class="content-card">
                <div class="card-img">🎯</div>
                <div class="card-content">
                    <h3>VALORANT Aim Training Routine</h3>
                    <p>Daily exercises to improve your aim and reaction time in VALORANT.</p>
                    <div class="card-meta">
                        <span>By: Shoot3r</span>
                        <span>3 days ago</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gaming Apps -->
    <section class="container">
        <h2 class="section-title">Gaming Apps & Tools</h2>
        <div class="content-grid">
            <div class="content-card">
                <div class="card-img">📱</div>
                <div class="card-content">
                    <h3>FPS Monitor Tool</h3>
                    <p>Real-time performance monitoring app that helps you optimize game settings.</p>
                    <div class="card-meta">
                        <span>Version: 2.1.4</span>
                        <span>12.5MB</span>
                    </div>
                </div>
            </div>
            
            <div class="content-card">
                <div class="card-img">🖥️</div>
                <div class="card-content">
                    <h3>GameMap Designer</h3>
                    <p>Create custom maps for popular games with this easy-to-use editor.</p>
                    <div class="card-meta">
                        <span>Version: 1.0.3</span>
                        <span>48.7MB</span>
                    </div>
                </div>
            </div>
            
            <div class="content-card">
                <div class="card-img">🎵</div>
                <div class="card-content">
                    <h3>GameSound Extractor</h3>
                    <p>Extract and customize game sound effects and music tracks.</p>
                    <div class="card-meta">
                        <span>Version: 3.2.0</span>
                        <span>23.1MB</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Upload Section -->
    <section id="upload" class="upload-section">
        <div class="container">
            <h2 class="section-title">Upload Content</h2>
            <div class="upload-form">
                <div class="form-group">
                    <label for="content-type">Content Type</label>
                    <select id="content-type" class="form-control">
                        <option value="">Select Content Type</option>
                        <option value="tutorial">Tutorial</option>
                        <option value="app">App/Software</option>
                        <option value="video">Video Content</option>
                        <option value="other">Other</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label for="title">Title</label>
                    <input type="text" id="title" class="form-control" placeholder="Enter title">
                </div>
                
                <div class="form-group">
                    <label for="description">Description</label>
                    <textarea id="description" class="form-control" placeholder="Describe your content"></textarea>
                </div>
                
                <div class="form-group">
                    <label for="file">Upload File</label>
                    <input type="file" id="file" class="form-control">
                </div>
                
                <div class="form-group">
                    <label for="thumbnail">Thumbnail Image</label>
                    <input type="file" id="thumbnail" class="form-control" accept="image/*">
                </div>
                
                <button type="submit" class="btn">Submit Content</button>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <a href="#" class="logo">Game<span>Tutor</span>Hub</a>
            <ul class="footer-links">
                <li><a href="#">Home</a></li>
                <li><a href="#">Tutorials</a></li>
                <li><a href="#">Apps</a></li>
                <li><a href="#">Community</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Privacy Policy</a></li>
                <li><a href="#">Terms of Service</a></li>
            </ul>
            <p class="copyright">© 2023 GameTutorHub. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Simple form handling
        document.addEventListener('DOMContentLoaded', function() {
            const uploadForm = document.querySelector('.upload-form');
            
            uploadForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                const contentType = document.getElementById('content-type').value;
                const title = document.getElementById('title').value;
                const description = document.getElementById('description').value;
                
                if (!contentType || !title || !description) {
                    alert('Please fill in all required fields');
                    return;
                }
                
                // In a real application, you would send this data to a server
                alert('Content uploaded successfully! (This is a demo - no actual upload occurred)');
                uploadForm.reset();
            });
        });
    </script>
</body>
</html>
