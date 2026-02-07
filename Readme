<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>2064 · Evolución del Conocimiento</title>

  <style>
    /* ==============================
       RESET Y BASE
    ============================== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      height: 100vh;
      background: radial-gradient(circle at top, #0b1020, #000);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: Arial, sans-serif;
    }

    /* ==============================
       CANVAS BASE 1080x1080
    ============================== */
    #canvas {
      position: relative;
      width: 1080px;
      height: 1080px;
      background: linear-gradient(145deg, #050b1e, #02040a);
      overflow: hidden;
    }

    /* ==============================
       TEXTO PRINCIPAL
    ============================== */
    #title {
      position: absolute;
      top: 60px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 120px;
      font-weight: 900;
      letter-spacing: 6px;
      color: #e6f1ff;
      z-index: 10;
      text-shadow: 0 0 30px rgba(0, 180, 255, 0.6);
    }

    /* ==============================
       IMAGEN CIENCIA ANTIGUA
    ============================== */
    #ancient {
      position: absolute;
      width: 300px;
      z-index: 2;
      filter: drop-shadow(0 0 20px rgba(255, 200, 100, 0.3));
    }

    /* ==============================
       IMAGEN ESPACIAL
    ============================== */
    #space {
      position: absolute;
      width: 340px;
      z-index: 3;
      filter: drop-shadow(0 0 25px rgba(120, 180, 255, 0.4));
    }

    /* ==============================
       NÚCLEO CENTRAL (ARDUINO)
    ============================== */
    #arduino {
      position: absolute;
      width: 480px;
      height: 280px;
      border-radius: 18px;
      background: linear-gradient(135deg, #1e90ff, #00ffd5);
      box-shadow: 0 0 40px rgba(0, 255, 220, 0.6);
      z-index: 5;

      display: flex;
      align-items: center;
      justify-content: center;
      transition: transform 3s ease-in-out;
    }

    #arduino span {
      text-align: center;
      font-size: 36px;
      font-weight: 800;
      letter-spacing: 2px;
      color: #001018;
    }
  </style>
</head>

<body>

  <div id="canvas">

    <div id="title">2064</div>

    <img
      id="ancient"
      src="IMG_20260207_180810_846.jpg"
      alt="Instrumento astronómico antiguo"
    />

    <img
      id="space"
      src="IMG_20260207_180408_501.jpg"
      alt="Satélites en el espacio"
    />

    <div id="arduino">
      <span>ARDUINO<br>+<br>COSMOS</span>
    </div>

  </div>

  <script>
    /* ==============================
       COORDENADAS AJUSTABLES
    ============================== */

    const ancientPos = { x: 80,  y: 120 };
    const spacePos   = { x: 650, y: 150 };
    const arduinoPos = { x: 300, y: 420 };

    /* ==============================
       APLICAR POSICIONES
    ============================== */

    const ancient = document.getElementById("ancient");
    const space = document.getElementById("space");
    const arduino = document.getElementById("arduino");

    ancient.style.left = ancientPos.x + "px";
    ancient.style.top  = ancientPos.y + "px";

    space.style.left = spacePos.x + "px";
    space.style.top  = spacePos.y + "px";

    arduino.style.left = arduinoPos.x + "px";
    arduino.style.top  = arduinoPos.y + "px";

    /* ==============================
       ANIMACIÓN SUAVE
    ============================== */

    let direction = 1;

    setInterval(() => {
      direction *= -1;
      arduino.style.transform = `translateY(${direction * 8}px)`;
    }, 3000);
  </script>

</body>
</html>
