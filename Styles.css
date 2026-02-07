<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
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

    /* HEADER */
    header {
      position: fixed;
      top: 0;
      width: 100%;
      padding: 20px 60px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 10;
      background: rgba(0,0,0,0.45);
      backdrop-filter: blur(10px);
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

    /* HERO FULL IMAGE SIN FRAME */
    .hero {
      height: 100vh;
      width: 100%;
      background: url("assets/images/hero.jpg") center / cover no-repeat;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .hero::after {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(
        to bottom,
        rgba(0,0,0,0.55),
        #000
      );
    }

    .hero-content {
      position: relative;
      text-align: center;
      max-width: 800px;
      padding: 20px;
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

    /* SECCIONES */
    section {
      padding: 120px 10%;
      opacity: 0;
      transform: translateY(40px);
      transition: all 0.8s ease;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      margin-bottom: 20px;
      color: var(--accent);
      letter-spacing: 1px;
    }

    /* TECNOLOGÍA */
    .tech {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      align-items: center;
    }

    .tech img {
      width: 100%;
      border-radius: 0; /* SIN FRAME */
      box-shadow: none;
    }

    /* SHOWCASE */
    .showcase {
      display: flex;
      gap: 30px;
      justify-content: center;
      flex-wrap: wrap;
    }

    .card {
      padding: 60px;
      border: 1px solid rgba(255,255,255,0.1);
      transition: transform 0.3s ease;
      min-width: 220px;
      text-align: center;
    }

    .card:hover {
      transform: translateY(-12px);
    }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 40px;
      background: #000;
      font-size: 0.8rem;
      opacity: 0.7;
    }

    /* RESPONSIVE */
    @media (max-width: 900px) {
      .tech {
        grid-template-columns: 1fr;
      }

      header {
        padding: 20px 30px;
      }

      .hero h1 {
        font-size: 2.2rem;
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

  <!-- HERO -->
  <section class="hero">
    <div class="hero-content">
      <h1>HUMANIDAD & TECNOLOGÍA</h1>
      <p>El futuro no se predice. Se diseña.</p>
      <button id="cta">Explorar</button>
    </div>
  </section>

  <!-- VISIÓN -->
  <section id="vision">
    <h2>Visión</h2>
    <p>
      La tecnología no es una herramienta externa.  
      Es una extensión directa de la conciencia humana.
    </p>
  </section>

  <!-- TECNOLOGÍA -->
  <section id="tech" class="tech">
    <img src="assets/images/tech.jpg" alt="Tecnología avanzada">
    <div>
      <h2>Tecnología</h2>
      <p>
        Electrónica, sistemas híbridos, espacio y tiempo
        integrados en una misma arquitectura conceptual.
      </p>
    </div>
  </section>

  <!-- PROYECTO -->
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
    // Scroll reveal
    const sections = document.querySelectorAll("section");

    const reveal = () => {
      const trigger = window.innerHeight * 0.85;
      sections.forEach(sec => {
        const top = sec.getBoundingClientRect().top;
        if (top < trigger) sec.classList.add("visible");
      });
    };

    window.addEventListener("scroll", reveal);
    reveal();

    // CTA
    document.getElementById("cta").onclick = () => {
      document.getElementById("vision")
        .scrollIntoView({ behavior: "smooth" });
    };
  </script>

</body>
</html>
