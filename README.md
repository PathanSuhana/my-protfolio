# my-protfolio
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Suhana Pathan </title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg: #0f0f1a;
      --card: #16162a;
      --accent: #8b5cf6;
      --accent2: #22d3ee;
      --text: #e5e7eb;
      --muted: #9ca3af;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background: radial-gradient(circle at top, #1a1a2e, var(--bg));
      color: var(--text);
      overflow-x: hidden;
    }

    /* ===== NAV ===== */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(15, 15, 26, 0.85);
      backdrop-filter: blur(10px);
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 60px;
      z-index: 1000;
    }

    nav h2 {
      color: var(--accent);
      font-weight: 700;
    }

    nav ul {
      display: flex;
      gap: 25px;
      list-style: none;
    }

    nav ul li a {
      text-decoration: none;
      color: var(--text);
      font-size: 0.95rem;
      transition: color 0.3s;
    }

    nav ul li a:hover {
      color: var(--accent2);
    }

    /* ===== HERO ===== */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 120px 80px 40px;
      gap: 50px;
    }

    .hero-text {
      max-width: 600px;
      animation: fadeUp 1.2s ease forwards;
    }

    .hero-text h1 {
      font-size: 3.2rem;
      line-height: 1.2;
    }

    .hero-text span {

  background: linear-gradient(90deg, var(--accent), var(--accent2));
  background-clip: text;              /* standard */
  -webkit-background-clip: text;      /* Chrome, Safari */
  -webkit-text-fill-color: transparent;
}

    

    .hero-text p {
      margin: 20px 0 30px;
      color: var(--muted);
      font-size: 1.05rem;
    }

    .btn {
      padding: 12px 28px;
      border-radius: 30px;
      border: none;
      background: linear-gradient(90deg, var(--accent), var(--accent2));
      color: #000;
      font-weight: 600;
      cursor: pointer;
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .btn:hover {
      transform: translateY(-4px);
      box-shadow: 0 10px 30px rgba(139, 92, 246, 0.4);
    }

    .hero-img {
     
  position: relative;
  animation: float 4s ease-in-out infinite;
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero-img img {
  width: 400px; /* bigger image */
  height: 400px; /* make it square for perfect circle */
  border-radius: 50%; /* circular image */
  object-fit: cover;
  border: 6px solid var(--accent2); /* glowing border */
  box-shadow: 0 25px 60px rgba(0,0,0,0.6);
  transition: transform 0.5s;
}

.hero-img img:hover {
  transform: scale(1.05) rotate(3deg); /* subtle hover animation */
}
.hero-img img {
  box-shadow: 0 0 30px var(--accent2), 0 25px 60px rgba(0,0,0,0.6);
}

/* Float animation (already exists) */
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-20px); } /* slightly higher float */
}


    

    /* ===== SECTIONS ===== */
    section {
      padding: 100px 80px;
    }

    section h2 {
      text-align: center;
      font-size: 2.4rem;
      margin-bottom: 50px;
      color: var(--accent);
    }

    /* ===== ABOUT ===== */
    .about {
      max-width: 900px;
      margin: auto;
      text-align: center;
      color: var(--muted);
      line-height: 1.8;
      animation: fadeUp 1s ease forwards;
    }

    /* ===== SKILLS ===== */
    .skills {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 25px;
    }

    .skill-card {
      background: var(--card);
      padding: 30px;
      border-radius: 18px;
      text-align: center;
      transition: transform 0.4s, box-shadow 0.4s;
    }

    .skill-card:hover {
      transform: translateY(-8px) scale(1.03);
      box-shadow: 0 20px 50px rgba(34, 211, 238, 0.2);
    }

    /* ===== PROJECTS ===== */
    .projects {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 30px;
    }

    .project {
      position: relative;
      background: rgba(255,255,255,0.05);
      backdrop-filter: blur(14px);
      border: 1px solid rgba(255,255,255,0.08);
      padding: 30px;
      border-radius: 22px;
      transition: transform 0.4s, box-shadow 0.4s;
      cursor: pointer;
    }

    .project:hover {
      transform: translateY(-12px) scale(1.02);
      box-shadow: 0 25px 60px rgba(139, 92, 246, 0.35);
    }

    .project:hover {
      transform: translateY(-10px);
    }

    .project h3 {
      margin-bottom: 10px;
      color: var(--accent2);
    }

    /* ===== CONTACT ===== */
    .contact {
      text-align: center;
      color: var(--muted);
    }

    footer {
      padding: 30px;
      text-align: center;
      background: #0b0b14;
      color: var(--muted);
    }

    /* ===== ANIMATIONS ===== */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
    }

    /* ===== RESPONSIVE ===== */
    @media (max-width: 900px) {
      .hero {
        flex-direction: column-reverse;
        text-align: center;
      }
      nav {
        padding: 15px 30px;
      }
      section {
        padding: 80px 30px;
      }
    }
    .typing {
      margin-top: 15px;
      font-weight: 500;
      color: var(--accent2);
      min-height: 28px;
    }

    .reveal {
      opacity: 0;
      transform: translateY(50px);
      transition: all 0.8s ease;
    }

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }

</style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <h2>Suhana</h2>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section class="hero" id="home">
    <div class="hero-text">
      <h1>Hi, I'm <span>Suhana Pathan</span></h1>
      <h3 class="typing"></h3>
      <p>
        Aspiring Python Developer & Frontend Enthusiast passionate about
        building elegant, animated, user-friendly web applications.
      </p>
    </div>
   <div class="hero-img">
  <img src="C:\Users\patha\Downloads\new photo.jpeg" alt="Suhana Pathan">
</div>

  </section>

  <!-- ABOUT -->
  <section id="about" class="reveal">
    <h2>About Me</h2>
    <div class="about">
      I am a B.Tech graduate focusing on Python , Web Development, and
      modern UI/UX design. I enjoy crafting dark-themed, animated interfaces
      that feel smooth, professional, and intuitive.
    </div>
  </section>

  <!-- SKILLS -->
  <section id="skills" class="reveal">
    <h2>Skills</h2>
    <div class="skills">
      <div class="skill-card">Python</div>
      <div class="skill-card">HTML& CSS</div>
      <div class="skill-card">JavaScript</div>
      <div class="skill-card">SQL</div>
      <div class="skill-card">UI / UX Design</div>
    </div>
  </section>

  <!-- PROJECTS -->
   <section id="projects" class="reveal">
  <h2>Projects</h2>
  <div class="projects">
    <!-- Project Card 1 -->
    <div class="project" onclick="openModal('Personal Portfolio','A clean, responsive portfolio website built with HTML, CSS, and JavaScript to showcase skills and projects.')">
      <h3>🌙 Personal Portfolio</h3>
      <p>Responsive + Animations</p>
    </div>

    <!-- Project Card 2 -->
    <div class="project" onclick="openModal('Weather App','A simple weather application that fetches real-time data from a public API and displays it with a clean UI.')">
      <h3>☀️ Weather App</h3>
      <p>API + Responsive Design</p>
    </div>

    <!-- Project Card 3 -->
    <div class="project" onclick="openModal('Task Manager','A basic task manager application built using vanilla JS. Supports adding, editing, deleting, and saving tasks in local storage.')">
      <h3>📋 Task Manager</h3>
      <p>CRUD + Local Storage</p>
    </div>

    <!-- Project Card 4 -->
    <div class="project" onclick="openModal('Calculator','A simple web calculator built with HTML, CSS, and JS, supporting basic arithmetic operations.')">
      <h3>🧮 Calculator</h3>
      <p>JavaScript Logic + UI</p>
    </div>
  </div>
</section>

 

  <!-- MODAL -->
  <div id="modal" style="display:none; position:fixed; inset:0; background:rgba(0,0,0,0.7); backdrop-filter:blur(6px); z-index:2000; align-items:center; justify-content:center;">
    <div style="background:#111827; padding:40px; border-radius:20px; max-width:450px; width:90%; text-align:center; box-shadow:0 30px 80px rgba(0,0,0,0.8);">
      <h2 id="modalTitle" style="color:var(--accent)"></h2>
      <p id="modalDesc" style="margin:20px 0; color:var(--muted)"></p>
      <button class="btn" onclick="closeModal()">Close</button>
    </div>
  </div>

  <!-- CONTACT -->
<section id="contact" class="reveal">
<h2>Contact</h2>
<div class="contact">
<div style="margin-top:20px; display:flex; justify-content:center; gap:25px; font-size:1.5rem;">
<a href="#" style="color:var(--accent2); text-decoration:none;">🔗</a>
<a href="#" style="color:var(--accent); text-decoration:none;">🐱</a>
</div>
<p>Email: pathansuhanakhan72@gmail.com</p>
<p>LinkedIn | GitHub</p>
</div>
</section>

  <footer>
    © 2026 Suhana Pathan  Portfolio
  </footer>

  <!-- JS -->
  <script>
    // Smooth scroll animation
    document.querySelectorAll('nav a').forEach(link => {
      link.addEventListener('click', e => {
        e.preventDefault();
        document.querySelector(link.getAttribute('href'))
          .scrollIntoView({ behavior: 'smooth' });
      });
    });
      // Typing animation
    const text = [
      "Python Developer",
      "Web Development",
      "UI/UX Designer",
      "Placement Ready Fresher"
    ];
    let i = 0, j = 0;
    const typing = document.querySelector('.typing');

    function type() {
      if (j < text[i].length) {
        typing.innerHTML += text[i].charAt(j);
        j++;
        setTimeout(type, 100);
      } else {
        setTimeout(erase, 1500);
      }
    }

    function erase() {
      if (j > 0) {
        typing.innerHTML = text[i].substring(0, j - 1);
        j--;
        setTimeout(erase, 60);
      } else {
        i = (i + 1) % text.length;
        setTimeout(type, 500);
      }
    }
    type();

    // Modal functions
    function openModal(title, desc) {
      document.getElementById('modalTitle').innerText = title;
      document.getElementById('modalDesc').innerText = desc;
      document.getElementById('modal').style.display = 'flex';
    }

    function closeModal() {
      document.getElementById('modal').style.display = 'none';
    }

    // Scroll reveal animation
    const reveals = document.querySelectorAll('.reveal');
    window.addEventListener('scroll', () => {
      reveals.forEach(el => {
        const top = el.getBoundingClientRect().top;
        if (top < window.innerHeight - 100) {
          el.classList.add('active');
        }
      });
    });
  </script>

</body>
</html>
