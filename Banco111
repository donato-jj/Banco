<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Interfaz Bancaria Institucional — Simulación Académica</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        /* ==============================
           ESTILO INSTITUCIONAL BANCARIO
           ============================== */

        :root {
            --azul-institucional: #0a2a43;
            --azul-secundario: #123d5a;
            --gris-claro: #f2f4f7;
            --gris-medio: #d1d5db;
            --texto-principal: #1f2933;
            --texto-secundario: #4b5563;
            --blanco: #ffffff;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: "Segoe UI", Arial, sans-serif;
        }

        body {
            background-color: var(--gris-claro);
            color: var(--texto-principal);
            line-height: 1.5;
        }

        header {
            background-color: var(--azul-institucional);
            color: var(--blanco);
            padding: 20px;
            text-align: center;
        }

        header h1 {
            font-size: 1.4rem;
            letter-spacing: 0.5px;
        }

        header p {
            font-size: 0.9rem;
            opacity: 0.9;
        }

        main {
            max-width: 1100px;
            margin: 30px auto;
            padding: 20px;
        }

        .panel {
            background-color: var(--blanco);
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 25px;
            box-shadow: 0 2px 6px rgba(0,0,0,0.08);
        }

        .panel h2 {
            font-size: 1.1rem;
            margin-bottom: 15px;
            color: var(--azul-secundario);
            border-bottom: 1px solid var(--gris-medio);
            padding-bottom: 8px;
        }

        .saldo-principal {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .saldo-monto {
            font-size: 2rem;
            font-weight: 600;
            color: var(--azul-institucional);
        }

        .estado-cuenta {
            font-size: 0.9rem;
            color: green;
            font-weight: 500;
        }

        .detalle-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
        }

        .detalle-item {
            font-size: 0.9rem;
        }

        .detalle-item span {
            display: block;
            font-weight: 600;
            color: var(--texto-secundario);
            margin-bottom: 3px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.9rem;
        }

        table thead {
            background-color: var(--gris-claro);
        }

        table th, table td {
            padding: 10px;
            border-bottom: 1px solid var(--gris-medio);
            text-align: left;
        }

        .estado-ok {
            color: green;
            font-weight: 600;
        }

        .comprobante {
            border: 1px dashed var(--gris-medio);
            padding: 15px;
            margin-top: 15px;
            font-size: 0.85rem;
        }

        .qr {
            margin-top: 15px;
            text-align: center;
            font-size: 0.8rem;
            color: var(--texto-secundario);
        }

        .qr-box {
            width: 120px;
            height: 120px;
            margin: 10px auto;
            border: 2px solid var(--gris-medio);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.7rem;
            color: var(--texto-secundario);
        }

        .nota-legal {
            margin-top: 30px;
            background-color: #fffbe6;
            border-left: 4px solid #facc15;
            padding: 15px;
            font-size: 0.85rem;
            color: #78350f;
        }

        footer {
            text-align: center;
            font-size: 0.75rem;
            color: var(--texto-secundario);
            margin: 20px 0;
        }

        @media (max-width: 600px) {
            .saldo-monto {
                font-size: 1.6rem;
            }
        }
    </style>
</head>

<body>

<header>
    <h1>Plataforma Bancaria Institucional</h1>
    <p>Interfaz académica de simulación financiera — Uso demostrativo</p>
</header>

<main>

    <!-- PANEL SALDO -->
    <section class="panel">
        <h2>Resumen de Cuenta</h2>
        <div class="saldo-principal">
            <div class="saldo-monto">ARS 40.000.000,00</div>
            <div class="estado-cuenta">Cuenta activa – Operativa (representación visual)</div>
        </div>
    </section>

    <!-- DETALLE DE CUENTA -->
    <section class="panel">
        <h2>Detalle de la Cuenta</h2>
        <div class="detalle-grid">
            <div class="detalle-item">
                <span>Tipo de Cuenta</span>
                Cuenta Bancaria Institucional
            </div>
            <div class="detalle-item">
                <span>CBU</span>
                0000000000000000000000 (simulado)
            </div>
            <div class="detalle-item">
                <span>Alias</span>
                CUENTA.INSTITUCIONAL.DEMO
            </div>
            <div class="detalle-item">
                <span>Código MORFE</span>
                MORFE-INT-40M-ARS-001
            </div>
            <div class="detalle-item">
                <span>Entidad Emisora</span>
                Entidad Financiera Institucional Genérica
            </div>
            <div class="detalle-item">
                <span>Fecha de Apertura</span>
                01/01/2025
            </div>
        </div>
    </section>

    <!-- TRANSFERENCIAS -->
    <section class="panel">
        <h2>Transferencias Bancarias (Simulación)</h2>
        <table>
            <thead>
                <tr>
                    <th>Fecha</th>
                    <th>Tipo</th>
                    <th>Monto</th>
                    <th>Concepto</th>
                    <th>Estado</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>14/01/2026 14:32</td>
                    <td>Saliente</td>
                    <td>ARS 5.000.000,00</td>
                    <td>Transferencia institucional simulada</td>
                    <td class="estado-ok">Procesada</td>
                </tr>
                <tr>
                    <td>12/01/2026 09:10</td>
                    <td>Entrante</td>
                    <td>ARS 8.500.000,00</td>
                    <td>Acreditación demostrativa</td>
                    <td class="estado-ok">Acreditada</td>
                </tr>
            </tbody>
        </table>

        <div class="comprobante">
            <strong>Comprobante de Operación (Simulado)</strong><br>
            Número de comprobante: COMP-INT-00045872<br>
            Referencia bancaria: REF-DEMO-ARS-40M<br>
            CBU origen/destino: Datos simulados<br>
            Fecha de emisión: 14/01/2026
        </div>

        <div class="qr">
            Identificador visual QR / MORFE
            <div class="qr-box">QR<br>SIMULADO</div>
        </div>
    </section>

    <!-- NOTA LEGAL -->
    <div class="nota-legal">
        <strong>Nota legal:</strong><br>
        Esta interfaz es de carácter académico, demostrativo e institucional. No constituye un sistema bancario real, no ejecuta transacciones financieras reales ni representa una entidad financiera operativa. Todos los datos, montos e identificadores son simulados con fines educativos y de presentación.
    </div>

</main>

<footer>
    © 2026 — Prototipo bancario institucional | Simulación visual profesional
</footer>

</body>
</html>
