
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name | Portfolio</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        :root {
            --bg: #0b1120;
            --card: #111c30;
            --blue: #38bdf8;
            --white: #f1f5f9;
            --gray: #94a3b8;
            --border: #263449;
        }

        body {
            font-family: Arial, sans-serif;
            background: var(--bg);
            color: var(--white);
            line-height: 1.7;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        .container {
            width: 90%;
            max-width: 1100px;
            margin: auto;
        }

        /* Navigation */
        header {
            border-bottom: 1px solid var(--border);
            position: sticky;
            top: 0;
            background: #0b1120;
            z-index: 10;
        }

        nav {
            min-height: 75px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .logo {
            font-size: 25px;
            font-weight: bold;
        }

        .logo span,
        .hero h1 span {
            color: var(--blue);
        }

        nav ul {
            display: flex;
            gap: 22px;
            list-style: none;
            flex-wrap: wrap;
        }

        nav ul a {
            color: var(--gray);
            transition: 0.3s;
        }

        nav ul a:hover {
            color: var(--blue);
        }

        /* Hero */
        .hero {
            min-height: 85vh;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 45px;
            padding-top: 60px;
            padding-bottom: 60px;
        }

        .hero-text {
            max-width: 620px;
        }

        .subtitle {
            color: var(--blue);
            letter-spacing: 3px;
            font-size: 13px;
            font-weight: bold;
        }

        .hero h1 {
            font-size: clamp(38px, 6vw, 62px);
            line-height: 1.2;
            margin: 15px 0;
        }

        .hero h2 {
            font-size: 25px;
            color: var(--gray);
            margin-bottom: 20px;
        }

        .hero p,
        .section-description {
            color: var(--gray);
        }

        .buttons {
            display: flex;
            gap: 15px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            background: var(--blue);
            color: #07111f;
            padding: 11px 22px;
            border-radius: 7px;
            font-weight: bold;
            transition: 0.3s;
        }

        .btn:hover {
            transform: translateY(-3px);
        }

        .btn-outline {
            background: transparent;
            color: var(--white);
            border: 1px solid var(--border);
        }

        .profile-card {
            min-width: 260px;
            text-align: center;
            padding: 35px 25px;
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: 18px;
        }

        .avatar {
            width: 120px;
            height: 120px;
            margin: 0 auto 20px;
            display: grid;
            place-items: center;
            border-radius: 50%;
            background: linear-gradient(135deg, #38bdf8, #818cf8);
            color: #07111f;
            font-size: 38px;
            font-weight: bold;
        }

        .profile-card p {
            font-size: 14px;
            color: var(--gray);
        }

        .available {
            margin-top: 15px;
            color: #4ade80;
            font-size: 12px;
        }

        /* General sections */
        section:not(.hero) {
            padding-top: 80px;
            padding-bottom: 80px;
        }

        .section-title {
            font-size: 35px;
            margin: 8px 0 25px;
        }

        .section-description {
            max-width: 750px;
        }

        /* Skills */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 18px;
            margin-top: 30px;
        }

        .skill {
            padding: 25px 18px;
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: 12px;
            transition: 0.3s;
        }

        .skill:hover,
        .project:hover {
            border-color: var(--blue);
            transform: translateY(-5px);
        }

        .skill h3 {
            color: var(--blue);
            margin-bottom: 8px;
        }

        .skill p {
            font-size: 14px;
            color: var(--gray);
        }

        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 22px;
            margin-top: 30px;
        }

        .project {
            padding: 25px;
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: 12px;
            transition: 0.3s;
        }

        .project .number {
            color: var(--blue);
            font-size: 12px;
            letter-spacing: 2px;
        }

        .project h3 {
            margin: 12px 0;
        }

        .project p {
            color: var(--gray);
            font-size: 14px;
        }

        .tags {
            display: flex;
            gap: 8px;
            margin: 20px 0;
            flex-wrap: wrap;
        }

        .tags span {
            color: var(--blue);
            background: #123047;
            border-radius: 5px;
            padding: 4px 9px;
            font-size: 12px;
        }

        .project-link {
            color: var(--blue);
            font-weight: bold;
        }

        /* Contact */
        .contact {
            text-align: center;
        }

        .contact .section-description {
            margin: auto;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
            margin-top: 25px;
        }

        .contact-links a {
            border: 1px solid var(--border);
            border-radius: 7px;
            padding: 10px 20px;
            transition: 0.3s;
        }

        .contact-links a:hover {
            color: var(--blue);
            border-color: var(--blue);
        }

        /* Footer */
        footer {
            border-top: 1px solid var(--border);
            padding: 25px;
            text-align: center;
            color: var(--gray);
            font-size: 13px;
        }

        /* Mobile responsive */
        @media (max-width: 800px) {
            nav {
                justify-content: center;
                padding: 15px 0;
            }

            nav ul {
                justify-content: center;
                gap: 12px 18px;
            }

            .hero {
                flex-direction: column;
                align-items: flex-start;
                min-height: auto;
            }

            .profile-card {
                width: 100%;
            }

            .skills-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .projects-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 500px) {
            .skills-grid,
            .projects-grid {
                grid-template-columns: 1fr;
            }

            .hero h1 {
                font-size: 39px;
            }

            .section-title {
                font-size: 29px;
            }

            section:not(.hero) {
                padding-top: 55px;
                padding-bottom: 55px;
            }
        }
    </style>
</head>

<body>

    <header>
        <nav class="container">
            <a href="#home" class="logo">MyPortfolio<span>.</span></a>

            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="hero container" id="home">
            <div class="hero-text">
                <div class="subtitle">WELCOME TO MY PORTFOLIO</div>

                <h1>Hi, I'm <span>Your Name</span></h1>

                <h2>Frontend Developer</h2>

                <p>
                    I'm a passionate web developer who enjoys
                    creating modern, responsive, and user-friendly
                    websites using HTML and CSS. I love learning
                    new skills and turning ideas into reality.
                </p>

                <div class="buttons">
                    <a href="#projects" class="btn">View My Projects</a>
                    <a href="#contact" class="btn btn-outline">
                        Contact Me
                    </a>
                </div>
            </div>

            <div class="profile-card">
                <div class="avatar">YN</div>
                <h2>Your Name</h2>
                <p>Web Developer | Creative Thinker</p>
                <div class="available">● Open to opportunities</div>
            </div>
        </section>

        <section id="about">
            <div class="container">
                <div class="subtitle">GET TO KNOW ME</div>
                <h2 class="section-title">About Me</h2>

                <p class="section-description">
                    Hello! I'm an aspiring frontend developer with
                    an interest in web design and technology.
                    I enjoy building attractive websites, solving
                    problems, and improving my coding skills.
                    My current focus is HTML and CSS, responsive
                    layouts, and creating projects that showcase
                    my creativity and knowledge.
                </p>
            </div>
        </section>

        <section id="skills">
            <div class="container">
                <div class="subtitle">WHAT I KNOW</div>
                <h2 class="section-title">My Skills</h2>

                <div class="skills-grid">
                    <div class="skill">
                        <h3>HTML5</h3>
                        <p>Building structured and accessible webpages.</p>
                    </div>

                    <div class="skill">
                        <h3>CSS3</h3>
                        <p>Creating beautiful layouts and styling.</p>
                    </div>

                    <div class="skill">
                        <h3>Responsive Design</h3>
                        <p>Designing for mobile, tablet, and desktop.</p>
                    </div>

                    <div class="skill">
                        <h3>GitHub</h3>
                        <p>Sharing projects and managing repositories.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="projects">
            <div class="container">
                <div class="subtitle">MY RECENT WORK</div>
                <h2 class="section-title">Featured Projects</h2>

                <div class="projects-grid">
                    <article class="project">
                        <div class="number">PROJECT 01</div>
                        <h3>Personal Portfolio</h3>
                        <p>
                            A personal website to introduce myself
                            and showcase my skills and projects.
                        </p>

                        <div class="tags">
                            <span>HTML</span>
                            <span>CSS</span>
                        </div>

                        <a class="project-link"
                           href="https://github.com/YOUR-USERNAME/YOUR-REPO">
                            View Project →
                        </a>
                    </article>

                    <article class="project">
                        <div class="number">PROJECT 02</div>
                        <h3>Landing Page</h3>
                        <p>
                            A modern landing page with clean design,
                            responsive layouts, and attractive styling.
                        </p>

                        <div class="tags">
                            <span>HTML</span>
                            <span>CSS</span>
                        </div>

                        <a class="project-link"
                           href="https://github.com/YOUR-USERNAME/YOUR-REPO">
                            View Project →
                        </a>
                    </article>

                    <article class="project">
                        <div class="number">PROJECT 03</div>
                        <h3>Login Page UI</h3>
                        <p>
                            A simple login page interface featuring
                            styled inputs and a clean layout.
                        </p>

                        <div class="tags">
                            <span>HTML</span>
                            <span>CSS</span>
                        </div>

                        <a class="project-link"
                           href="https://github.com/YOUR-USERNAME/YOUR-REPO">
                            View Project →
                        </a>
                    </article>
                </div>
            </div>
        </section>

        <section id="contact" class="contact">
            <div class="container">
                <div class="subtitle">LET'S CONNECT</div>
                <h2 class="section-title">Contact Me</h2>

                <p class="section-description">
                    I'm always interested in learning, collaborating,
                    and exploring new opportunities. Feel free to
                    reach out!
                </p>

                <div class="contact-links">
                    <a href="mailto:your-email@example.com">Email Me</a>

                    <a href="https://github.com/YOUR-USERNAME"
                       target="_blank" rel="noopener noreferrer">
                        GitHub
                    </a>

                    <a href="https://www.linkedin.com/in/YOUR-USERNAME"
                       target="_blank" rel="noopener noreferrer">
                        LinkedIn
                    </a>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>© 2026 Your Name | Built with HTML & CSS</p>
    </footer>

</body>
</html>
