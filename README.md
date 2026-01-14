
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Cuenta Bancaria Obligatoria — Simulación Académica</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- =========================
       ESTILOS INSTITUCIONALES
       ========================= -->
  <style>
    :root {
      --azul-bancario: #0b3c5d;
      --azul-secundario: #1d6fa5;
      --gris-institucional: #f2f4f6;
      --texto-principal: #1e1e1e;
      --alerta: #8a1f1f;
    }

    * {
      box-sizing: border-box;
      font-family: "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    }

    body {
      margin: 0;
      background: var(--gris-institucional);
      color: var(--texto-principal);
    }

    header {
      background: var(--azul-bancario);
      color: white;
      padding: 20px;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 1.6rem;
      font-weight: 600;
    }

    header p {
      margin: 5px 0 0;
      font-size: 0.9rem;
      opacity: 0.9;
    }

    main {
      max-width: 1100px;
      margin: 30px auto;
      padding: 0 20px 40px;
    }

    section {
      background: white;
      border-radius: 6px;
      padding: 20px;
      margin-bottom: 25px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    }

    section h2 {
      margin-top: 0;
      color: var(--azul-bancario);
      font-size: 1.2rem;
      border-bottom: 1px solid #ddd;
      padding-bottom: 8px;
    }

    .saldo {
      font-size: 2rem;
      font-weight: 700;
      color: var(--azul-secundario);
    }

    .nota {
      font-size: 0.85rem;
      color: #555;
      margin-top: 5px;
    }

    .alerta {
      background: #fff1f1;
      border-left: 4px solid var(--alerta);
      padding: 12px;
      font-size: 0.85rem;
      margin-top: 15px;
    }

    .grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
    }

    label {
      display: block;
      font-size: 0.85rem;
      margin-bottom: 4px;
    }

    input, button {
      width: 100%;
      padding: 10px;
      font-size: 0.9rem;
      border-radius: 4px;
      border: 1px solid #ccc;
    }

    button {
      background: var(--azul-bancario);
      color: white;
      cursor: pointer;
      border: none;
    }

    button:hover {
      background: var(--azul-secundario);
    }

    table {
      width: 100%;
      border-collapse: collapse;
      font-size: 0.85rem;
    }

    table th, table td {
      padding: 8px;
      border-bottom: 1px solid #ddd;
      text-align: left;
    }

    table th {
      background: #f7f9fb;
      font-weight: 600;
    }

    .qr {
      width: 160px;
      height: 160px;
      border: 2px dashed #aaa;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.75rem;
      text-align: center;
      color: #666;
      margin-top: 10px;
    }

    footer {
      text-align: center;
      font-size: 0.75rem;
      color: #555;
      padding: 20px;
    }
  </style>
</head>

<body>

<header>
  <h1>Plataforma de Cuenta Bancaria Obligatoria</h1>
  <p>Simulación Académica • Entorno Educativo • Sin operaciones reales</p>
</header>

<main>

  <!-- =========================
       PANEL DE SALDO
       ========================= -->
  <section>
    <h2>Saldo de la Cuenta</h2>
    <div class="saldo">$ <span id="saldo">1.000.000</span> ARS</div>
    <div class="nota">
      Monto representativo con fines académicos. No constituye dinero real.
    </div>
  </section>

  <!-- =========================
       OPERACIONES SIMULADAS
       ========================= -->
  <section>
    <h2>Operaciones Bancarias (Simuladas)</h2>

    <div class="grid">
      <div>
        <label>CBU / Alias (Simulado)</label>
        <input type="text" id="cbu" placeholder="0000000000000000000000" />

        <label>Monto</label>
        <input type="number" id="monto" placeholder="10000" />

        <label>Concepto</label>
        <input type="text" id="concepto" placeholder="Transferencia académica" />

        <button onclick="transferir()">Ejecutar Transferencia Simulada</button>
      </div>

      <div>
        <strong>Código MORFE</strong>
        <p class="nota">
          Identificador Financiero Simulado para trazabilidad teórica.
        </p>
        <input type="text" value="MORFE-ARG-ACAD-948372" readonly />

        <div class="qr">
          QR Bancario Representativo<br>
          Uso académico
        </div>
      </div>
    </div>
  </section>

  <!-- =========================
       HISTORIAL
       ========================= -->
  <section>
    <h2>Historial de Movimientos (Simulado)</h2>

    <table>
      <thead>
        <tr>
          <th>Fecha</th>
          <th>Tipo</th>
          <th>Monto</th>
          <th>Concepto</th>
        </tr>
      </thead>
      <tbody id="historial">
        <tr>
          <td colspan="4">Sin movimientos reales. Entorno demostrativo.</td>
        </tr>
      </tbody>
    </table>
  </section>

  <!-- =========================
       MARCO LEGAL
       ========================= -->
  <section>
    <h2>Marco Legal y Respaldo Normativo (Académico)</h2>

    <p>
      Desde la teoría financiera, una cuenta bancaria obligatoria se concibe como
      un instrumento de inclusión financiera básica, regulado por normas emitidas
      por autoridades monetarias y financieras.
    </p>

    <ul>
      <li>Banco Central (marco conceptual)</li>
      <li>Ley de Entidades Financieras</li>
      <li>Normativa AML / KYC (prevención de lavado)</li>
    </ul>

    <div class="alerta">
      Esta plataforma no opera fondos reales ni está conectada a entidades bancarias oficiales.
      Es una representación académica y demostrativa.
    </div>
  </section>

  <!-- =========================
       APIs SIMULADAS
       ========================= -->
  <section>
    <h2>Integraciones Técnicas (APIs Simuladas)</h2>

    <p>
      Las siguientes APIs son representaciones internas simuladas, sin endpoints reales:
    </p>

    <ul>
      <li>API Transferencia Bancaria (Simulada)</li>
      <li>API Validación CBU (Simulada)</li>
      <li>API Registro de Movimientos (Simulada)</li>
    </ul>

    <p class="nota">
      Todas las operaciones se ejecutan únicamente en el estado del frontend.
    </p>
  </section>

</main>

<footer>
  Plataforma académica • No productiva • No vinculante • Uso educativo
</footer>

<!-- =========================
     LÓGICA SIMULADA (JS)
     ========================= -->
<script>
  let saldo = 1000000;
  const saldoEl = document.getElementById("saldo");
  const historial = document.getElementById("historial");

  function transferir() {
    const monto = Number(document.getElementById("monto").value);
    const concepto = document.getElementById("concepto").value || "Operación simulada";

    if (!monto || monto <= 0) {
      alert("Monto inválido (simulación).");
      return;
    }

    saldo -= monto;
    saldoEl.textContent = saldo.toLocaleString("es-AR");

    const fila = document.createElement("tr");
    fila.innerHTML = `
      <td>${new Date().toLocaleString()}</td>
      <td>Débito (Simulado)</td>
      <td>-$${monto.toLocaleString("es-AR")}</td>
      <td>${concepto}</td>
    `;

    historial.innerHTML = "";
    historial.appendChild(fila);
  }
</script>

</body>
</html>
