
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Siva Krishna Pinnika | Portfolio</title>

  <style>
    /* GENERAL STYLES */
    :root {
      --bg: #090b14;
      --card: #151a2b;
      --text: #f5f7ff;
      --muted: #a7b0c5;
      --accent: #8b5cf6;
      --cyan: #22d3ee;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
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

    section {
      padding: 80px 0;
    }

    h2 {
      font-size: 2.3rem;
      margin-bottom: 20px;
    }

    .gradient {
      background: linear-gradient(90deg, var(--cyan), var(--accent));
      color: transparent;
      background-clip: text;
      -webkit-background-clip: text;
    }

    .button {
      display: inline-block;
      padding: 12px 22px;
      margin: 10px 8px 0 0;
      border-radius: 30px;
      background: linear-gradient(90deg, var(--cyan), #a78bfa);
      color: #090b14;
      font-weight: bold;
      transition: 0.3s;
    }

    .button:hover {
      transform: translateY(-4px);
      box-shadow: 0 8px 25px #8b5cf655;
    }

    /* NAVIGATION */
    header {
      position: sticky;
      top: 0;
      z-index: 100;
      background: #090b14ee;
      backdrop-filter: blur(12px);
      border-bottom: 1px solid #ffffff18;
    }

    nav {
      min-height: 70px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
    }

    .logo {
      font-size: 1.2rem;
      font-weight: bold;
    }

    nav ul {
      display: flex;
      gap: 20px;
      list-style: none;
    }

    nav ul a {
      color: var(--muted);
    }

    nav ul a:hover {
      color: var(--cyan);
    }

    /* HERO */
    #home {
      min-height: 85vh;
      display: flex;
      align-items: center;
      background:
        radial-gradient(circle at 85% 20%, #8b5cf633, transparent 30%),
        radial-gradient(circle at 10% 80%, #22d3ee18, transparent 30%);
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.4fr 0.6fr;
      align-items: center;
      gap: 40px;
    }

    .hero-label {
      color: var(--cyan);
      letter-spacing: 3px;
      font-size: 0.85rem;
      text-transform: uppercase;
    }

    h1 {
      font-size: clamp(2.6rem, 6vw, 4.5rem);
      line-height: 1.1;
      margin: 20px 0;
    }

    .hero p {
      color: var(--muted);
      font-size: 1.1rem;
      max-width: 650px;
    }

    .profile {
      background: var(--card);
      border: 1px solid #ffffff20;
      padding: 30px;
      border-radius: 25px;
      text-align: center;
      animation: float 4s ease-in-out infinite;
    }

    .avatar {
      width: 110px;
      height: 110px;
      margin: 0 auto 20px;
      border-radius: 30px;
      display: grid;
      place-items: center;
      background: linear-gradient(135deg, var(--accent), var(--cyan));
      color: #090b14;
      font-size: 2.5rem;
      font-weight: bold;
    }

    .profile p {
      font-size: 0.95rem;
      margin-top: 8px;
    }

    /* ABOUT */
    .description {
      max-width: 750px;
      color: var(--muted);
      font-size: 1.08rem;
    }

    /* SKILLS */
    .grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      margin-top: 30px;
    }

    .card {
      padding: 25px;
      background: var(--card);
      border: 1px solid #ffffff15;
      border-radius: 18px;
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-7px);
      border-color: var(--cyan);
    }

    .card h3 {
      margin-bottom: 10px;
    }

    .card p {
      color: var(--muted);
    }

    .skill-icon {
      color: var(--cyan);
      font-size: 1.5rem;
      font-weight: bold;
      margin-bottom: 10px;
    }

    /* PROJECTS */
    .project-tags {
      margin-top: 15px;
    }

    .tag {
      display: inline-block;
      border: 1px solid #ffffff25;
      padding: 5px 10px;
      margin: 4px 3px 0 0;
      border-radius: 20px;
      color: var(--cyan);
      font-size: 0.8rem;
    }

    /* EDUCATION AND CONTACT */
    .info-box {
      background: var(--card);
      border-left: 4px solid var(--accent);
      border-radius: 12px;
      padding: 25px;
      margin-top: 20px;
    }

    .info-box p {
      color: var(--muted);
    }

    #contact {
      text-align: center;
      background: linear-gradient(180deg, transparent, #8b5cf615);
    }

    footer {
      text-align: center;
      color: var(--muted);
      border-top: 1px solid #ffffff15;
      padding: 25px;
    }

    /* ANIMATIONS */
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    .reveal {
      opacity: 0;
      transform: translateY(25px);
      transition: opacity 0.7s, transform 0.7s;
    }

    .reveal.show {
      opacity: 1;
      transform: translateY(0);
    }

    /* MOBILE RESPONSIVE DESIGN */
    @media (max-width: 750px) {
      nav {
        align-items: flex-start;
        padding: 18px 0;
        flex-direction: column;
      }

      nav ul {
        flex-wrap: wrap;
        gap: 12px;
      }

      .hero-grid {
        grid-template-columns: 1fr;
      }

      .grid {
        grid-template-columns: repeat(2, 1fr);
      }

      #home {
        padding: 60px 0;
      }
    }

    @media (max-width: 480px) {
      .grid {
        grid-template-columns: 1fr;
      }

      section {
        padding: 60px 0;
      }

      h2 {
        font-size: 1.9rem;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->
  <header>
    <nav class="container">
      <a class="logo" href="#home">SK<span class="gradient">.</span> Portfolio</a>

      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#education">Education</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- HERO SECTION -->
  <section id="home" class="hero">
    <div class="container hero-grid">
      <div class="reveal">
        <span class="hero-label">AI • Data Science • Analytics</span>

        <h1>
          Hi, I'm<br>
          <span class="gradient">Siva Krishna Pinnika</span>
        </h1>

        <p>
          An Artificial Intelligence and Data Science student passionate
          about Python, data analytics, visualization, and building
          practical technology projects.
        </p>

        <a href="#projects" class="button">Explore Projects ↗</a>
        <a href="#contact" class="button">Contact Me</a>
      </div>

      <div class="profile reveal">
        <div class="avatar">SK</div>
        <h3>AI & Data Science</h3>
        <p>Student | Aspiring Data Analyst</p>
        <p>Interested in AI, analytics, and problem-solving.</p>
      </div>
    </div>
  </section>

  <!-- ABOUT SECTION -->
  <section id="about">
    <div class="container reveal">
      <span class="hero-label">About Me</span>
      <h2>Curious about data. <span class="gradient">Ready to learn.</span></h2>

      <p class="description">
        I am pursuing Artificial Intelligence and Data Science at
        Annamacharya University. I enjoy learning programming, exploring
        datasets, creating visualizations, and developing projects that
        solve practical problems. I am looking for internship opportunities
        where I can improve my skills and contribute to a team.
      </p>
    </div>
  </section>

  <!-- SKILLS SECTION -->
  <section id="skills">
    <div class="container reveal">
      <span class="hero-label">My Technical Skills</span>
      <h2>Skills & <span class="gradient">Tools</span></h2>

      <div class="grid">
        <div class="card">
          <div class="skill-icon">Py</div>
          <h3>Python</h3>
          <p>Programming and data analysis.</p>
        </div>

        <div class="card">
          <div class="skill-icon">Pd</div>
          <h3>Pandas</h3>
          <p>Data cleaning and manipulation.</p>
        </div>

        <div class="card">
          <div class="skill-icon">Np</div>
          <h3>NumPy</h3>
          <p>Numerical computing and arrays.</p>
        </div>

        <div class="card">
          <div class="skill-icon">BI</div>
          <h3>Power BI</h3>
          <p>Interactive dashboards and charts.</p>
        </div>

        <div class="card">
          <div class="skill-icon">Tb</div>
          <h3>Tableau</h3>
          <p>Data visualization and reporting.</p>
        </div>

        <div class="card">
          <div class="skill-icon">SQL</div>
          <h3>SQL</h3>
          <p>Database queries and data retrieval.</p>
        </div>

        <div class="card">
          <div class="skill-icon">Ja</div>
          <h3>Java</h3>
          <p>Programming fundamentals.</p>
        </div>

        <div class="card">
          <div class="skill-icon">C</div>
          <h3>C Programming</h3>
          <p>Logic and programming basics.</p>
        </div>

        <div class="card">
          <div class="skill-icon">&lt;/&gt;</div>
          <h3>HTML</h3>
          <p>Web page structure and layout.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- PROJECTS SECTION -->
  <section id="projects">
    <div class="container reveal">
      <span class="hero-label">My Work</span>
      <h2>Featured <span class="gradient">Projects</span></h2>

      <div class="grid">
        <div class="card">
          <div class="skill-icon">🛡️</div>
          <h3>Fraud Message Detection</h3>
          <p>
            A project designed to classify messages as potentially fraudulent
            or legitimate to help identify suspicious communications.
          </p>
          <div class="project-tags">
            <span class="tag">Python</span>
            <span class="tag">Data Analysis</span>
            <span class="tag">Classification</span>
          </div>
        </div>

        <div class="card">
          <div class="skill-icon">📊</div>
          <h3>Airline Flight and Price Analytics Dashboard</h3>
          <p>
            An analytics project exploring flight information and airfare
            patterns using data processing and visualization.
          </p>
          <div class="project-tags">
            <span class="tag">Pandas</span>
            <span class="tag">NumPy</span>
            <span class="tag">Power BI / Tableau</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- EDUCATION SECTION -->
  <section id="education">
    <div class="container reveal">
      <span class="hero-label">My Background</span>
      <h2><span class="gradient">Education</span></h2>

      <div class="info-box">
        <h3>Annamacharya University</h3>
        <p>Degree: Artificial Intelligence and Data Science</p>
        <p>Expected graduation: Add your year</p>
      </div>
    </div>
  </section>

  <!-- CONTACT SECTION -->
  <section id="contact">
    <div class="container reveal">
      <span class="hero-label">Get In Touch</span>
      <h2>Let's <span class="gradient">Connect</span></h2>

      <p class="description" style="margin: 0 auto;">
        I am interested in internships, learning opportunities, and
        collaborations on technology and data projects.
      </p>

      <a
        href="mailto:pininikasivakrishna123@gmail.com"
        class="button"
      >
        Email Me ↗
      </a>

      <!-- Replace the URL with your personal GitHub profile -->
      <a
        href="https://github.com/"
        target="_blank"
        rel="noopener noreferrer"
        class="button"
      >
        GitHub ↗
      </a>
    </div>
  </section>

  <footer>
    <p>© <span id="year"></span> Siva Krishna Pinnika | Built with HTML, CSS & JavaScript</p>
  </footer>

  <script>
    // Automatically show the current year
    document.getElementById("year").textContent =
      new Date().getFullYear();

    // Reveal elements when they enter the screen
    const revealElements = document.querySelectorAll(".reveal");

    if ("IntersectionObserver" in window) {
      const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add("show");
            observer.unobserve(entry.target);
          }
        });
      }, { threshold: 0.15 });

      revealElements.forEach((element) => {
        observer.observe(element);
      });
    } else {
      revealElements.forEach((element) => {
        element.classList.add("show");
      });
    }
  </script>

</body>
</html>
