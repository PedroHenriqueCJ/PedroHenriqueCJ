<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pedro Henrique - Full Stack Developer</title>
    <style>
        :root {
            --rp-base: #191724;
            --rp-surface: #1f1d2e;
            --rp-overlay: #26233a;
            --rp-muted: #6e6a86;
            --rp-subtle: #908caa;
            --rp-text: #e0def4;
            --rp-love: #eb6f92;
            --rp-gold: #f6c177;
            --rp-rose: #ebbcba;
            --rp-pine: #31748f;
            --rp-foam: #9ccfd8;
            --rp-iris: #c4a7e7;
            --rp-highlight-low: #21202e;
            --rp-highlight-med: #403d52;
            --rp-highlight-high: #524f67;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--rp-base);
            color: var(--rp-text);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            text-align: center;
            padding: 60px 0;
            background: linear-gradient(to bottom, var(--rp-surface), var(--rp-base));
            border-bottom: 1px solid var(--rp-highlight-med);
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at top right, var(--rp-iris), transparent 70%);
            opacity: 0.1;
            z-index: 0;
        }

        .profile-header {
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            background: linear-gradient(135deg, var(--rp-text), var(--rp-foam));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
        }

        h2 {
            font-size: 1.8rem;
            color: var(--rp-subtle);
            margin-bottom: 20px;
            font-weight: 400;
        }

        .typing-container {
            min-height: 60px;
            margin: 20px 0;
        }

        .typing-text {
            font-size: 1.5rem;
            color: var(--rp-foam);
            display: inline-block;
            overflow: hidden;
            border-right: 2px solid var(--rp-foam);
            white-space: nowrap;
            animation: typing 4s steps(40, end), blink-caret 0.75s step-end infinite;
        }

        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }

        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: var(--rp-foam) }
        }

        /* Section Styles */
        section {
            padding: 60px 0;
            border-bottom: 1px solid var(--rp-highlight-med);
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }

        .section-title h2 {
            font-size: 2.2rem;
            display: inline-block;
            padding-bottom: 10px;
            color: var(--rp-rose);
        }

        .section-title h2::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: linear-gradient(to right, var(--rp-love), var(--rp-iris));
            border-radius: 3px;
        }

        /* About Me */
        .about-content {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 40px;
        }

        .about-text {
            flex: 1;
            min-width: 300px;
        }

        .about-text p {
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .philosophy {
            background: var(--rp-overlay);
            padding: 25px;
            border-radius: 12px;
            border-left: 4px solid var(--rp-pine);
            margin-top: 20px;
        }

        .philosophy p {
            font-style: italic;
            color: var(--rp-subtle);
            margin: 0;
        }

        /* Skills */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 20px;
        }

        .skill-category {
            background: var(--rp-overlay);
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-5px);
        }

        .skill-category h3 {
            color: var(--rp-gold);
            margin-bottom: 15px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
        }

        .skill-category h3 i {
            margin-right: 10px;
        }

        .skill-items {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill-item {
            background: var(--rp-highlight-med);
            color: var(--rp-text);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: inline-block;
        }

        /* Projects */
        .project-card {
            background: var(--rp-overlay);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            margin-bottom: 30px;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }

        .project-content {
            padding: 25px;
        }

        .project-title {
            color: var(--rp-foam);
            font-size: 1.5rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }

        .project-title i {
            margin-right: 10px;
            color: var(--rp-iris);
        }

        .project-description {
            margin-bottom: 20px;
            color: var(--rp-subtle);
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }

        .tech-tag {
            background: linear-gradient(to right, var(--rp-pine), var(--rp-foam));
            color: var(--rp-base);
            padding: 5px 12px;
            border-radius: 15px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .project-link {
            display: inline-block;
            background: var(--rp-iris);
            color: var(--rp-base);
            padding: 10px 20px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 600;
            transition: background 0.3s ease;
        }

        .project-link:hover {
            background: var(--rp-rose);
        }

        /* Stats */
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .stat-card {
            background: var(--rp-overlay);
            padding: 25px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--rp-gold);
            margin-bottom: 10px;
        }

        .stat-label {
            color: var(--rp-subtle);
            font-size: 1rem;
        }

        /* Contact */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .contact-card {
            background: var(--rp-overlay);
            padding: 25px;
            border-radius: 12px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .contact-card:hover {
            transform: translateY(-5px);
        }

        .contact-icon {
            font-size: 2rem;
            margin-bottom: 15px;
            color: var(--rp-iris);
        }

        .contact-title {
            color: var(--rp-text);
            margin-bottom: 10px;
            font-size: 1.2rem;
        }

        .contact-link {
            color: var(--rp-subtle);
            text-decoration: none;
            transition: color 0.3s ease;
            display: inline-block;
        }

        .contact-link:hover {
            color: var(--rp-foam);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 40px 0;
            color: var(--rp-subtle);
            background: var(--rp-surface);
        }

        .quote {
            font-style: italic;
            margin-bottom: 20px;
            color: var(--rp-rose);
            font-size: 1.1rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
            
            .typing-text {
                font-size: 1.2rem;
            }
            
            .stats-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <header>
        <div class="container">
            <div class="profile-header">
                <h1>Pedro Henrique Cerqueira de Jesus</h1>
                <h2>💻 Full-Stack Developer | 🎨 UX/UI Designer</h2>
                <div class="typing-container">
                    <p class="typing-text">Crafting seamless digital experiences with code and design</p>
                </div>
            </div>
        </div>
    </header>

    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2><i class="fas fa-user"></i> About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <p>Sou Pedro Henrique Cerqueira de Jesus, um desenvolvedor <strong>Full-Stack e UX/UI Designer</strong> de São Gonçalo dos Campos. Gosto de criar soluções digitais que funcionem de forma impecável, mas que também sejam visualmente elegantes — interfaces que não apenas funcionam, mas contam histórias.</p>
                    <p>Minha abordagem integra conhecimentos técnicos sólidos com princípios de design centrado no usuário para criar experiências que não apenas funcionam perfeitamente, mas também contam histórias e geram impacto.</p>
                    <div class="philosophy">
                        <p>"Interfaces devem ser intuitivas, código deve ser limpo, e a experiência do usuário deve ser memorável."</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <div class="section-title">
                <h2><i class="fas fa-laptop-code"></i> Technical Skills</h2>
            </div>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fas fa-code"></i> Frontend</h3>
                    <div class="skill-items">
                        <span class="skill-item">HTML5</span>
                        <span class="skill-item">CSS3</span>
                        <span class="skill-item">JavaScript</span>
                        <span class="skill-item">TypeScript</span>
                        <span class="skill-item">React</span>
                        <span class="skill-item">SASS</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-server"></i> Backend</h3>
                    <div class="skill-items">
                        <span class="skill-item">Java</span>
                        <span class="skill-item">PHP</span>
                        <span class="skill-item">C#</span>
                        <span class="skill-item">Python</span>
                        <span class="skill-item">Node.js</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-database"></i> Database</h3>
                    <div class="skill-items">
                        <span class="skill-item">MySQL</span>
                        <span class="skill-item">MongoDB</span>
                        <span class="skill-item">PostgreSQL</span>
                        <span class="skill-item">SQLite</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-paint-brush"></i> Design</h3>
                    <div class="skill-items">
                        <span class="skill-item">Figma</span>
                        <span class="skill-item">Adobe XD</span>
                        <span class="skill-item">UI/UX Design</span>
                        <span class="skill-item">Prototyping</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-tools"></i> Tools</h3>
                    <div class="skill-items">
                        <span class="skill-item">Git</span>
                        <span class="skill-item">GitHub</span>
                        <span class="skill-item">VS Code</span>
                        <span class="skill-item">Docker</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="container">
            <div class="section-title">
                <h2><i class="fas fa-project-diagram"></i> Featured Projects</h2>
            </div>
            
            <div class="project-card">
                <div class="project-content">
                    <h3 class="project-title"><i class="fas fa-trello"></i> Kards - Trello Clone</h3>
                    <p class="project-description">Uma aplicação web inspirada no Trello para gerenciamento de tarefas com funcionalidades de arrastar e soltar, desenvolvida com React e TypeScript.</p>
                    <div class="project-tech">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">TypeScript</span>
                        <span class="tech-tag">CSS Modules</span>
                        <span class="tech-tag">LocalStorage API</span>
                    </div>
                    <a href="https://github.com/PedroHenriqueCJ/Kards-Trello-clone" class="project-link">View Project</a>
                </div>
            </div>
        </div>
    </section>

    <section id="stats">
        <div class="container">
            <div class="section-title">
                <h2><i class="fas fa-chart-line"></i> GitHub Statistics</h2>
            </div>
            
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-number">42</div>
                    <div class="stat-label">Repositories</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">1,248</div>
                    <div class="stat-label">Commits</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">86</div>
                    <div class="stat-label">Followers</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">24</div>
                    <div class="stat-label">Projects</div>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 30px;">
                <img src="https://github-readme-stats.vercel.app/api?username=PedroHenriqueCJ&show_icons=true&theme=rose_pine" alt="GitHub Stats" style="max-width: 100%; border-radius: 10px;">
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=PedroHenriqueCJ&layout=compact&theme=rose_pine" alt="Top Languages" style="max-width: 100%; border-radius: 10px; margin-top: 20px;">
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <div class="section-title">
                <h2><i class="fas fa-envelope"></i> Connect With Me</h2>
            </div>
            
            <div class="contact-grid">
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fab fa-linkedin"></i>
                    </div>
                    <h3 class="contact-title">LinkedIn</h3>
                    <a href="https://www.linkedin.com/in/pedro-henrique-cerqueira-de-jesus-26b116318" class="contact-link">/in/pedrohenrique</a>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fab fa-github"></i>
                    </div>
                    <h3 class="contact-title">GitHub</h3>
                    <a href="https://github.com/PedroHenriqueCJ" class="contact-link">@PedroHenriqueCJ</a>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fab fa-instagram"></i>
                    </div>
                    <h3 class="contact-title">Instagram</h3>
                    <a href="https://instagram.com/Beu266" class="contact-link">@Beu266</a>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <h3 class="contact-title">Email</h3>
                    <a href="mailto:pedrohenriquecerqueiraj@gmail.com" class="contact-link">pedrohenriquecerqueiraj@gmail.com</a>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p class="quote">"Code is like humor. When you have to explain it, it's bad." – Cory House</p>
            <p>© 2023 Pedro Henrique Cerqueira de Jesus. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Simple typing effect
        document.addEventListener('DOMContentLoaded', function() {
            const phrases = [
                "Crafting seamless digital experiences with code and design",
                "Building functional and beautiful user interfaces",
                "Transforming ideas into digital reality"
            ];
            let currentPhrase = 0;
            const typingElement = document.querySelector('.typing-text');
            
            function typeNextPhrase() {
                typingElement.textContent = phrases[currentPhrase];
                typingElement.style.width = '0';
                typingElement.style.animation = 'none';
                void typingElement.offsetWidth; // Trigger reflow
                typingElement.style.animation = null;
                
                currentPhrase = (currentPhrase + 1) % phrases.length;
                
                setTimeout(typeNextPhrase, 4000);
            }
            
            typeNextPhrase();
        });
    </script>
</body>
</html>
