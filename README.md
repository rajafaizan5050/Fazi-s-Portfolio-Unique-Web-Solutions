<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fazi's Portfolio | Unique Web Solutions</title>

  <style>
    /* Basic Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    /* Body */
    body {
      font-family: 'Roboto', sans-serif;
      background: #141414;
      color: white;
      line-height: 1.6;
    }

    /* Custom Cursor */
    body {
      cursor: url('https://www.google.com/intl/en/chrome/browser/feature/images/cursors/arrow.cur'), auto;
    }

    /* Fullscreen Background */
    .background {
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      background: url('https://images.unsplash.com/photo-1556740749-887f6717d7e4') center/cover no-repeat;
      filter: brightness(50%);
      z-index: -1;
    }

    /* Navbar */
    nav {
      position: sticky;
      top: 0;
      background-color: #141414;
      padding: 20px;
      z-index: 1000;
      border-bottom: 1px solid #444;
    }

    nav ul {
      list-style: none;
      display: flex;
      justify-content: center;
    }

    nav ul li {
      margin: 0 20px;
    }

    nav ul li a {
      color: white;
      text-decoration: none;
      font-size: 1.2rem;
      letter-spacing: 1px;
      text-transform: uppercase;
      transition: color 0.3s;
    }

    nav ul li a:hover {
      color: #ff6f61;
    }

    /* Hero Section */
    .hero {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      text-align: center;
      z-index: 1;
      position: relative;
    }

    .hero h1 {
      font-size: 4rem;
      letter-spacing: 3px;
      font-weight: bold;
      animation: fadeIn 2s ease-in-out;
    }

    .hero p {
      font-size: 1.3rem;
      color: #ddd;
      margin-top: 20px;
      animation: fadeIn 2s ease-in-out 1s;
    }

    .hero a {
      background-color: #ff6f61;
      padding: 12px 30px;
      border-radius: 30px;
      color: white;
      font-size: 1.5rem;
      text-decoration: none;
      margin-top: 20px;
      display: inline-block;
      letter-spacing: 1px;
      transition: transform 0.3s ease;
    }

    .hero a:hover {
      transform: scale(1.1);
    }

    /* About Section */
    .about {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 100px 50px;
      background-color: #1f1f1f;
    }

    .about h2 {
      font-size: 3rem;
      color: #ff6f61;
      margin-bottom: 20px;
    }

    .about .text {
      font-size: 1.2rem;
      max-width: 600px;
      color: #bbb;
    }

    .about img {
      border-radius: 10px;
      width: 40%;
      height: auto;
      transition: transform 0.5s ease-in-out;
    }

    .about img:hover {
      transform: scale(1.1);
    }

    /* Services Section */
    .services {
      padding: 100px 50px;
      text-align: center;
      background-color: #222;
    }

    .services h2 {
      font-size: 3.5rem;
      color: #ff6f61;
      margin-bottom: 40px;
    }

    .services .service-card {
      display: inline-block;
      width: 30%;
      background-color: #333;
      padding: 30px;
      margin: 10px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
      color: white;
      transition: transform 0.3s ease-in-out;
    }

    .services .service-card:hover {
      transform: translateY(-10px);
    }

    .services .service-card h3 {
      font-size: 1.8rem;
      color: #ff6f61;
      margin-bottom: 10px;
    }

    .services .service-card p {
      font-size: 1rem;
      color: #bbb;
    }

    /* Projects Section */
    .projects {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-gap: 30px;
      padding: 100px 50px;
      background-color: #141414;
    }

    .projects .project-card {
      background-color: #222;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
      transition: transform 0.3s ease;
    }

    .projects .project-card:hover {
      transform: scale(1.05);
    }

    .projects img {
      width: 100%;
      border-radius: 10px;
    }

    .projects h3 {
      color: #ff6f61;
      font-size: 1.6rem;
      margin-top: 20px;
    }

    .projects p {
      color: #bbb;
      font-size: 1rem;
    }

    /* Contact Section */
    .contact {
      padding: 80px 50px;
      text-align: center;
      background-color: #ff6f61;
    }

    .contact h2 {
      font-size: 3.5rem;
      color: white;
      margin-bottom: 30px;
    }

    .contact form {
      max-width: 600px;
      margin: 0 auto;
    }

    .contact input,
    .contact textarea {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border-radius: 5px;
      border: 1px solid #ddd;
      background-color: #333;
      color: white;
      font-size: 1rem;
    }

    .contact button {
      background-color: #222;
      color: white;
      padding: 12px 30px;
      border-radius: 30px;
      cursor: pointer;
      transition: background-color 0.3s ease;
      border: none;
    }

    .contact button:hover {
      background-color: #555;
    }

    /* Footer Section */
    footer {
      background-color: #141414;
      color: white;
      text-align: center;
      padding: 20px;
    }

    /* Scroll Animations */
    @keyframes fadeIn {
      0% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }

    @media screen and (max-width: 768px) {
      .about {
        flex-direction: column;
        text-align: center;
      }

      .about img {
        width: 80%;
        margin-top: 20px;
      }

      .projects {
        grid-template-columns: 1fr;
      }

      .services .service-card {
        width: 80%;
        margin: 20px auto;
      }
    }
  </style>
</head>

<body>
  <!-- Navbar Section -->
  <nav>
    <ul>
      <li><a href="#hero">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#portfolio">Portfolio</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- Background -->
  <div class="background"></div>

  <!-- Hero Section -->
  <section class="hero" id="hero">
    <h1>Hi, I'm Fazi</h1>
    <p>Based in [Pakistan], crafting digital solutions with precision and passion.</p>
    <a href="#about">Learn More</a>
  </section>

  <!-- About Section -->
  <section class="about" id="about">
    <div>
      <h2>About Me</h2>
      <p class="text">
        I am a passionate web developer specializing in crafting beautiful, functional websites. My goal is to help you bring your vision to life through innovative digital solutions.
      </p>
    </div>
    <img src="my pic/e1dd2689-2a7f-4119-8b5e-d8b8d6c58fbe.webp" alt="Fazi"/>
  </section>

  <!-- Services Section -->
  <section class="services" id="services">
    <h2>What I Do</h2>
    <div class="service-card">
      <h3>Web Development</h3>
      <p>Crafting responsive, user-friendly websites that deliver results.</p>
    </div>
    <div class="service-card">
      <h3>SEO Optimization</h3>
      <p>Helping your site rank higher and get noticed by the right audience.</p>
    </div>
    <div class="service-card">
      <h3>Custom Solutions</h3>
      <p>Tailored web solutions designed to meet your specific needs.</p>
    </div>
  </section>

  <!-- Projects Section -->
  <section class="projects" id="portfolio">
    <h2>My Work</h2>
    <div class="project-card">
      <img src="http://127.0.0.1:3000/my-project.html" alt="Project 1" />
      <h3>Project 1</h3>
      <p>A brief description of the project.</p>
    </div>
    <div class="project-card">
      <img src="http://127.0.0.1:3000/homepage.html" alt="Project 2" />
      <h3>Project 2</h3>
      <p>A brief description of the project.</p>
    </div>
    <div class="project-card">
      <img src="project3.jpg" alt="Project 3" />
      <h3>Project 3</h3>
      <p>A brief description of the project.</p>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="contact" id="contact">
    <h2>Contact Me</h2>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <!-- Footer Section -->
  <footer>
    <p>&copy; 2025 Fazi's Portfolio | All Rights Reserved</p>
  </footer>

  <!-- Scroll Animation JavaScript -->
  <script>
    document.addEventListener("scroll", function () {
      if (window.scrollY > 100) {
        document.body.style.backgroundColor = "#222";
      } else {
        document.body.style.backgroundColor = "#141414";
      }
    });
  </script>
</body>
</html>
