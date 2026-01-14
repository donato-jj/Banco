# Banco
Banco 
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Cuenta Bancaria Obligatoria – Respaldo Legal</title>

    <!--
        ESTILOS GENERALES
        Diseño sobrio, institucional, inspirado en home banking y portales estatales.
        CSS embebido según requisito académico.
    -->
    <style>
        :root {
            --azul-institucional: #1f3a5f;
            --gris-oscuro: #2e2e2e;
            --gris-claro: #f2f4f6;
            --blanco: #ffffff;
            --borde: #d0d6dc;
        }

        * {
            box-sizing: border-box;
            font-family: "Segoe UI", Roboto, Arial, sans-serif;
        }

        body {
            margin: 0;
            background-color: var(--gris-claro);
            color: var(--gris-oscuro);
        }

        header {
            background-color: var(--azul-institucional);
            color: var(--blanco);
            padding: 24px;
            text-align: center;
        }

        header h1 {
            margin: 0;
            font-size: 1.6rem;
            font-weight: 600;
        }

        header p {
            margin-top: 8px;
            font-size: 0.95rem;
            opacity: 0.9;
        }

        main {
            max-width: 1100px;
            margin: 32px auto;
            padding: 0 16px;
        }

        section {
            background-color: var(--blanco);
            border: 1px solid var(--borde);
            border-radius: 6px;
            padding: 24px;
            margin-bottom: 24px;
        }

        section h2 {
            margin-top: 0;
            font-size: 1.25rem;
            color: var(--azul-institucional);
            border-bottom: 1px solid var(--borde);
            padding-bottom: 8px;
        }

        .destacado {
            font-size: 1.2rem;
            font-weight: 600;
            margin: 12px 0;
        }

        .aclaracion {
            font-size: 0.9rem;
            color: #555;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 16px;
        }

        .dato {
            border: 1px solid var(--borde);
            border-radius: 4px;
            padding: 12px;
            background-color: #fafbfc;
        }

        .dato span {
            display: block;
            font-size: 0.8rem;
            color: #666;
        }

        .dato strong {
            font-size: 0.95rem;
        }

        /* Transferencias (visual) */
        .transferencias label {
            display: block;
            font-size: 0.85rem;
            margin-top: 12px;
        }

        .transferencias input {
            width: 100%;
            padding: 8px;
            margin-top: 4px;
            border: 1px solid var(--borde);
            border-radius: 4px;
        }

        .btn {
            margin-top: 16px;
            padding: 10px;
            width: 100%;
            background-color: var(--azul-institucional);
            color: var(--blanco);
            border: none;
            border-radius: 4px;
            font-size: 0.95rem;
            cursor: default; /* visual, no funcional */
        }

        /* QR simulado */
        .qr-box {
            width: 140px;
            height: 140px;
            background:
                linear-gradient(90deg, #000 25%, transparent 25%) 0 0 / 20px 20px,
                linear-gradient(#000 25%, transparent 25%) 0 0 / 20px 20px;
            border: 6px solid #000;
            margin: 16px auto;
        }

        footer {
            text-align: center;
            font-size: 0.8rem;
            color: #666;
            padding: 24px;
        }
    </style>
</head>

<body>

    <!-- ENCABEZADO INSTITUCIONAL -->
    <header>
        <h1>Cuenta Bancaria Obligatoria – Respaldo Legal</h1>
        <p>Interfaz académica de carácter institucional y regulado</p>
    </header>

    <main>

        <!-- MONTO GARANTIZADO -->
        <section>
            <h2>Monto Garantizado</h2>
            <p class="destacado">Monto garantizado: $1.000.000 (un millón de pesos)</p>
            <p class="aclaracion">
                Este monto se encuentra garantizado por normativa vigente aplicable al esquema de
                cuentas bancarias obligatorias, conforme a marcos regulatorios financieros.
            </p>
        </section>

        <!-- MARCO LEGAL -->
        <section>
            <h2>Marco Legal y Respaldo Normativo</h2>
            <p>
                La Cuenta Bancaria Obligatoria es un instrumento financiero de carácter regulado,
                establecido dentro de un marco normativo que define su obligatoriedad, trazabilidad
                y alcance institucional.
            </p>
            <p>
                El esquema legal vigente establece la garantía del monto informado, así como los
                mecanismos de validación, supervisión y control por parte de las entidades
                reguladoras correspondientes.
            </p>
            <p class="aclaracion">
                Texto redactado con fines académicos y demostrativos, no constitutivo de asesoramiento legal.
            </p>
        </section>

        <!-- DATOS BANCARIOS SIMULADOS -->
        <section>
            <h2>Datos Bancarios de la Cuenta</h2>
            <div class="grid">
                <div class="dato">
                    <span>CBU / CVU</span>
                    <strong>2850590940090418135201</strong>
                </div>
                <div class="dato">
                    <span>Alias Bancario</span>
                    <strong>CUENTA.OBLIGATORIA.LEGAL</strong>
                </div>
                <div class="dato">
                    <span>Tipo de Cuenta</span>
                    <strong>Cuenta Bancaria Obligatoria</strong>
                </div>
                <div class="dato">
                    <span>Entidad Reguladora</span>
                    <strong>Autoridad Financiera Nacional</strong>
                </div>
                <div class="dato">
                    <span>Estado de la Cuenta</span>
                    <strong>Activa y validada</strong>
                </div>
            </div>
        </section>

        <!-- TRANSFERENCIAS (VISUAL) -->
        <section class="transferencias">
            <h2>Transferencias Bancarias</h2>

            <!-- Campos únicamente visuales -->
            <label>Monto</label>
            <input type="text" placeholder="$">

            <label>CBU / CVU destino</label>
            <input type="text" placeholder="Ingrese CBU o CVU">

            <label>Concepto</label>
            <input type="text" placeholder="Concepto de la transferencia">

            <button class="btn">Iniciar transferencia</button>
        </section>

        <!-- QR -->
        <section>
            <h2>Validación y Transferencias mediante QR</h2>
            <div class="qr-box" aria-label="Código QR simulado"></div>
            <p class="aclaracion" style="text-align:center;">
                QR interoperable con plataformas bancarias y billeteras virtuales.
            </p>
        </section>

        <!-- CÓDIGO MORFE -->
        <section>
            <h2>Código MORFE</h2>
            <p>
                El Código MORFE (Módulo de Operación y Registro Financiero Estandarizado)
                es un identificador institucional utilizado para reforzar los procesos de
                validación, trazabilidad y control de operaciones asociadas a esta cuenta.
            </p>
            <p>
                Su función principal es asegurar la coherencia entre la identidad de la cuenta,
                las operaciones registradas y los sistemas de supervisión regulatoria.
            </p>

            <div class="dato">
                <span>Ejemplo de Código MORFE</span>
                <strong>MORFE-AR-2026-0001-LEG</strong>
            </div>
        </section>

        <!-- COMPATIBILIDAD -->
        <section>
            <h2>Compatibilidad con Plataformas</h2>
            <p>
                Esta cuenta se encuentra diseñada para operar dentro de esquemas de interoperabilidad
                financiera, permitiendo su integración con:
            </p>
            <ul>
                <li>Bancos tradicionales</li>
                <li>Billeteras virtuales</li>
                <li>Plataformas de pago interoperables</li>
            </ul>
            <p class="aclaracion">
                Información presentada con fines descriptivos y académicos.
            </p>
        </section>

    </main>

    <!-- PIE INSTITUCIONAL -->
    <footer>
        Interfaz académica • Diseño institucional • HTML + CSS sin JavaScript
    </footer>

</body>
</html>
