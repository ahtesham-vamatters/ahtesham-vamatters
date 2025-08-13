<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>✨ Cosmic Developer Profile ✨</title>
    <script src="https://unpkg.com/@lottiefiles/lottie-player@latest/dist/lottie-player.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;700&family=Pacifico&display=swap');
        
        :root {
            --primary: #ff4d79;
            --secondary: #6e45e2;
            --dark: #1a1a2e;
            --light: #fefefe;
            --accent: #00f5d4;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(135deg, var(--dark), #16213e);
            color: var(--light);
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }
        
        #particles-js {
            position: fixed;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        header {
            text-align: center;
            padding: 3rem 0;
            position: relative;
            overflow: hidden;
        }
        
        .title {
            font-size: 4rem;
            margin: 0;
            background: linear-gradient(to right, var(--primary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
            text-shadow: 0 0 20px rgba(255, 77, 121, 0.3);
            animation: pulse 2s infinite alternate;
        }
        
        .subtitle {
            font-size: 1.5rem;
            opacity: 0.9;
            margin-top: 1rem;
        }
        
        .avatar-container {
            width: 200px;
            height: 200px;
            margin: 2rem auto;
            border-radius: 50%;
            border: 5px solid var(--primary);
            box-shadow: 0 0 30px var(--primary);
            overflow: hidden;
            position: relative;
            transition: all 0.3s ease;
        }
        
        .avatar-container:hover {
            transform: scale(1.05);
            box-shadow: 0 0 50px var(--primary);
        }
        
        .avatar {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .section {
            background: rgba(26, 26, 46, 0.7);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 2rem;
            margin: 2rem 0;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s ease;
        }
        
        .section:hover {
            transform: translateY(-5px);
        }
        
        .section-title {
            font-size: 2rem;
            margin-top: 0;
            color: var(--accent);
            display: flex;
            align-items: center;
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .tech-item {
            background: rgba(110, 69, 226, 0.2);
            border: 1px solid rgba(110, 69, 226, 0.3);
            border-radius: 10px;
            padding: 1rem;
            text-align: center;
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .tech-item:hover {
            background: rgba(110, 69, 226, 0.4);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(110, 69, 226, 0.3);
        }
        
        .tech-icon {
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 1.5rem;
            text-align: center;
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--primary);
            margin: 0.5rem 0;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .project-card {
            background: linear-gradient(145deg, #1a1a2e, #16213e);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
            position: relative;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }
        
        .project-image {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }
        
        .project-content {
            padding: 1.5rem;
        }
        
        .project-title {
            font-size: 1.3rem;
            margin: 0 0 0.5rem 0;
        }
        
        .project-description {
            opacity: 0.8;
            font-size: 0.9rem;
        }
        
        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }
        
        .project-tag {
            background: rgba(0, 245, 212, 0.2);
            color: var(--accent);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }
        
        .social-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(145deg, var(--primary), var(--secondary));
            color: white;
            font-size: 1.5rem;
            transition: all 0.3s ease;
            text-decoration: none;
            box-shadow: 0 5px 15px rgba(255, 77, 121, 0.3);
        }
        
        .social-link:hover {
            transform: translateY(-5px) scale(1.1);
            box-shadow: 0 10px 20px rgba(255, 77, 121, 0.4);
        }
        
        footer {
            text-align: center;
            padding: 3rem 0;
            margin-top: 2rem;
            opacity: 0.8;
        }
        
        .heart {
            color: var(--primary);
            animation: heartbeat 1.5s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            100% { transform: scale(1.05); }
        }
        
        @keyframes heartbeat {
            0% { transform: scale(1); }
            25% { transform: scale(1.1); }
            50% { transform: scale(1); }
            75% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        
        .floating {
            animation: floating 3s ease-in-out infinite;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            .title {
                font-size: 2.5rem;
            }
            
            .subtitle {
                font-size: 1.2rem;
            }
            
            .tech-grid {
                grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div id="particles-js"></div>
    
    <div class="container">
        <header>
            <lottie-player 
                src="https://assets6.lottiefiles.com/packages/lf20_2glqweqs.json" 
                background="transparent" 
                speed="1" 
                style="width: 300px; height: 300px; margin: 0 auto;"
                loop 
                autoplay
                class="floating"
            ></lottie-player>
            
            <h1 class="title">Cosmic Developer</h1>
            <p class="subtitle">Crafting digital experiences that are out of this world 🚀</p>
            
            <div class="avatar-container">
                <img src="https://avatars.githubusercontent.com/u/yourusername" alt="Profile Avatar" class="avatar">
            </div>
        </header>
        
        <section class="section">
            <h2 class="section-title">
                <lottie-player 
                    src="https://assets1.lottiefiles.com/packages/lf20_vybwn7df.json" 
                    background="transparent" 
                    speed="1" 
                    style="width: 50px; height: 50px; margin-right: 15px;"
                    loop 
                    autoplay
                ></lottie-player>
                About Me
            </h2>
            
            <div style="display: flex; align-items: center; gap: 2rem; flex-wrap: wrap;">
                <div style="flex: 1; min-width: 300px;">
                    <p>Hello there! I'm a passionate developer who loves creating beautiful, functional, and innovative digital experiences. With a blend of creativity and technical expertise, I build solutions that push boundaries and delight users.</p>
                    <p>When I'm not coding, you can find me exploring new technologies, contributing to open source, or sharing knowledge with the developer community.</p>
                </div>
                
                <div style="flex: 1; min-width: 300px;">
                    <pre style="background: rgba(0,0,0,0.3); padding: 1rem; border-radius: 10px; overflow-x: auto;">
                        <code style="color: var(--accent);">
const developer = {
    pronouns: "he" | "she" | "they",
    code: ["JavaScript", "Python", "TypeScript"],
    askMeAbout: ["web dev", "tech", "ai"],
    currentFocus: "Building the future",
    funFact: "I can solve a Rubik's cube blindfolded"
};
                        </code>
                    </pre>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title">
                <lottie-player 
                    src="https://assets1.lottiefiles.com/packages/lf20_yo4mry.json" 
                    background="transparent" 
                    speed="1" 
                    style="width: 50px; height: 50px; margin-right: 15px;"
                    loop 
                    autoplay
                ></lottie-player>
                My Tech Stack
            </h2>
            
            <div class="tech-grid">
                <div class="tech-item">
                    <div class="tech-icon">⚛️</div>
                    <div>React</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🐍</div>
                    <div>Python</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🚀</div>
                    <div>Node.js</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">💎</div>
                    <div>Ruby on Rails</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">📱</div>
                    <div>React Native</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🛢️</div>
                    <div>MongoDB</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">☁️</div>
                    <div>AWS</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🤖</div>
                    <div>TensorFlow</div>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title">
                <lottie-player 
                    src="https://assets1.lottiefiles.com/packages/lf20_issf4flx.json" 
                    background="transparent" 
                    speed="1" 
                    style="width: 50px; height: 50px; margin-right: 15px;"
                    loop 
                    autoplay
                ></lottie-player>
                GitHub Stats
            </h2>
            
            <div class="stats-container">
                <div class="stat-card">
                    <div>Total Contributions</div>
                    <div class="stat-number">1,248</div>
                    <div>Last year</div>
                </div>
                <div class="stat-card">
                    <div>Repositories</div>
                    <div class="stat-number">42</div>
                    <div>Public & Private</div>
                </div>
                <div class="stat-card">
                    <div>Streak</div>
                    <div class="stat-number">128</div>
                    <div>Days and counting</div>
                </div>
            </div>
            
            <div style="display: flex; justify-content: center; margin-top: 2rem; flex-wrap: wrap; gap: 1rem;">
                <img src="https://github-readme-stats.vercel.app/api?username=yourusername&show_icons=true&theme=radical" alt="GitHub Stats">
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=yourusername&layout=compact&theme=radical" alt="Top Languages">
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title">
                <lottie-player 
                    src="https://assets1.lottiefiles.com/packages/lf20_5tkzkblw.json" 
                    background="transparent" 
                    speed="1" 
                    style="width: 50px; height: 50px; margin-right: 15px;"
                    loop 
                    autoplay
                ></lottie-player>
                Featured Projects
            </h2>
            
            <div class="projects-grid">
                <div class="project-card">
                    <img src="https://via.placeholder.com/600x400/6e45e2/ffffff?text=AI+Platform" alt="Project 1" class="project-image">
                    <div class="project-content">
                        <h3 class="project-title">AI Content Platform</h3>
                        <p class="project-description">Next-gen content generation platform powered by GPT-3 and custom ML models.</p>
                        <div class="project-tags">
                            <span class="project-tag">AI</span>
                            <span class="project-tag">React</span>
                            <span class="project-tag">Node.js</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <img src="https://via.placeholder.com/600x400/ff4d79/ffffff?text=Blockchain+App" alt="Project 2" class="project-image">
                    <div class="project-content">
                        <h3 class="project-title">Blockchain Explorer</h3>
                        <p class="project-description">Interactive explorer for Ethereum blockchain with real-time analytics.</p>
                        <div class="project-tags">
                            <span class="project-tag">Blockchain</span>
                            <span class="project-tag">Web3</span>
                            <span class="project-tag">TypeScript</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <img src="https://via.placeholder.com/600x400/00f5d4/ffffff?text=AR+Experience" alt="Project 3" class="project-image">
                    <div class="project-content">
                        <h3 class="project-title">AR Shopping Assistant</h3>
                        <p class="project-description">Augmented reality app that helps users visualize products in their space.</p>
                        <div class="project-tags">
                            <span class="project-tag">AR</span>
                            <span class="project-tag">Unity</span>
                            <span class="project-tag">C#</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title">
                <lottie-player 
                    src="https://assets1.lottiefiles.com/packages/lf20_mjlh3hcy.json" 
                    background="transparent" 
                    speed="1" 
                    style="width: 50px; height: 50px; margin-right: 15px;"
                    loop 
                    autoplay
                ></lottie-player>
                Let's Connect!
            </h2>
            
            <div style="text-align: center; margin-bottom: 2rem;">
                <p>I'm always open to interesting conversations, collaborations, or just saying hi!</p>
            </div>
            
            <div class="social-links">
                <a href="https://github.com/yourusername" class="social-link" target="_blank">👾</a>
                <a href="https://linkedin.com/in/yourprofile" class="social-link" target="_blank">💼</a>
                <a href="https://twitter.com/yourhandle" class="social-link" target="_blank">🐦</a>
                <a href="https://instagram.com/yourprofile" class="social-link" target="_blank">📸</a>
                <a href="mailto:youremail@example.com" class="social-link" target="_blank">✉️</a>
            </div>
        </section>
        
        <footer>
            <p>Made with <span class="heart">❤️</span> and too much coffee</p>
            <p>© 2023 Cosmic Developer | Keep coding awesome stuff!</p>
        </footer>
    </div>
    
    <script>
        // Initialize particles.js
        particlesJS("particles-js", {
            "particles": {
                "number": {
                    "value": 80,
                    "density": {
                        "enable": true,
                        "value_area": 800
                    }
                },
                "color": {
                    "value": ["#ff4d79", "#6e45e2", "#00f5d4"]
                },
                "shape": {
                    "type": "circle",
                    "stroke": {
                        "width": 0,
                        "color": "#000000"
                    },
                    "polygon": {
                        "nb_sides": 5
                    }
                },
                "opacity": {
                    "value": 0.5,
                    "random": false,
                    "anim": {
                        "enable": false,
                        "speed": 1,
                        "opacity_min": 0.1,
                        "sync": false
                    }
                },
                "size": {
                    "value": 3,
                    "random": true,
                    "anim": {
                        "enable": false,
                        "speed": 40,
                        "size_min": 0.1,
                        "sync": false
                    }
                },
                "line_linked": {
                    "enable": true,
                    "distance": 150,
                    "color": "#6e45e2",
                    "opacity": 0.4,
                    "width": 1
                },
                "move": {
                    "enable": true,
                    "speed": 2,
                    "direction": "none",
                    "random": false,
                    "straight": false,
                    "out_mode": "out",
                    "bounce": false,
                    "attract": {
                        "enable": false,
                        "rotateX": 600,
                        "rotateY": 1200
                    }
                }
            },
            "interactivity": {
                "detect_on": "canvas",
                "events": {
                    "onhover": {
                        "enable": true,
                        "mode": "grab"
                    },
                    "onclick": {
                        "enable": true,
                        "mode": "push"
                    },
                    "resize": true
                },
                "modes": {
                    "grab": {
                        "distance": 140,
                        "line_linked": {
                            "opacity": 1
                        }
                    },
                    "bubble": {
                        "distance": 400,
                        "size": 40,
                        "duration": 2,
                        "opacity": 8,
                        "speed": 3
                    },
                    "repulse": {
                        "distance": 200,
                        "duration": 0.4
                    },
                    "push": {
                        "particles_nb": 4
                    },
                    "remove": {
                        "particles_nb": 2
                    }
                }
            },
            "retina_detect": true
        });
        
        // Add floating animation to project cards
        const projectCards = document.querySelectorAll('.project-card');
        projectCards.forEach((card, index) => {
            card.style.animationDelay = `${index * 0.1}s`;
            card.classList.add('floating');
        });
    </script>
</body>
</html>
