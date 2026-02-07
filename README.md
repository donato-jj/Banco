<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CVΛL · Humanidad & Tecnología</title>

  <style>
    :root {
      --dark: #050505;
      --light: #f5f5f5;
      --accent: #c9a24d;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }

    body {
      background: var(--dark);
      color: var(--light);
      overflow-x: hidden;
    }

    header {
      position: fixed;
      top: 0;
      width: 100%;
      padding: 20px 60px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: rgba(0,0,0,0.45);
      backdrop-filter: blur(10px);
      z-index: 10;
    }

    .logo {
      font-weight: bold;
      letter-spacing: 4px;
    }

    nav a {
      margin-left: 30px;
      color: var(--light);
      text-decoration: none;
      font-size: 0.9rem;
    }

    /* HERO */
    .hero {
      height: 100vh;
      background: url("assets/images/hero.jpg") center / cover no-repeat;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
    }

    .hero::after {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(to bottom, rgba(0,0,0,0.6), #000);
    }

    .hero-content {
      position: relative;
      text-align: center;
      z-index: 1;
    }

    .hero h1 {
      font-size: 3rem;
      letter-spacing: 3px;
    }

    .hero p {
      margin: 20px 0 40px;
      opacity: 0.85;
    }

    .hero button {
      padding: 14px 42px;
      border: none;
      background: var(--accent);
      color: #000;
      font-weight: bold;
      cursor: pointer;
    }

    section {
      padding: 120px 10%;
      opacity: 0;
      transform: translateY(40px);
      transition: 0.8s ease;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      color: var(--accent);
      margin-bottom: 20px;
    }

    .tech {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      align-items: center;
    }

    .tech img {
      width: 100%;
    }

    .showcase {
      display: flex;
      gap: 30px;
      justify-content: center;
      flex-wrap: wrap;
    }

    .card {
      padding: 60px;
      border: 1px solid rgba(255,255,255,0.1);
      min-width: 220px;
      text-align: center;
      transition: transform 0.3s;
    }

    .card:hover {
      transform: translateY(-12px);
    }

    footer {
      padding: 40px;
      text-align: center;
      background: #000;
      font-size: 0.8rem;
      opacity: 0.7;
    }

    @media (max-width: 900px) {
      .tech {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>

<body>

<header>
  <div class="logo">CVΛL</div>
  <nav>
    <a href="#vision">Visión</a>
    <a href="#tech">Tecnología</a>
    <a href="#proyecto">Proyecto</a>
    <a href="#contacto">Contacto</a>
  </nav>
</header>

<section class="hero">
  <div class="hero-content">
    <h1>HUMANIDAD & TECNOLOGÍA</h1>
    <p>El futuro no se predice. Se diseña.</p>
    <button id="cta">Explorar</button>
  </div>
</section>

<section id="vision">
  <h2>Visión</h2>
  <p>La tecnología es una extensión directa de la conciencia humana.</p>
</section>

<section id="tech" class="tech">
  <img src="assets/images/tech.jpg" alt="Tecnología avanzada">
  <div>
    <h2>Tecnología</h2>
    <p>Electrónica, sistemas híbridos y arquitectura conceptual.</p>
  </div>
</section>

<section id="proyecto">
  <h2>Proyecto</h2>
  <div class="showcase">
    <div class="card">Electrónica</div>
    <div class="card">Espacio</div>
    <div class="card">Conciencia</div>
  </div>
</section>

<footer id="contacto">
  © 2064 · Proyecto CVΛL
</footer>

<script>
  const sections = document.querySelectorAll("section");

  const reveal = () => {
    const trigger = window.innerHeight * 0.85;
    sections.forEach(sec => {
      if (sec.getBoundingClientRect().top < trigger) {
        sec.classList.add("visible");
      }
    });
  };

  window.addEventListener("scroll", reveal);
  reveal();

  document.getElementById("cta").onclick = () => {
    document.getElementById("vision").scrollIntoView({ behavior: "smooth" });
  };
</script>

</body>
</html>
