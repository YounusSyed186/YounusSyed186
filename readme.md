<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Syed Younusuddin | Full-Stack Developer</title>
    <style>
        :root {
            --primary: #00FFFF;
            --secondary: #0a0a0a;
            --accent: #6366f1;
            --text: #e2e8f0;
            --card-bg: rgba(30, 41, 59, 0.7);
            --gradient: linear-gradient(135deg, #00FFFF 0%, #6366f1 100%);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--secondary);
            color: var(--text);
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .header {
            text-align: center;
            padding: 40px 0;
            background: var(--gradient);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 30px;
        }
        
        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }
        
        .typing-container {
            height: 40px;
            margin: 20px 0;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .typing-text {
            font-size: 1.2rem;
            font-weight: 500;
            overflow: hidden;
            border-right: 2px solid var(--primary);
            white-space: nowrap;
            animation: typing 4s steps(40, end), blink-caret 0.75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: var(--primary) }
        }
        
        .section {
            background-color: var(--card-bg);
            border-radius: 12px;
            padding: 25px;
            margin-bottom: 30px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .section-title {
            color: var(--primary);
            margin-bottom: 20px;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .section-title::after {
            content: '';
            flex: 1;
            height: 1px;
            background: linear-gradient(to right, var(--primary), transparent);
            margin-left: 10px;
        }
        
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .info-card {
            background: rgba(15, 23, 42, 0.7);
            padding: 20px;
            border-radius: 8px;
            border-left: 3px solid var(--primary);
        }
        
        .info-card h3 {
            color: var(--primary);
            margin-bottom: 10px;
            font-size: 1.1rem;
        }
        
        .contact-links {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
        }
        
        .contact-link {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 10px 15px;
            background: rgba(99, 102, 241, 0.2);
            border-radius: 6px;
            text-decoration: none;
            color: var(--text);
            transition: all 0.3s ease;
        }
        
        .contact-link:hover {
            background: rgba(99, 102, 241, 0.4);
            transform: translateY(-2px);
        }
        
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .skill-category {
            background: rgba(15, 23, 42, 0.7);
            padding: 20px;
            border-radius: 8px;
        }
        
        .skill-category h3 {
            color: var(--primary);
            margin-bottom: 15px;
            font-size: 1.2rem;
        }
        
        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .skill-tag {
            background: rgba(99, 102, 241, 0.2);
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
        }
        
        .chart-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 300px;
        }
        
        .pie-chart {
            position: relative;
            width: 250px;
            height: 250px;
            border-radius: 50%;
            background: conic-gradient(
                #3b82f6 0% 30%,
                #8b5cf6 30% 55%,
                #06b6d4 55% 75%,
                #10b981 75% 85%,
                #f59e0b 85% 100%
            );
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .pie-center {
            width: 120px;
            height: 120px;
            background: var(--secondary);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            color: var(--primary);
        }
        
        .chart-legend {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-left: 30px;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .legend-color {
            width: 15px;
            height: 15px;
            border-radius: 3px;
        }
        
        .legend-1 { background-color: #3b82f6; }
        .legend-2 { background-color: #8b5cf6; }
        .legend-3 { background-color: #06b6d4; }
        .legend-4 { background-color: #10b981; }
        .legend-5 { background-color: #f59e0b; }
        
        .footer {
            text-align: center;
            padding: 20px;
            margin-top: 30px;
            color: var(--text);
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .info-grid, .skills-container {
                grid-template-columns: 1fr;
            }
            
            .chart-container {
                flex-direction: column;
                height: auto;
            }
            
            .chart-legend {
                margin-left: 0;
                margin-top: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>🧑‍💻 Syed Younusuddin</h1>
        <p>Full-Stack Developer | AI Enthusiast</p>
        <div class="typing-container">
            <div class="typing-text">B.Tech CS (Data Science) Student | Technical Lead | Open-Source Contributor</div>
        </div>
    </div>
    
    <div class="section">
        <h2 class="section-title">👤 Personal & Academic Info</h2>
        <div class="info-grid">
            <div class="info-card">
                <h3>Personal Details</h3>
                <p><strong>Name:</strong> Syed Younusuddin</p>
                <p><strong>Location:</strong> Hyderabad, India</p>
                <p><strong>Languages:</strong> English, Hindi, Telugu</p>
            </div>
            <div class="info-card">
                <h3>Education</h3>
                <p><strong>College:</strong> Swami Vivekananda Institute of Technology, Hyderabad</p>
                <p><strong>Degree:</strong> B.Tech — Computer Science (Data Science)</p>
                <p><strong>Graduation Year:</strong> <span style="color: var(--primary);">2028</span></p>
            </div>
            <div class="info-card">
                <h3>Professional</h3>
                <p><strong>Current Role:</strong> Technical Lead @ Code Viveks Coding Club</p>
                <p><strong>Interests:</strong> Full-Stack Engineering, AI, Cloud, DevOps, System Architecture</p>
            </div>
        </div>
    </div>
    
    <div class="section">
        <h2 class="section-title">📞 Contact & Links</h2>
        <div class="contact-links">
            <a href="mailto:younussyed1011@gmail.com" class="contact-link">
                <span>📧</span> younussyed1011@gmail.com
            </a>
            <a href="https://linkedin.com/in/younus-syed-2b7913295" class="contact-link">
                <span>💼</span> LinkedIn
            </a>
            <a href="https://github.com/YounusSyed186" class="contact-link">
                <span>👨‍💻</span> GitHub
            </a>
            <a href="https://younussyed.netlify.app" class="contact-link">
                <span>🌍</span> Portfolio
            </a>
            <a href="tel:+916304898428" class="contact-link">
                <span>📱</span> +91 6304898428
            </a>
        </div>
    </div>
    
    <div class="section">
        <h2 class="section-title">🧠 Technical Skills</h2>
        <div class="skills-container">
            <div class="skill-category">
                <h3>💻 Programming</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Java</span>
                    <span class="skill-tag">JavaScript</span>
                    <span class="skill-tag">Python</span>
                    <span class="skill-tag">TypeScript</span>
                    <span class="skill-tag">Solidity</span>
                    <span class="skill-tag">SQL</span>
                </div>
            </div>
            <div class="skill-category">
                <h3>🎨 Frontend</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Next.js</span>
                    <span class="skill-tag">React</span>
                    <span class="skill-tag">TailwindCSS</span>
                    <span class="skill-tag">MUI</span>
                    <span class="skill-tag">SSR/ISR Rendering</span>
                </div>
            </div>
            <div class="skill-category">
                <h3>⚙ Backend</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Node.js</span>
                    <span class="skill-tag">Express.js</span>
                    <span class="skill-tag">WebSockets</span>
                    <span class="skill-tag">JWT</span>
                    <span class="skill-tag">Supabase</span>
                    <span class="skill-tag">Microservices</span>
                </div>
            </div>
            <div class="skill-category">
                <h3>🗄️ Databases</h3>
                <div class="skill-tags">
                    <span class="skill-tag">MongoDB</span>
                    <span class="skill-tag">PostgreSQL</span>
                    <span class="skill-tag">Supabase</span>
                    <span class="skill-tag">Redis (Basics)</span>
                </div>
            </div>
            <div class="skill-category">
                <h3>☁ DevOps & Cloud</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Docker (Basics)</span>
                    <span class="skill-tag">GitHub Actions</span>
                    <span class="skill-tag">CI/CD</span>
                    <span class="skill-tag">AWS (S3, Lambda)</span>
                    <span class="skill-tag">Nginx</span>
                    <span class="skill-tag">Vercel</span>
                </div>
            </div>
            <div class="skill-category">
                <h3>🧰 Tools</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Postman</span>
                    <span class="skill-tag">Figma</span>
                    <span class="skill-tag">System Design</span>
                    <span class="skill-tag">API Design</span>
                    <span class="skill-tag">Optimization</span>
                </div>
            </div>
        </div>
    </div>
    
    <div class="section">
        <h2 class="section-title">📊 Skill Distribution</h2>
        <div class="chart-container">
            <div class="pie-chart">
                <div class="pie-center">Skills</div>
            </div>
            <div class="chart-legend">
                <div class="legend-item">
                    <div class="legend-color legend-1"></div>
                    <span>Frontend (Next.js, React) - 30%</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color legend-2"></div>
                    <span>Backend (Node.js, APIs) - 25%</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color legend-3"></div>
                    <span>Databases - 20%</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color legend-4"></div>
                    <span>DevOps & Cloud - 10%</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color legend-5"></div>
                    <span>AI/ML + Learning - 15%</span>
                </div>
            </div>
        </div>
    </div>
    
    <div class="footer">
        <p>Always Learning 🔥 | Last Updated: 2024</p>
    </div>
</body>
</html>
