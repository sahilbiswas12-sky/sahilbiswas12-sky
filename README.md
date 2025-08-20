<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sahil Biswas - Full Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #6e44ff;
            --secondary: #ff4d7c;
            --dark: #1a1a2e;
            --darker: #0d0d1a;
            --light: #f0f0f5;
            --accent: #2ec4b6;
            --gradient: linear-gradient(135deg, var(--primary), var(--secondary));
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--darker);
            color: var(--light);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background: var(--dark);
            padding: 2rem 0;
            position: relative;
            overflow: hidden;
        }
        
        .header-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            position: relative;
            z-index: 2;
        }
        
        .profile {
            display: flex;
            align-items: center;
            gap: 20px;
        }
        
        .profile-img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 4px solid var(--primary);
            background: #2a2a4a;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            color: var(--primary);
        }
        
        .profile-text h1 {
            font-size: 2.5rem;
            margin-bottom: 5px;
            background: var(--gradient);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .profile-text h2 {
            font-size: 1.2rem;
            font-weight: 400;
            color: var(--accent);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 10px;
        }
        
        .social-links a {
            color: var(--light);
            font-size: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        .header-bg {
            position: absolute;
            top: 0;
            right: 0;
            width: 50%;
            height: 100%;
            background: var(--gradient);
            opacity: 0.1;
            clip-path: polygon(100% 0, 100% 100%, 0 0);
            z-index: 1;
        }
        
        section {
            padding: 4rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            display: inline-block;
            background: var(--gradient);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--gradient);
            border-radius: 2px;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
        }
        
        .about-text p {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }
        
        .about-highlights {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid var(--primary);
        }
        
        .highlight {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .highlight i {
            color: var(--accent);
            font-size: 1.2rem;
            margin-right: 10px;
        }
        
        .tech-stack {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .tech-category {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }
        
        .tech-category:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.08);
        }
        
        .tech-category h3 {
            color: var(--accent);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .tech-category h3 i {
            color: var(--primary);
        }
        
        .tech-items {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .tech-item {
            background: rgba(110, 68, 255, 0.15);
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .tech-item i {
            color: var(--primary);
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.08);
        }
        
        .stat-card i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .stat-card h3 {
            font-size: 2rem;
            margin-bottom: 5px;
            color: var(--accent);
        }
        
        .github-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .github-stat {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
        }
        
        .github-stat img {
            max-width: 100%;
            border-radius: 5px;
        }
        
        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
        }
        
        .project-img {
            height: 180px;
            background: var(--gradient);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .project-img i {
            font-size: 3rem;
            color: white;
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-content h3 {
            color: var(--accent);
            margin-bottom: 10px;
        }
        
        .project-content p {
            margin-bottom: 15px;
            font-size: 0.95rem;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }
        
        .project-tech span {
            background: rgba(110, 68, 255, 0.15);
            padding: 3px 10px;
            border-radius: 15px;
            font-size: 0.8rem;
        }
        
        .project-links {
            display: flex;
            gap: 15px;
        }
        
        .project-links a {
            color: var(--light);
            text-decoration: none;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: color 0.3s ease;
        }
        
        .project-links a:hover {
            color: var(--primary);
        }
        
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .contact-item i {
            font-size: 1.5rem;
            color: var(--primary);
            width: 40px;
            height: 40px;
            background: rgba(110, 68, 255, 0.15);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 12px 15px;
            margin-bottom: 15px;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 5px;
            color: var(--light);
            font-size: 1rem;
        }
        
        .contact-form textarea {
            min-height: 120px;
            resize: vertical;
        }
        
        .btn {
            background: var(--gradient);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 5px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }
        
        .btn:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }
        
        footer {
            background: var(--dark);
            padding: 2rem 0;
            text-align: center;
            margin-top: 4rem;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
        }
        
        .footer-links {
            display: flex;
            gap: 20px;
        }
        
        .footer-links a {
            color: var(--light);
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-links a:hover {
            color: var(--primary);
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
                gap: 20px;
            }
            
            .profile {
                flex-direction: column;
            }
            
            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
            }
            
            .github-stats {
                grid-template-columns: 1fr;
            }
        }
        
        /* Animation for elements */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .animate {
            animation: fadeIn 1s ease forwards;
        }
        
        .delay-1 {
            animation-delay: 0.2s;
        }
        
        .delay-2 {
            animation-delay: 0.4s;
        }
        
        .delay-3 {
            animation-delay: 0.6s;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="profile">
                    <div class="profile-img">
                        <i class="fas fa-user"></i>
                    </div>
                    <div class="profile-text">
                        <h1>Sahil Biswas</h1>
                        <h2>Full Stack Web Developer | MERN Stack Practitioner</h2>
                        <div class="social-links">
                            <a href="https://github.com/sahilbiswas12-sky" target="_blank"><i class="fab fa-github"></i></a>
                            <a href="https://www.linkedin.com/in/sahil-biswas-827337287" target="_blank"><i class="fab fa-linkedin"></i></a>
                            <a href="mailto:sahilbiswas890@gmail.com"><i class="fas fa-envelope"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="header-bg"></div>
    </header>

    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <p>I'm a passionate Full Stack Web Developer currently pursuing B.Tech in Computer Science and Design. I enjoy creating innovative web solutions and have expertise in both frontend and backend technologies.</p>
                    <p>With a strong foundation in programming languages like C, C++, Java, and Python, I'm constantly expanding my skill set to include modern technologies and best practices in web development.</p>
                    <p>I'm actively learning and exploring the MERN stack and system design principles. I believe in writing clean, efficient code to solve real-world problems and am always open to collaborating on impactful projects.</p>
                </div>
                <div class="about-highlights">
                    <div class="highlight">
                        <i class="fas fa-graduation-cap"></i>
                        <p>Pursuing B.Tech in Computer Science and Design</p>
                    </div>
                    <div class="highlight">
                        <i class="fas fa-laptop-code"></i>
                        <p>Full Stack Web Development</p>
                    </div>
                    <div class="highlight">
                        <i class="fas fa-rocket"></i>
                        <p>MERN Stack Enthusiast</p>
                    </div>
                    <div class="highlight">
                        <i class="fas fa-hands-helping"></i>
                        <p>Open to Collaborations</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="tech-stack">
        <div class="container">
            <div class="section-title">
                <h2>Tech Stack</h2>
            </div>
            <div class="tech-stack">
                <div class="tech-category animate">
                    <h3><i class="fas fa-paint-brush"></i> Frontend</h3>
                    <div class="tech-items">
                        <div class="tech-item"><i class="fab fa-html5"></i> HTML5</div>
                        <div class="tech-item"><i class="fab fa-css3-alt"></i> CSS3</div>
                        <div class="tech-item"><i class="fab fa-js"></i> JavaScript</div>
                        <div class="tech-item"><i class="fab fa-react"></i> React</div>
                        <div class="tech-item"><i class="fas fa-bold"></i> Bootstrap</div>
                        <div class="tech-item"><i class="fas fa-wind"></i> TailwindCSS</div>
                    </div>
                </div>
                
                <div class="tech-category animate delay-1">
                    <h3><i class="fas fa-server"></i> Backend</h3>
                    <div class="tech-items">
                        <div class="tech-item"><i class="fab fa-php"></i> PHP</div>
                        <div class="tech-item"><i class="fab fa-node-js"></i> Node.js</div>
                        <div class="tech-item"><i class="fas fa-bolt"></i> Express.js</div>
                    </div>
                </div>
                
                <div class="tech-category animate delay-2">
                    <h3><i class="fas fa-database"></i> Databases</h3>
                    <div class="tech-items">
                        <div class="tech-item"><i class="fas fa-database"></i> MySQL</div>
                        <div class="tech-item"><i class="fas fa-leaf"></i> MongoDB</div>
                    </div>
                </div>
                
                <div class="tech-category animate delay-3">
                    <h3><i class="fas fa-code"></i> Programming</h3>
                    <div class="tech-items">
                        <div class="tech-item">C</div>
                        <div class="tech-item">C++</div>
                        <div class="tech-item"><i class="fab fa-java"></i> Java</div>
                        <div class="tech-item"><i class="fab fa-python"></i> Python</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="stats">
        <div class="container">
            <div class="section-title">
                <h2>My Stats</h2>
            </div>
            <div class="stats">
                <div class="stat-card animate">
                    <i class="fas fa-code"></i>
                    <h3>50+</h3>
                    <p>Projects Completed</p>
                </div>
                <div class="stat-card animate delay-1">
                    <i class="fas fa-clock"></i>
                    <h3>1000+</h3>
                    <p>Hours of Coding</p>
                </div>
                <div class="stat-card animate delay-2">
                    <i class="fas fa-users"></i>
                    <h3>10+</h3>
                    <p>Collaborations</p>
                </div>
                <div class="stat-card animate delay-3">
                    <i class="fas fa-certificate"></i>
                    <h3>15+</h3>
                    <p>Certifications</p>
                </div>
            </div>
            
            <div class="github-stats">
                <div class="github-stat animate">
                    <img src="https://github-readme-stats.vercel.app/api?username=sahilbiswas12-sky&show_icons=true&theme=radical" alt="GitHub Stats">
                </div>
                <div class="github-stat animate delay-1">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=sahilbiswas12-sky&layout=compact&theme=radical" alt="Top Languages">
                </div>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="container">
            <div class="section-title">
                <h2>Featured Projects</h2>
            </div>
            <div class="projects">
                <div class="project-card animate">
                    <div class="project-img">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <div class="project-content">
                        <h3>E-Commerce Platform</h3>
                        <p>A full-stack e-commerce solution with React frontend and Node.js backend with MongoDB.</p>
                        <div class="project-tech">
                            <span>React</span>
                            <span>Node.js</span>
                            <span>MongoDB</span>
                            <span>Express</span>
                        </div>
                        <div class="project-links">
                            <a href="#"><i class="fab fa-github"></i> Code</a>
                            <a href="#"><i class="fas fa-external-link-alt"></i> Live Demo</a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card animate delay-1">
                    <div class="project-img">
                        <i class="fas fa-tasks"></i>
                    </div>
                    <div class="project-content">
                        <h3>Task Management App</h3>
                        <p>A productivity app for managing tasks with drag-and-drop functionality and real-time updates.</p>
                        <div class="project-tech">
                            <span>React</span>
                            <span>Firebase</span>
                            <span>Material UI</span>
                        </div>
                        <div class="project-links">
                            <a href="#"><i class="fab fa-github"></i> Code</a>
                            <a href="#"><i class="fas fa-external-link-alt"></i> Live Demo</a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card animate delay-2">
                    <div class="project-img">
                        <i class="fas fa-blog"></i>
                    </div>
                    <div class="project-content">
                        <h3>Developer Blog</h3>
                        <p>A blogging platform for developers to share tutorials and coding experiences.</p>
                        <div class="project-tech">
                            <span>PHP</span>
                            <span>MySQL</span>
                            <span>Bootstrap</span>
                        </div>
                        <div class="project-links">
                            <a href="#"><i class="fab fa-github"></i> Code</a>
                            <a href="#"><i class="fas fa-external-link-alt"></i> Live Demo</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Get In Touch</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item animate">
                        <i class="fas fa-envelope"></i>
                        <div>
                            <h3>Email</h3>
                            <p>sahilbiswas890@gmail.com</p>
                        </div>
                    </div>
                    <div class="contact-item animate delay-1">
                        <i class="fab fa-linkedin"></i>
                        <div>
                            <h3>LinkedIn</h3>
                            <p>linkedin.com/in/sahil-biswas-827337287</p>
                        </div>
                    </div>
                    <div class="contact-item animate delay-2">
                        <i class="fab fa-github"></i>
                        <div>
                            <h3>GitHub</h3>
                            <p>github.com/sahilbiswas12-sky</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form animate delay-3">
                    <form>
                        <input type="text" placeholder="Your Name" required>
                        <input type="email" placeholder="Your Email" required>
                        <input type="text" placeholder="Subject" required>
                        <textarea placeholder="Your Message" required></textarea>
                        <button type="submit" class="btn"><i class="fas fa-paper-plane"></i> Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <p>© 2023 Sahil Biswas. All Rights Reserved.</p>
                <div class="footer-links">
                    <a href="#about">About</a>
                    <a href="#tech-stack">Skills</a>
                    <a href="#projects">Projects</a>
                    <a href="#contact">Contact</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Simple animation on scroll
        document.addEventListener('DOMContentLoaded', function() {
            const animatedElements = document.querySelectorAll('.animate');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = 1;
                    }
                });
            }, {
                threshold: 0.1
            });
            
            animatedElements.forEach(element => {
                element.style.opacity = 0;
                element.style.transition = 'opacity 0.5s ease-in-out';
                observer.observe(element);
            });
        });
    </script>
</body>
</html>
