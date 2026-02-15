# FUTURE_FS_01
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ragul personal-Professional Portfolio</title>
    <meta name="description" content="Professional portfolio showcasing web development skills, projects, and experience">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: hsla(0, 93%, 6%, 0.959);
            scroll-behavior: smooth;
        }
        header {
            position: fixed;
            width: 100%;
            background: rgba(255, 249, 249, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #110f0b;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #2563eb;
        }
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding: 0 2rem;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.2s both;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .btn {
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
            cursor: pointer;
        }

        .btn-primary {
            background: white;
            color: #2563eb;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(255,255,255,0.3);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid white;
        }

        .btn-secondary:hover {
            background: white;
            color: #2563eb;
        }
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            color: #2563eb;
        }
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 3rem;
            align-items: center;
        }

        .about-image {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            height: 400px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: #2563eb;
        }
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-10px);
        }

        .skill-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .project-card:hover {
            transform: translateY(-10px);
        }

        .project-image {
            height: 200px;
            background: linear-gradient(45deg, #2563eb, #1e40af);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
        }

        .project-content {
            padding: 1.5rem;
        }
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .contact-info h3 {
            color: #2563eb;
            margin-bottom: 1rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
        }

        .contact-item svg {
            width: 24px;
            height: 24px;
            margin-right: 1rem;
            color: #af9395;
        }

        .contact-form {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: 2px solid #e5e7eb;
            border-radius: 10px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #2563eb;
        }
        footer {
            background: #1f2937;
            color: white;
            text-align: center;
            padding: 2rem;
        }
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .about-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            section {
                padding: 3rem 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">Login</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Hi, I'm <span style="color: #ffd700;">Ragul</span></h1>
            <p>Full Stack Developer & UI/UX Designer creating amazing digital experiences</p>
            <div class="cta-buttons">
                <a href="#projects" class="btn btn-primary">View My Work</a>
                <a href="#contact" class="btn btn-secondary">Get In Touch</a>
            </div>
        </div>
    </section>
    <section id="about" class="about">
        <h2>About Me</h2>
        <div class="about-grid">
            <div class="about-image">👨‍💻</div>
            <div>
                <h3>Passionate Developer with 3+ Years Experience</h3>
                <p>I specialize in creating responsive web applications using modern technologies like React, Node.js, and Tailwind CSS. I love turning complex problems into simple, beautiful solutions.</p>
                <p>Currently based in Coimbatore, I'm always looking for exciting new opportunities to build innovative projects and collaborate with amazing teams.</p>
            </div>
        </div>
    </section>
    <section id="skills" class="skills">
        <h2>Skills & Technologies</h2>
        <div class="skills-grid">
            <div class="skill-card">
                <div class="skill-icon">⚛️</div>
                <h3>React.js</h3>
                <p>Modern UI development with React, Next.js & state management</p>
            </div>
            <div class="skill-card">
                <div class="skill-icon">🔗</div>
                <h3>Node.js</h3>
                <p>Backend development & RESTful APIs</p>
            </div>
            <div class="skill-card">
                <div class="skill-icon">💾</div>
                <h3>MongoDB</h3>
                <p>NoSQL database design & optimization</p>
            </div>
            <div class="skill-card">
                <div class="skill-icon">🎨</div>
                <h3>Tailwind CSS</h3>
                <p>Rapid, responsive UI development</p>
            </div>
        </div>
    </section>
    <section id="projects" class="projects">
        <h2>Featured Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-image">E-Commerce Platform</div>
                <div class="project-content">
                    <h3>ShopSphere</h3>
                    <p>Full-stack e-commerce solution with React, Node.js & MongoDB. Features payment integration and admin dashboard.</p>
                    <div style="margin-top: 1rem;">
                        <span class="btn" style="padding: 0.5rem 1rem; font-size: 0.9rem; margin-right: 0.5rem;">Live Demo</span>
                        <span class="btn" style="padding: 0.5rem 1rem; font-size: 0.9rem; background: #10b981; color: white;">GitHub</span>
                    </div>
                </div>
            </div>
            <div class="project-card">
                <div class="project-image">Task Management App</div>
                <div class="project-content">
                    <h3>TaskMaster</h3>
                    <p>Real-time collaborative task management app built with React and Socket.io. Drag & drop interface.</p>
                    <div style="margin-top: 1rem;">
                        <span class="btn" style="padding: 0.5rem 1rem; font-size: 0.9rem;">Live Demo</span>
                        <span class="btn" style="padding: 0.5rem 1rem; font-size: 0.9rem; background: #10b981; color: white;">GitHub</span>
                    </div>
                </div>
            </div>
            <div class="project-card">
                <div class="project-image">Portfolio Website</div>
                <div class="project-content">
                    <h3>This Portfolio</h3>
                    <p>Fully responsive portfolio website built with HTML5, CSS3 and vanilla JavaScript. SEO optimized.</p>
                    <div style="margin-top: 1rem;">
                        <span class="btn" style="padding: 0.5rem 1rem; font-size: 0.9rem; margin-right: 0.5rem;">Live Demo</span>
                        <span class="btn" style="padding: 0.5rem 1rem; font-size: 0.9rem; background: #10b981; color: white;">Source Code</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section id="contact" class="contact">
        <h2>Let's Work Together</h2>
        <div class="contact-grid">
            <div class="contact-info">
                <h3>Get In Touch</h3>
                <div class="contact-item">
                    <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 4.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
                    <span>hello@yourname.com</span>
                </div>
                <div class="contact-item">
                    <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path></svg>
                    <span>+91 98765 43210</span>
                </div>
                <div class="contact-item">
                    <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>
                    <span>Coimbatore, Tamil Nadu</span>
                </div>
            </div>
                <img src="C:\Users\ELCOT\Downloads\pxfuel.jpg"  height="360" width="444"
            <form class="contact-form" onsubmit="handleSubmit(event)">
                <div class="form-group">
                    <input type="text" placeholder="Your Name" required>
                </div>
                <div class="form-group">
                    <input type="email" placeholder="Your Email" required>
                </div>
                <div class="form-group">
                    <input type="text" placeholder="Subject" required>
                </div>
                <div class="form-group">
                    <textarea rows="5" placeholder="Your Message" required></textarea>
                </div>
                <button type="submit" class="btn btn-primary" style="width: 100%;">Send Message</button>
            </form>
        </div>
    </section>
    <footer>
        <p>&copy; 2026 Ragul. All rights reserved. | Made with ❤️ in Coimbatore</p>
    </footer>
    <script>
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
        function handleSubmit(event) {
            event.preventDefault();
            alert('Thank you for your message! I\'ll get back to you soon.');
            event.target.reset();
        }
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(255, 255, 255, 0.98)';
            } else {
                header.style.background = 'rgba(255, 255, 255, 0.95)';
            }
        });
    </script>
</body>
<body style="background-color: rgb(118, 214, 169);"></body>
</body>
</html>
