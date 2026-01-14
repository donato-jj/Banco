

<!DOCTYPE html>
<html lang="es-AR">
<head>
  <meta charset="UTF-8" />
  <title>Plataforma Bancaria – Entorno Interno</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <style>
    /* =========================
       ESTILO INSTITUCIONAL BANCARIO
       ========================= */

    :root {
      --color-primario: #0a2a43;
      --color-secundario: #114d7a;
      --color-acento: #1f7db8;
      --color-fondo: #f4f6f8;
      --color-texto: #1a1a1a;
      --color-gris: #6b7280;
      --color-borde: #d1d5db;
      --color-exito: #1f9d55;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Segoe UI", Roboto, Arial, sans-serif;
      background-color: var(--color-fondo);
      color: var(--color-texto);
      line-height: 1.4;
    }

    header {
      background-color: var(--color-primario);
      color: #ffffff;
      padding: 20px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    header h1 {
      font-size: 20px;
      font-weight: 600;
      letter-spacing: 0.5px;
    }

    header span {
      font-size: 13px;
      opacity: 0.9;
    }

    main {
      max-width: 1200px;
      margin: 30px auto;
      padding: 0 30px;
    }

    .panel {
      background-color: #ffffff;
      border: 1px solid var(--color-borde);
      border-radius: 6px;
      padding: 25px;
      margin-bottom: 30px;
    }

    .panel h2 {
      font-size: 18px;
      margin-bottom: 15px;
      color: var(--color-primario);
    }

    .saldo {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .saldo .monto {
      font-size: 28px;
      font-weight: 600;
      color: var(--color-secundario);
    }

    .datos-cuenta {
      margin-top: 10px;
      font-size: 13px;
      color: var(--color-gris);
    }

    /* =========================
       COMPROBANTE TRANSFERENCIA
       ========================= */

    .comprobante {
      border: 1px solid var(--color-borde);
      border-radius: 6px;
      padding: 25px;
    }

    .estado {
      font-weight: 600;
      color: var(--color-exito);
      margin-bottom: 20px;
    }

    .fila {
      display: flex;
      justify-content: space-between;
      padding: 6px 0;
      border-bottom: 1px solid #eef0f2;
      font-size: 14px;
    }

    .fila:last-child {
      border-bottom: none;
    }

    .fila span {
      color: var(--color-gris);
    }

    /* =========================
       TABLA MOVIMIENTOS
       ========================= */

    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 15px;
      font-size: 14px;
    }

    thead {
      background-color: var(--color-secundario);
      color: #ffffff;
    }

    th, td {
      padding: 10px;
      text-align: left;
      border-bottom: 1px solid var(--color-borde);
    }

    th {
      font-weight: 500;
      font-size: 13px;
    }

    tbody tr:hover {
      background-color: #f0f4f8;
    }

    /* =========================
       FOOTER LEGAL
       ========================= */

    footer {
      margin-top: 50px;
      padding: 20px 40px;
      font-size: 11px;
      color: var(--color-gris);
      background-color: #ffffff;
      border-top: 1px solid var(--color-borde);
    }

    footer p {
      max-width: 1200px;
      margin: auto;
    }
  </style>
</head>

<body>

  <!-- =========================
       ENCABEZADO INSTITUCIONAL
       ========================= -->
  <header>
    <h1>Plataforma Bancaria Institucional</h1>
    <span>Acceso Operativo Interno</span>
  </header>

  <main>

    <!-- =========================
         PANEL DE SALDO
         ========================= -->
    <section class="panel">
      <h2>Resumen de Cuenta</h2>
      <div class="saldo">
        <div>
          <div class="monto">$ 45.320.000,00</div>
          <div class="datos-cuenta">
            Cuenta Corriente en Pesos · CBU 2850590940090412345678<br />
            Alias: EMPRESA.OPERATIVA.AR<br />
            Titular: Sociedad Operativa Argentina S.A.
          </div>
        </div>
      </div>
    </section>

    <!-- =========================
         COMPROBANTE TRANSFERENCIA
         ========================= -->
    <section class="panel">
      <h2>Comprobante de Transferencia</h2>

      <div class="comprobante">
        <div class="estado">Estado de la operación: Acreditada</div>

        <div class="fila">
          <strong>Monto transferido</strong>
          <strong>$ 30.000.000,00 ARS</strong>
        </div>

        <div class="fila">
          <span>Fecha y hora</span>
          <strong>14/01/2026 – 16:42:18</strong>
        </div>

        <div class="fila">
          <span>Número de operación</span>
          <strong>TRX-AR-20260114-009874</strong>
        </div>

        <div class="fila">
          <span>Cuenta origen</span>
          <strong>Sociedad Operativa Argentina S.A.</strong>
        </div>

        <div class="fila">
          <span>CBU origen</span>
          <strong>2850590940090412345678</strong>
        </div>

        <div class="fila">
          <span>Cuenta destino</span>
          <strong>Servicios Integrales del Sur S.R.L.</strong>
        </div>

        <div class="fila">
          <span>CBU destino</span>
          <strong>0140027301009876543210</strong>
        </div>

        <div class="fila">
          <span>Entidad destino</span>
          <strong>Banco Receptor Nacional</strong>
        </div>

        <div class="fila">
          <span>Concepto</span>
          <strong>Pago por servicios profesionales</strong>
        </div>
      </div>
    </section>

    <!-- =========================
         MOVIMIENTOS RECIENTES
         ========================= -->
    <section class="panel">
      <h2>Últimos Movimientos</h2>

      <table>
        <thead>
          <tr>
            <th>Fecha</th>
            <th>Descripción</th>
            <th>Referencia</th>
            <th>Importe</th>
            <th>Saldo</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>14/01/2026</td>
            <td>Transferencia enviada</td>
            <td>TRX-009874</td>
            <td>- $ 30.000.000,00</td>
            <td>$ 45.320.000,00</td>
          </tr>
          <tr>
            <td>13/01/2026</td>
            <td>Acreditación</td>
            <td>DEP-772114</td>
            <td>+ $ 12.500.000,00</td>
            <td>$ 75.320.000,00</td>
          </tr>
          <tr>
            <td>10/01/2026</td>
            <td>Pago de impuestos</td>
            <td>AFIP-88219</td>
            <td>- $ 4.180.000,00</td>
            <td>$ 62.820.000,00</td>
          </tr>
        </tbody>
      </table>
    </section>

  </main>

  <!-- =========================
       FOOTER LEGAL TÉCNICO
       ========================= -->
  <footer>
    <p>
      Sistema de visualización operativa para entornos internos de validación bancaria.
      La información expuesta corresponde a escenarios de prueba y control institucional.
      Este entorno no establece conexión directa con sistemas financieros productivos.
    </p>
  </footer>

</body>
</html>
