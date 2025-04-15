<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>YASH GALANDE | Engineering Student</title>
  <!-- Import Google Font Montserrat -->
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700&display=swap" rel="stylesheet">
  <style>
    /* Base Styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Montserrat', sans-serif;
    }
    body {
      /* Indian tricolor gradient background */
      background: linear-gradient(135deg, #FF9933, #FFFFFF, #138808);
      color: #2D2D2D; /* dark text for readability on light section backgrounds */
      line-height: 1.6;
      overflow-x: hidden;
    }
    a {
      text-decoration: none;
      color: inherit;
    }
    /* Navigation */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: rgba(255, 255, 255, 0.85);
      z-index: 1000;
      padding: 1rem 2rem;
      display: flex;
      justify-content: center;
      backdrop-filter: blur(8px);
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }
    nav ul {
      display: flex;
      list-style: none;
    }
    nav ul li {
      margin: 0 1rem;
    }
    nav ul li a {
      color: #2D2D2D;
      font-weight: 500;
      padding: 0.5rem 1rem;
      border-radius: 4px;
      transition: background-color 0.3s ease;
    }
    nav ul li a:hover,
    nav ul li a.active {
      background: linear-gradient(45deg, #FF9933, #138808);
      color: #fff;
    }
    /* Sections */
    section {
      min-height: 100vh;
      padding: 7rem 2rem 2rem;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      /* Use a semi-transparent white background to give each section depth */
      background: rgba(255, 255, 255, 0.9);
      margin: 2rem auto;
      width: 90%;
      max-width: 1200px;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
    }
    section h1 {
      font-size: 2.5rem;
      margin-bottom: 2rem;
      color: #2D2D2D;
      position: relative;
    }
    section h1:after {
      content: '';
      position: absolute;
      bottom: -10px;
      left: 50%;
      transform: translateX(-50%);
      width: 60px;
      height: 4px;
      background: linear-gradient(90deg, #FF9933, #138808);
      border-radius: 2px;
    }
    /* Hero Section */
    #home {
      background: transparent; /* Let the body gradient show for the hero */
    }
    .hero-content {
      max-width: 800px;
    }
    .hero-content h1 {
      font-size: 3rem;
      margin-bottom: 1rem;
      color: #2D2D2D;
    }
    .hero-content h2 {
      font-size: 1.5rem;
      font-weight: 400;
      margin-bottom: 2rem;
      color: #555;
    }
    .hero-content p {
      font-size: 1.1rem;
      margin-bottom: 2rem;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
      color: #333;
    }
    /* About Section */
    #about {
      background: rgba(255, 255, 255, 0.95);
    }
    .about-content {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
      gap: 3rem;
      max-width: 1000px;
      text-align: left;
    }
    .about-text {
      flex: 1;
      min-width: 300px;
    }
    .about-text p {
      margin-bottom: 1.5rem;
      line-height: 1.8;
      color: #2D2D2D;
    }
    .about-image {
      flex: 1;
      min-width: 300px;
      display: flex;
      justify-content: center;
    }
    .profile-img {
      width: 250px;
      height: 250px;
      border-radius: 50%;
      object-fit: cover;
      border: 5px solid #FF9933;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    }
    /* Qualifications Section */
    #qualifications {
      background: rgba(255, 255, 255, 0.95);
    }
    .qualifications-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2rem;
      max-width: 1000px;
    }
    .qualification-card {
      background: #f7f7f7;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      flex: 1;
      min-width: 300px;
      text-align: left;
      transition: transform 0.3s ease, border-color 0.3s ease;
      border: 1px solid transparent;
    }
    .qualification-card:hover {
      transform: translateY(-10px);
      border-color: #FF9933;
    }
    .qualification-card h3 {
      margin-bottom: 1rem;
      color: #2D2D2D;
      font-size: 1.3rem;
    }
    .qualification-card p {
      margin-bottom: 0.5rem;
      color: #555;
    }
    .qualification-card .year {
      font-weight: bold;
      color: #2D2D2D;
    }
    /* Skills Section */
    #skills {
      background: rgba(255, 255, 255, 0.95);
    }
    .skills-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2rem;
      max-width: 1000px;
    }
    .skills-column {
      flex: 1;
      min-width: 300px;
      text-align: left;
    }
    .skills-column h3 {
      margin-bottom: 1.5rem;
      color: #2D2D2D;
      font-size: 1.3rem;
      position: relative;
      padding-bottom: 10px;
    }
    .skills-column h3:after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 50px;
      height: 2px;
      background: linear-gradient(90deg, #FF9933, #138808);
      border-radius: 1px;
    }
    .skill-item {
      margin-bottom: 1.5rem;
    }
    .skill-name {
      display: flex;
      justify-content: space-between;
      margin-bottom: 0.5rem;
      color: #555;
    }
    .skill-bar {
      height: 8px;
      background: #ddd;
      border-radius: 4px;
      overflow: hidden;
    }
    .skill-progress {
      height: 100%;
      background: linear-gradient(90deg, #FF9933, #138808);
      width: 0;
      transition: width 1.5s ease;
    }
    /* Achievements Section */
    #achievements {
      background: rgba(255, 255, 255, 0.95);
    }
    .achievements-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2rem;
      max-width: 1000px;
    }
    .achievement-card {
      background: #f7f7f7;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      flex: 1;
      min-width: 300px;
      text-align: left;
      transition: transform 0.3s ease, border-color 0.3s ease;
      border: 1px solid transparent;
    }
    .achievement-card:hover {
      transform: translateY(-10px);
      border-color: #138808;
    }
    .achievement-card h3 {
      margin-bottom: 1rem;
      color: #2D2D2D;
      font-size: 1.3rem;
    }
    .achievement-card p {
      margin-bottom: 0.5rem;
      color: #555;
    }
    /* Resume Section */
    #resume {
      background: rgba(255, 255, 255, 0.95);
    }
    #resume h1 {
      margin-bottom: 1.5rem;
    }
    .resume-description {
      color: #555;
      max-width: 600px;
      margin-bottom: 1.5rem;
    }
    .resume-button {
      padding: 0.8rem 1.5rem;
      background: linear-gradient(45deg, #FF9933, #138808);
      color: #fff;
      border-radius: 5px;
      font-weight: bold;
      transition: background 0.3s ease;
    }
    .resume-button:hover {
      opacity: 0.9;
    }
    /* Hobbies Section */
    #hobbies {
      background: rgba(255, 255, 255, 0.95);
    }
    .hobbies-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2rem;
    }
    .hobby-card {
      background: #f7f7f7;
      padding: 1.5rem;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      width: 180px;
      text-align: center;
      transition: transform 0.3s ease, border-color 0.3s ease;
      border: 1px solid transparent;
    }
    .hobby-card:hover {
      transform: translateY(-10px);
      border-color: #FF9933;
    }
    .hobby-card i {
      font-size: 2.5rem;
      margin-bottom: 1rem;
      color: #138808;
    }
    .hobby-card h3 {
      color: #2D2D2D;
      font-size: 1.1rem;
    }
    /* Languages Section */
    #languages {
      background: rgba(255, 255, 255, 0.95);
    }
    .languages-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2rem;
    }
    .language-card {
      background: #f7f7f7;
      padding: 1.5rem;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      width: 180px;
      text-align: center;
      transition: transform 0.3s ease, border-color 0.3s ease;
      border: 1px solid transparent;
    }
    .language-card:hover {
      transform: translateY(-10px);
      border-color: #138808;
    }
    .language-card i {
      font-size: 2.5rem;
      margin-bottom: 1rem;
      color: #138808;
    }
    .language-card h3 {
      color: #2D2D2D;
      font-size: 1.1rem;
    }
    .language-card p {
      color: #555;
      font-size: 0.9rem;
    }
    /* Contact Section */
    #contact {
      background: rgba(255, 255, 255, 0.95);
    }
    .contact-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 3rem;
      max-width: 800px;
      text-align: center;
    }
    .contact-info {
      flex: 1;
      min-width: 300px;
    }
    .contact-info h3 {
      margin-bottom: 1.5rem;
      color: #2D2D2D;
      font-size: 1.3rem;
      position: relative;
      padding-bottom: 10px;
    }
    .contact-info h3:after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 50px;
      height: 2px;
      background: linear-gradient(90deg, #FF9933, #138808);
      border-radius: 1px;
    }
    .contact-info p {
      margin-bottom: 1rem;
      color: #555;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .contact-info i {
      margin-right: 10px;
      font-size: 1.2rem;
      color: #138808;
    }
    /* Footer */
    footer {
      background: rgba(0, 0, 0, 0.85);
      color: #fff;
      text-align: center;
      padding: 2rem;
    }
    .social-links {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      margin-bottom: 1rem;
    }
    .social-links a {
      color: #fff;
      font-size: 1.5rem;
      transition: color 0.3s ease;
    }
    .social-links a:hover {
      color: #FF9933;
    }
  </style>
  <script>
    // Smooth scrolling, active link highlighting, and skill bar animation
    document.addEventListener("DOMContentLoaded", function() {
      document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
          e.preventDefault();
          document.querySelector(this.getAttribute('href')).scrollIntoView({
            behavior: 'smooth'
          });
        });
      });
      
      const sections = document.querySelectorAll('section');
      const navLinks = document.querySelectorAll('.nav-link');
      
      window.addEventListener('scroll', () => {
        let current = '';
        sections.forEach(section => {
          const sectionTop = section.offsetTop;
          if (pageYOffset >= (sectionTop - 300)) {
            current = section.getAttribute('id');
          }
        });
        navLinks.forEach(link => {
          link.classList.remove('active');
          if (link.getAttribute('href') === '#' + current) {
            link.classList.add('active');
          }
        });
      });
      
      const skillBars = document.querySelectorAll('.skill-progress');
      function animateSkillBars() {
        skillBars.forEach(bar => {
          const width = bar.getAttribute('data-width');
          if (isElementInViewport(bar)) {
            bar.style.width = width + '%';
          }
        });
      }
      function isElementInViewport(el) {
        const rect = el.getBoundingClientRect();
        return (
          rect.top >= 0 &&
          rect.left >= 0 &&
          rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
          rect.right <= (window.innerWidth || document.documentElement.clientWidth)
        );
      }
      window.addEventListener('load', animateSkillBars);
      window.addEventListener('scroll', animateSkillBars);
    });
  </script>
</head>
<body>
  <!-- Navigation -->
  <nav>
    <ul>
      <li><a href="#home" class="nav-link active">Home</a></li>
      <li><a href="#about" class="nav-link">About</a></li>
      <li><a href="#qualifications" class="nav-link">Qualifications</a></li>
      <li><a href="#skills" class="nav-link">Skills</a></li>
      <li><a href="#achievements" class="nav-link">Achievements</a></li>
      <li><a href="#resume" class="nav-link">Resume</a></li>
      <li><a href="#hobbies" class="nav-link">Hobbies</a></li>
      <li><a href="#languages" class="nav-link">Languages</a></li>
      <li><a href="#contact" class="nav-link">Contact</a></li>
    </ul>
  </nav>

  <!-- Home Section -->
  <section id="home">
    <div class="hero-content">
      <h1>YASH GALANDE</h1>
      <h2>Engineering Student</h2>
      <p>
        I’m a motivated and passionate first-year BTech Computer Science student with a strong interest in technology and innovation. With a solid base in programming, data structures, and problem-solving, I’m eager to gain practical experience through internships or collaborative projects.
      </p>
    </div>
  </section>

  <!-- About Section -->
  <section id="about">
    <h1>About Me</h1>
    <div class="about-content">
      <div class="about-text">
        <p>
          I am a passionate first-year BTech student in Computer Engineering at MIT Academy of Engineering, Alandi, Pune. My journey in technology began with a strong academic foundation, scoring 97% in my 10th boards and 93% in my 12th boards.
        </p>
        <p>
          I am particularly interested in programming and system operations, with foundational skills in C, Python, and Linux OS. In my spare time, I enjoy gaming, watching anime, and cinema.
        </p>
      </div>
      <div class="about-image">
        <img src="C:\Users\yashg\Videos\Captures\WhatsApp Image 2025-04-13 at 16.26.02_090db0cc.jpg" alt="Profile Image" class="profile-img">
      </div>
    </div>
  </section>

  <!-- Qualifications Section -->
  <section id="qualifications">
    <h1>Qualifications</h1>
    <div class="qualifications-container">
      <div class="qualification-card">
        <h3>Education</h3>
        <p class="year">2024 - Present</p>
        <p><strong>Pursuing 1st year B.Tech in Computer Engineering</strong></p>
        <p>MITAOE, Alandi</p>
        <p style="margin-top: 1rem;" class="year">2023 - 2024</p>
        <p><strong>12th Boards: 93%</strong></p>
        <p>R.M.D College</p>
        <p style="margin-top: 1rem;" class="year">2021 - 2022</p>
        <p><strong>10th Boards: 97%</strong></p>
        <p>St. Pius Memorial School</p>
      </div>
      <div class="qualification-card">
        <h3>Strengths</h3>
        <ul style="list-style: none; padding-left: 0;">
          <li style="margin-bottom: 1rem;">• Problem Solving</li>
          <li style="margin-bottom: 1rem;">• Decision Making</li>
          <li style="margin-bottom: 1rem;">• Communication</li>
          <li style="margin-bottom: 1rem;">• Multi-tasking</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- Skills Section -->
  <section id="skills">
    <h1>Skills</h1>
    <div class="skills-container">
      <div class="skills-column">
        <h3>Technical Skills</h3>
        <div class="skill-item">
          <div class="skill-name">
            <span>C Language</span>
            <span>80%</span>
          </div>
          <div class="skill-bar">
            <div class="skill-progress" data-width="80"></div>
          </div>
        </div>
        <div class="skill-item">
          <div class="skill-name">
            <span>C++ Language</span>
            <span>80%</span>
          </div>
          <div class="skill-bar">
            <div class="skill-progress" data-width="80"></div>
          </div>
        </div>
        <div class="skill-item">
          <div class="skill-name">
            <span>Python Language</span>
            <span>55%</span>
          </div>
          <div class="skill-bar">
            <div class="skill-progress" data-width="55"></div>
          </div>
        </div>
        <div class="skill-item">
          <div class="skill-name">
            <span>Linux OS</span>
            <span>40%</span>
          </div>
          <div class="skill-bar">
            <div class="skill-progress" data-width="40"></div>
          </div>
        </div>
      </div>
      <div class="skills-column">
        <h3>Software Skills</h3>
        <div class="skill-item">
          <div class="skill-name">
            <span>Microsoft Word</span>
            <span>70%</span>
          </div>
          <div class="skill-bar">
            <div class="skill-progress" data-width="70"></div>
          </div>
        </div>
        <div class="skill-item">
          <div class="skill-name">
            <span>Microsoft Excel</span>
            <span>65%</span>
          </div>
          <div class="skill-bar">
            <div class="skill-progress" data-width="65"></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Achievements Section -->
  <section id="achievements">
    <h1>Achievements</h1>
    <div class="achievements-container">
      <div class="achievement-card">
        <h3>Academic Excellence</h3>
        <p><span class="year">2022</span></p>
        <p>Scored 97% in 10th board examinations, ranking 1st in school.</p>
        <p><span class="year">2024</span></p>
        <p>Scored 93% in 12th board examinations, ranking in the 94th percentile in JEE Mains.</p>
      </div>
      <div class="achievement-card">
        <h3>Technical Skills</h3>
        <p><span class="year">2024-25</span></p>
        <p>Developed proficiency in C, C++, Python, Linux, and HTML through coursework.</p>
      </div>
      <div class="achievement-card">
        <h3>Future Goals</h3>
        <p><span class="year">Ongoing</span></p>
        <p>Working to master advanced computer engineering concepts and skills.</p>
      </div>
    </div>
  </section>

  <!-- Resume Section -->
  <section id="resume">
    <h1>My Resume & Certifications</h1>
    <p class="resume-description">
      You can view or download my resume and certifications using the buttons below.
    </p>
    <a href="https://jmp.sh/s/1TWFM0KKpmvUkvaSEBOS" target="_blank" rel="noopener" class="resume-button">
      View Certifications
    </a>
    &nbsp;&nbsp;
    <a href="https://postimg.cc/62K1tJ49" target="_blank" rel="noopener" class="resume-button">
      View Resume
    </a>
  </section>

  <!-- Hobbies Section -->
  <section id="hobbies">
    <h1>Hobbies</h1>
    <div class="hobbies-container">
      <div class="hobby-card">
        <i class="fas fa-gamepad"></i>
        <h3>CRICKET</h3>
      </div>
      <div class="hobby-card">
        <i class="fas fa-film"></i>
        <h3>WATCHING ANIME</h3>
      </div>
      <div class="hobby-card">
        <i class="fas fa-video"></i>
        <h3>WATCHING CINEMA</h3>
      </div>
    </div>
  </section>

  <!-- Languages Section -->
  <section id="languages">
    <h1>Languages</h1>
    <div class="languages-container">
      <div class="language-card">
        <i class="fas fa-language"></i>
        <h3>English</h3>
        <p>Professional Proficiency</p>
      </div>
      <div class="language-card">
        <i class="fas fa-language"></i>
        <h3>Hindi</h3>
        <p>Native Proficiency</p>
      </div>
      <div class="language-card">
        <i class="fas fa-language"></i>
        <h3>Marathi</h3>
        <p>Native Proficiency</p>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact">
    <h1>Contact Me</h1>
    <div class="contact-container">
      <div class="contact-info">
        <h3>Get In Touch</h3>
        <p><i class="fas fa-envelope"></i> 202401040179@mitace.ac.in</p>
        <p><i class="fas fa-phone"></i> +91 9028090297</p>
        <p><i class="fas fa-map-marker-alt"></i> Alandi, Pune, Maharashtra</p>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="social-links">
      <a href="#"><i class="fab fa-linkedin"></i></a>
      <a href="#"><i class="fab fa-github"></i></a>
      <a href="#"><i class="fab fa-twitter"></i></a>
    </div>
    <p>&copy; 2024 YASH GALANDE. All rights reserved.</p>
  </footer>
</body>
</html>
