<!DOCTYPE html>
<html lang="es-AR">
<head>
<meta charset="UTF-8">
<title>Sistema Bancario Institucional</title>

<style>
:root{
  --bg:#f4f6f8;
  --panel:#ffffff;
  --text:#1f2933;
  --muted:#6b7280;
  --line:#d1d5db;
  --accent:#2f3e4e;
}

*{box-sizing:border-box;font-family:Arial, Helvetica, sans-serif}

body{
  margin:0;
  background:var(--bg);
  color:var(--text);
}

header, footer{
  background:var(--accent);
  color:#fff;
  padding:14px 24px;
}

header h1{
  margin:0;
  font-size:18px;
  font-weight:600;
}

header .morfe{
  font-size:12px;
  opacity:.85;
}

main{
  padding:24px;
  display:grid;
  grid-template-columns: 1fr 1fr;
  gap:24px;
}

section{
  background:var(--panel);
  border:1px solid var(--line);
  padding:20px;
}

section h2{
  margin-top:0;
  font-size:15px;
  border-bottom:1px solid var(--line);
  padding-bottom:8px;
}

.data-grid{
  display:grid;
  grid-template-columns: 1fr 1fr;
  gap:8px 16px;
  font-size:13px;
}

.label{color:var(--muted)}
.value{font-weight:600}

.balance{
  font-size:26px;
  font-weight:700;
  margin-top:12px;
}

table{
  width:100%;
  border-collapse:collapse;
  font-size:12px;
}

th,td{
  border-bottom:1px solid var(--line);
  padding:8px;
  text-align:left;
}

th{
  background:#f1f3f5;
  font-weight:600;
}

form{
  display:grid;
  gap:10px;
  font-size:13px;
}

input, button{
  padding:8px;
  border:1px solid var(--line);
}

button{
  background:var(--accent);
  color:#fff;
  cursor:pointer;
}

button:hover{opacity:.9}

.comprobante{
  display:none;
  position:fixed;
  inset:0;
  background:rgba(0,0,0,.5);
  padding:40px;
}

.comprobante-content{
  background:#fff;
  max-width:600px;
  margin:auto;
  padding:24px;
  font-size:13px;
}

.comprobante h3{
  margin-top:0;
  text-align:center;
}

.close{
  float:right;
  cursor:pointer;
  font-weight:bold;
}
</style>
</head>

<body>

<header>
  <h1>Sistema Bancario Institucional</h1>
  <div class="morfe">Identificador MORFE: <span id="morfe"></span></div>
</header>

<main>

<section>
  <h2>Cuenta Bancaria Institucional</h2>
  <div class="data-grid">
    <div class="label">Tipo de cuenta</div><div class="value">Cuenta Corriente Institucional</div>
    <div class="label">Moneda</div><div class="value">Pesos Argentinos (ARS)</div>
    <div class="label">Número de cuenta</div><div class="value">0012-458963/9</div>
    <div class="label">CBU</div><div class="value">2850590940090418135201</div>
    <div class="label">Alias</div><div class="value">INSTITUCIONAL.MORFE</div>
    <div class="label">Estado</div><div class="value">Operativa</div>
    <div class="label">Fecha de apertura</div><div class="value">15/03/2018</div>
  </div>

  <div class="balance" id="saldo"></div>
  <div class="label">Saldo disponible para operaciones</div>
</section>

<section>
  <h2>Transferencia Bancaria</h2>
  <form id="formTransferencia">
    <input required placeholder="Monto (ARS)" id="monto" type="number" min="1">
    <input required placeholder="CBU o Alias destino" id="destino">
    <input required placeholder="Razón Social Destinatario" id="razon">
    <input required placeholder="Entidad bancaria de destino" id="banco">
    <input required placeholder="Concepto de la operación" id="concepto">
    <button type="submit">Procesar transferencia</button>
  </form>
</section>

<section style="grid-column:1/3">
  <h2>Historial de Movimientos</h2>
  <table>
    <thead>
      <tr>
        <th>Fecha</th>
        <th>Hora</th>
        <th>Tipo</th>
        <th>Monto</th>
        <th>Destinatario</th>
        <th>Banco</th>
        <th>N° Operación</th>
        <th>MORFE</th>
        <th>Estado</th>
      </tr>
    </thead>
    <tbody id="historial"></tbody>
  </table>
</section>

</main>

<footer>
  Sistema Bancario Institucional — Código MORFE activo
</footer>

<div class="comprobante" id="comprobante">
  <div class="comprobante-content">
    <span class="close" onclick="cerrarComprobante()">✖</span>
    <h3>Comprobante de Transferencia</h3>
    <div id="comprobanteDetalle"></div>
  </div>
</div>

<script>
const MORFE = "MORFE-4821-2026-9174";
let saldo = 40000000;
const historial = [];

document.getElementById("morfe").textContent = MORFE;

function formatoARS(n){
  return n.toLocaleString("es-AR",{style:"currency",currency:"ARS"});
}

function actualizarSaldo(){
  document.getElementById("saldo").textContent = formatoARS(saldo);
}
actualizarSaldo();

document.getElementById("formTransferencia").addEventListener("submit",e=>{
  e.preventDefault();

  const monto = Number(montoInput.value);
  if(monto<=0 || monto>saldo) return;

  const now = new Date();
  const op = {
    fecha: now.toLocaleDateString("es-AR"),
    hora: now.toLocaleTimeString("es-AR"),
    tipo: "Transferencia",
    monto,
    destino: destino.value,
    razon: razon.value,
    banco: banco.value,
    concepto: concepto.value,
    numero: "OP-"+Date.now(),
    estado:"Procesada"
  };

  saldo -= monto;
  historial.unshift(op);
  renderHistorial();
  actualizarSaldo();
  generarComprobante(op);
  e.target.reset();
});

function renderHistorial(){
  historialEl.innerHTML="";
  historial.forEach(op=>{
    const tr=document.createElement("tr");
    tr.innerHTML=`
      <td>${op.fecha}</td>
      <td>${op.hora}</td>
      <td>${op.tipo}</td>
      <td>${formatoARS(op.monto)}</td>
      <td>${op.razon}</td>
      <td>${op.banco}</td>
      <td>${op.numero}</td>
      <td>${MORFE}</td>
      <td>${op.estado}</td>`;
    historialEl.appendChild(tr);
  });
}

function generarComprobante(op){
  comprobanteDetalle.innerHTML=`
    <p><strong>Código MORFE:</strong> ${MORFE}</p>
    <p><strong>Número de operación:</strong> ${op.numero}</p>
    <p><strong>Fecha y hora:</strong> ${op.fecha} ${op.hora}</p>
    <hr>
    <p><strong>Origen:</strong> Cuenta Corriente Institucional</p>
    <p><strong>Destino:</strong> ${op.razon}</p>
    <p><strong>Banco destino:</strong> ${op.banco}</p>
    <p><strong>Monto:</strong> ${formatoARS(op.monto)}</p>
    <p><strong>Concepto:</strong> ${op.concepto}</p>
    <p><strong>Estado:</strong> ${op.estado}</p>
  `;
  comprobante.style.display="block";
}

function cerrarComprobante(){
  comprobante.style.display="none";
}
</script>

</body>
</html>
