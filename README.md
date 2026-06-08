 <!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FEMLAC 2026 — Directorio de Socios</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Segoe UI',Arial,sans-serif;background:#f0f7fc;color:#0d3550;min-height:100vh}
.header{background:linear-gradient(135deg,#1a5f8a 0%,#2478a8 60%,#3b9dd2 100%);padding:16px 20px 0;box-shadow:0 3px 16px rgba(26,95,138,.25)}
.header-top{display:flex;align-items:center;gap:14px;margin-bottom:14px}
.logo-box{width:64px;height:64px;border-radius:12px;background:#fff;display:flex;align-items:center;justify-content:center;padding:5px;box-shadow:0 2px 8px rgba(0,0,0,.2);flex-shrink:0}
.header-title{color:#fff;font-size:15px;font-weight:800;line-height:1.2}
.header-sub{color:rgba(255,255,255,.72);font-size:11px;margin-top:3px}
.tabs{display:flex;gap:2px;overflow-x:auto}
.tab{border:none;cursor:pointer;padding:9px 16px;font-size:12px;font-weight:700;border-radius:8px 8px 0 0;background:rgba(255,255,255,.15);color:rgba(255,255,255,.9);transition:all .15s;white-space:nowrap}
.tab.active{background:#fff;color:#1a5f8a}
.main{max-width:1160px;margin:0 auto;padding:16px 12px 60px}
.stats{display:flex;gap:8px;margin-bottom:16px;flex-wrap:wrap}
.stat{background:#fff;border-radius:10px;padding:10px 14px;border:1px solid #aed6ef;flex:1;min-width:120px}
.stat-label{font-size:9.5px;color:#4a7fa0;font-weight:600;text-transform:uppercase;letter-spacing:.05em;margin-bottom:3px}
.stat-value{font-size:22px;font-weight:800;line-height:1}
.stat-sub{font-size:10px;color:#89b0c8;margin-top:2px}
.banner{background:#fff3cc;border:1px solid #f5c49a;border-radius:10px;padding:10px 14px;margin-bottom:12px;font-size:12px;color:#916a00;display:flex;align-items:center;gap:8px}
.filters{display:flex;gap:8px;margin-bottom:12px;flex-wrap:wrap;align-items:center}
.filters input,.filters select{border:1px solid #aed6ef;border-radius:8px;padding:8px 10px;font-size:12px;background:#fff;color:#0d3550;outline:none}
.filters input{flex:1;min-width:160px}
.btn{border:none;border-radius:8px;padding:8px 14px;cursor:pointer;font-size:12px;font-weight:700;white-space:nowrap}
.btn-orange{background:#e87722;color:#fff;border:1px solid #e87722}
.btn-blue{background:#3b9dd2;color:#fff;border:1px solid #3b9dd2}
.btn-green{background:#1a7a4a;color:#fff;border:1px solid #1a7a4a}
.btn-red{background:#b83232;color:#fff;border:1px solid #b83232}
.btn-gray{background:#f4f8fb;color:#4a7fa0;border:1px solid #aed6ef}
.table-wrap{background:#fff;border-radius:12px;border:1px solid #aed6ef;overflow-x:auto;box-shadow:0 2px 12px rgba(26,95,138,.07)}
table{width:100%;border-collapse:collapse;font-size:12px;min-width:500px}
thead th{background:#e8f1f7;padding:8px 10px;text-align:left;font-weight:700;font-size:10px;color:#4a7fa0;border-bottom:1px solid #aed6ef;cursor:pointer;white-space:nowrap;text-transform:uppercase;letter-spacing:.04em}
tbody tr{border-bottom:1px solid #f4f8fb;cursor:pointer;transition:background .1s}
tbody tr:nth-child(even){background:#f4f8fb}
tbody tr:hover{background:#d4ecf9}
td{padding:7px 10px}
.pill{display:inline-block;font-size:10px;padding:2px 8px;border-radius:20px;font-weight:700;white-space:nowrap}
.pill-green{background:#d6f2e4;color:#1a7a4a}
.pill-red{background:#fce8e8;color:#b83232}
.pill-amber{background:#fff3cc;color:#916a00}
.pill-blue{background:#d4ecf9;color:#1a5f8a}
.pill-gray{background:#e8f1f7;color:#89b0c8}
.pill-orange{background:#fef0e3;color:#e87722}
.pag{display:flex;gap:8px;align-items:center;justify-content:flex-end;margin-top:10px;font-size:12px;color:#4a7fa0;flex-wrap:wrap}
.pag button{border:1px solid #aed6ef;border-radius:6px;padding:4px 10px;cursor:pointer;background:#fff;color:#3b9dd2;font-size:13px}
.pag button:disabled{opacity:.4;cursor:default}
.alert{margin-top:12px;border-radius:10px;padding:10px 14px;font-size:12px}
.alert-amber{background:#fff3cc;border:1px solid #f5c49a;color:#916a00}
.alert-green{background:#d6f2e4;border:1px solid #a0dcc0;color:#1a7a4a}
.alert-blue{background:#d4ecf9;border:1px solid #aed6ef;color:#1a5f8a}
/* MODAL */
.modal-bg{display:none;position:fixed;inset:0;background:rgba(10,35,60,.55);z-index:50;align-items:center;justify-content:center;padding:16px}
.modal-bg.open{display:flex}
.modal{background:#fff;border-radius:16px;width:100%;max-width:540px;max-height:90vh;overflow-y:auto;box-shadow:0 24px 64px rgba(0,0,0,.3)}
.modal-header{background:linear-gradient(135deg,#1a5f8a 0%,#2478a8 60%,#3b9dd2 100%);padding:16px 18px 12px;border-radius:16px 16px 0 0;display:flex;align-items:center;gap:12px}
.modal-avatar{width:44px;height:44px;border-radius:50%;background:rgba(255,255,255,.22);display:flex;align-items:center;justify-content:center;font-weight:800;font-size:14px;color:#fff;flex-shrink:0}
.modal-name{color:#fff;font-weight:700;font-size:14px;line-height:1.3}
.modal-sub{color:rgba(255,255,255,.75);font-size:11px;margin-top:2px}
.modal-close{border:1px solid rgba(255,255,255,.4);border-radius:8px;padding:5px 10px;cursor:pointer;background:rgba(255,255,255,.18);color:#fff;font-size:12px;margin-left:auto;flex-shrink:0}
.modal-body{padding:14px 18px 18px}
.modal-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px 16px;margin-top:12px}
.field-label{font-size:10px;color:#89b0c8;font-weight:600;text-transform:uppercase;letter-spacing:.05em;margin-bottom:2px}
.field-val{font-size:12.5px;color:#0d3550;word-break:break-word}
/* ADMIN PANEL */
.admin-panel{background:#fff;border-radius:12px;border:1px solid #aed6ef;padding:20px;margin-top:16px;box-shadow:0 2px 12px rgba(26,95,138,.07)}
.admin-panel h3{color:#1a5f8a;font-size:14px;margin-bottom:14px;padding-bottom:8px;border-bottom:2px solid #e87722}
.form-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.form-group{display:flex;flex-direction:column;gap:4px}
.form-group.full{grid-column:1/-1}
.form-group label{font-size:10.5px;color:#4a7fa0;font-weight:600;text-transform:uppercase;letter-spacing:.04em}
.form-group input,.form-group select,.form-group textarea{border:1px solid #aed6ef;border-radius:8px;padding:8px 10px;font-size:12px;color:#0d3550;outline:none;background:#fff;width:100%}
.form-group textarea{resize:vertical;min-height:60px}
.form-group input:focus,.form-group select:focus,.form-group textarea:focus{border-color:#3b9dd2}
/* ADMIN TABLE */
.admin-table-wrap{overflow-x:auto;margin-top:14px}
.admin-table{width:100%;border-collapse:collapse;font-size:11px;min-width:600px}
.admin-table th{background:#1a5f8a;color:#fff;padding:7px 10px;text-align:left;font-size:10px;text-transform:uppercase;letter-spacing:.04em}
.admin-table td{padding:6px 10px;border-bottom:1px solid #e8f1f7}
.admin-table tr:nth-child(even){background:#f4f8fb}
.admin-table tr:hover{background:#d4ecf9}
/* LOGIN */
.login-box{max-width:360px;margin:60px auto;background:#fff;border-radius:16px;padding:30px;border:1px solid #aed6ef;box-shadow:0 4px 20px rgba(26,95,138,.1);text-align:center}
.login-box h2{color:#1a5f8a;margin-bottom:6px;font-size:18px}
.login-box p{color:#89b0c8;font-size:12px;margin-bottom:20px}
.login-box input{width:100%;border:1px solid #aed6ef;border-radius:8px;padding:10px 14px;font-size:14px;outline:none;margin-bottom:10px;text-align:center;letter-spacing:4px}
/* LOADING */
.loading{text-align:center;padding:40px;color:#4a7fa0;font-size:14px}
.spinner{display:inline-block;width:32px;height:32px;border:3px solid #aed6ef;border-top-color:#1a5f8a;border-radius:50%;animation:spin .8s linear infinite;margin-bottom:12px}
@keyframes spin{to{transform:rotate(360deg)}}
/* PRINT VIEW */
#print-view{display:none;position:fixed;inset:0;background:#fff;z-index:100;overflow-y:auto;padding:20px}
/* RESPONSIVE */
@media(max-width:600px){
  .stats{gap:6px}
  .stat{min-width:calc(50% - 4px)}
  .header-title{font-size:12px}
  .tab{padding:8px 10px;font-size:11px}
  .form-grid{grid-template-columns:1fr}
  .form-group.full{grid-column:1}
  .modal-grid{grid-template-columns:1fr}
}
</style>
</head>
<body>

<!-- HEADER -->
<div class="header">
  <div class="header-top">
    <div class="logo-box">
      <svg viewBox="0 0 100 110" width="54" height="54" xmlns="http://www.w3.org/2000/svg">
        <circle cx="28" cy="8" r="6" fill="#f5a623"/>
        <circle cx="50" cy="5" r="6" fill="#f5a623"/>
        <circle cx="72" cy="8" r="6" fill="#f5a623"/>
        <rect x="14" y="20" width="72" height="12" rx="6" fill="#f5a623"/>
        <rect x="18" y="28" width="14" height="34" rx="7" fill="#f5a623"/>
        <rect x="43" y="28" width="14" height="34" rx="7" fill="#f5a623"/>
        <rect x="68" y="28" width="14" height="34" rx="7" fill="#f5a623"/>
        <text x="50" y="80" text-anchor="middle" font-family="serif" font-weight="bold" font-size="18" fill="#f5a623">FEMLAC</text>
        <line x1="8" y1="88" x2="92" y2="88" stroke="#f5a623" stroke-width="1.5"/>
      </svg>
    </div>
    <div>
      <div class="header-title">FEDERACIÓN MEXICANA DE LABORATORIOS PARA LA CONSTRUCCIÓN</div>
      <div class="header-sub" id="header-sub">Cargando datos...</div>
    </div>
  </div>
  <div class="tabs">
    <button class="tab active" onclick="setTab(0)">📋 Inscritos</button>
    <button class="tab" onclick="setTab(1)">💳 Pagos</button>
    <button class="tab" onclick="setTab(2)">🏅 Reconocimientos</button>
    <button class="tab" onclick="setTab(3)">🖼 Logo / Web</button>
    <button class="tab" onclick="setTab(4)">⚙️ Administrar</button>
  </div>
</div>

<div class="main">
  <div id="loading" class="loading"><div class="spinner"></div><br>Cargando datos desde Google Sheets…</div>
  <div id="app" style="display:none">
    <div id="stats-area"></div>
    <div id="banner-area"></div>
    <div class="filters" id="filters-area">
      <input type="text" id="search" placeholder="🔍 Buscar nombre, estado o ciudad…" oninput="applyFilters()">
      <select id="fEst" onchange="applyFilters()"><option value="">Todos los estados</option></select>
      <select id="fPago" onchange="applyFilters()" style="display:none">
        <option value="">Todos los pagos</option>
        <option value="PAGADO">Pagados</option>
        <option value="ABONO">Con abono</option>
      </select>
      <button class="btn btn-blue" onclick="loadData()">⟳ Actualizar</button>
      <button class="btn btn-orange" onclick="printResults()">🖨️ Imprimir</button>
    </div>
    <div class="table-wrap" id="table-area">
      <table><thead id="thead"></thead><tbody id="tbody"></tbody></table>
    </div>
    <div class="pag" id="pag"></div>
    <div id="alert-area"></div>
    <!-- ADMIN TAB -->
    <div id="admin-area" style="display:none"></div>
  </div>
</div>

<!-- DETAIL MODAL -->
<div class="modal-bg" id="modal" onclick="closeModal(event)">
  <div class="modal" onclick="event.stopPropagation()">
    <div class="modal-header">
      <div class="modal-avatar" id="m-avatar"></div>
      <div><div class="modal-name" id="m-name"></div><div class="modal-sub" id="m-sub"></div></div>
      <button class="modal-close" onclick="document.getElementById('modal').classList.remove('open')">✕</button>
    </div>
    <div class="modal-body" id="m-body"></div>
  </div>
</div>

<!-- EDIT MODAL -->
<div class="modal-bg" id="edit-modal" onclick="closeEditModal(event)">
  <div class="modal" onclick="event.stopPropagation()" style="max-width:580px">
    <div class="modal-header">
      <div><div class="modal-name" id="edit-title">Editar laboratorio</div></div>
      <button class="modal-close" onclick="closeEditModal()">✕</button>
    </div>
    <div class="modal-body" id="edit-body"></div>
  </div>
</div>

<!-- PRINT VIEW -->
<div id="print-view">
  <div style="margin-bottom:14px;display:flex;gap:10px;flex-wrap:wrap">
    <button onclick="document.getElementById('print-view').style.display='none'" class="btn btn-blue">← Volver</button>
    <button onclick="window.print()" class="btn btn-orange">🖨️ Imprimir / PDF</button>
    <span style="font-size:11px;color:#89b0c8;align-self:center">También Ctrl+P</span>
  </div>
  <div id="print-content"></div>
</div>

<script>
/* ════════════════════════════════════════════
   URLS CSV (live from Google Sheets)
════════════════════════════════════════════ */
const URLS = {
  inscritos:'https://docs.google.com/spreadsheets/d/e/2PACX-1vRrn0tDIZfQhJ61iuTXt8edkH1UCvZBvHVtSad4ZkzWZjhZzxgobZYbq44I7nR0Yx3tImSUJGUodxM3/pub?gid=1482124389&single=true&output=csv',
  pagos:'https://docs.google.com/spreadsheets/d/e/2PACX-1vRrn0tDIZfQhJ61iuTXt8edkH1UCvZBvHVtSad4ZkzWZjhZzxgobZYbq44I7nR0Yx3tImSUJGUodxM3/pub?gid=1054439263&single=true&output=csv',
  reconocimientos:'https://docs.google.com/spreadsheets/d/e/2PACX-1vRrn0tDIZfQhJ61iuTXt8edkH1UCvZBvHVtSad4ZkzWZjhZzxgobZYbq44I7nR0Yx3tImSUJGUodxM3/pub?gid=472740108&single=true&output=csv',
  logos:'https://docs.google.com/spreadsheets/d/e/2PACX-1vRrn0tDIZfQhJ61iuTXt8edkH1UCvZBvHVtSad4ZkzWZjhZzxgobZYbq44I7nR0Yx3tImSUJGUodxM3/pub?gid=1486724500&single=true&output=csv',
};
const CUOTA = 7500;
const ADMIN_PIN = '2026';

/* ════════════════════════════════════════════
   STATE
════════════════════════════════════════════ */
let currentTab = 0;
let currentPage = 1;
const PER = 15;
let sortKey = 'num';
let sortDir = 1;
let filtered = [];
let adminUnlocked = false;

// Data from Sheets
let sheetInscritos = [];
let sheetPagos = {};      // email → {monto, ficha, lab}
let sheetReconoc = new Set();
let sheetLogos = {};      // num → {logo, web}

// Local overrides (stored in localStorage)
function getLocal(key, def) {
  try { const v = localStorage.getItem(key); return v ? JSON.parse(v) : def; } catch(e){ return def; }
}
function setLocal(key, val) {
  try { localStorage.setItem(key, JSON.stringify(val)); } catch(e){}
}

// localNums: {email → num} — auto-assigned numbers
let localNums = getLocal('femlac_nums', {});
// localManual: array of manually added labs
let localManual = getLocal('femlac_manual', []);
// localDeleted: set of emails deleted
let localDeleted = getLocal('femlac_deleted', []);
// localEdits: {email → overrides}
let localEdits = getLocal('femlac_edits', {});

/* ════════════════════════════════════════════
   CSV PARSER
════════════════════════════════════════════ */
function parseCSV(text) {
  const lines = text.trim().split('\n');
  const headers = splitLine(lines[0]);
  return lines.slice(1).map(l => {
    const v = splitLine(l);
    const o = {};
    headers.forEach((h,i) => o[h.trim()] = (v[i]||'').trim());
    return o;
  }).filter(r => Object.values(r).some(v=>v));
}
function splitLine(line) {
  const res=[]; let cur=''; let q=false;
  for(let i=0;i<line.length;i++){
    const c=line[i];
    if(c==='"'){q=!q;continue;}
    if(c===','&&!q){res.push(cur);cur='';continue;}
    cur+=c;
  }
  res.push(cur);
  return res;
}

/* ════════════════════════════════════════════
   LOAD DATA
════════════════════════════════════════════ */
async function loadData() {
  document.getElementById('loading').style.display='block';
  document.getElementById('app').style.display='none';
  try {
    const [r1,r2,r3,r4] = await Promise.all([
      fetch(URLS.inscritos+'&t='+Date.now()).then(r=>r.text()),
      fetch(URLS.pagos+'&t='+Date.now()).then(r=>r.text()),
      fetch(URLS.reconocimientos+'&t='+Date.now()).then(r=>r.text()),
      fetch(URLS.logos+'&t='+Date.now()).then(r=>r.text()),
    ]);

    // INSCRIPCION
    const ins = parseCSV(r1);
    sheetInscritos = ins.map(row => ({
      num: row['N SOCIO'] ? parseInt(row['N SOCIO']) : null,
      nombre: row['NOMBRE COMERCIAL DEL LABORATORIO'] || row['NOMBRE O RAZÓN SOCIAL'] || '',
      razon: row['NOMBRE O RAZÓN SOCIAL'] || '',
      email: (row['Dirección de correo electrónico']||'').toLowerCase().trim(),
      estado: row['ESTADO']||'',
      ciudad: row['CIUDAD']||'',
      empleados: row['NUMERO DE EMPLEADOS']||'',
      acreditado: row['ESTA ACREDITADO SEÑALAR AREAS']||'',
      rep: row['NOMBRE REPRESENTANTE LEGAL']||'',
      tec: row['NOMBRE RESPONSABLE TÉCNICO']||'',
      tel: row['TELEFONOS OFICINA 1']||'',
      cel: row['CELULAR']||'',
      mapa: row['LOCALIZACION DEL LABORATORIO']||'',
      fuente: 'sheets',
    }));

    // PAGOS
    sheetPagos = {};
    parseCSV(r2).forEach(row => {
      const email = (row['Dirección de correo electrónico']||'').toLowerCase().trim();
      const ficha = row['ANEXAR FICHA DE DEPOSTIO']||'';
      const nota = Object.values(row).join(' ');
      let monto = 7500;
      if(nota.includes('PAGO 7000')) monto=7000;
      else if(nota.includes('PAGO 3000')) monto=3000;
      else if(!ficha) monto=0;
      if(email && ficha) sheetPagos[email]={monto,ficha,lab:row['CONFIRMACION NOMBRE COMERCIAL DEL LABORATORIO']||''};
    });

    // RECONOCIMIENTOS
    sheetReconoc = new Set();
    parseCSV(r3).forEach(row => {
      const n = parseInt(row['NO SOCIO']);
      if(!isNaN(n) && (row['CONSTANCIA DIGITAL SOCIO']||'').trim().toUpperCase()==='TRUE') sheetReconoc.add(n);
    });

    // LOGOS
    sheetLogos = {};
    parseCSV(r4).forEach(row => {
      const n = parseInt(row['NUMERO DE SOCIO']);
      if(!isNaN(n)) sheetLogos[n]={logo:row['LOGOTIPO']||'',web:row['DIRECCION DE PAGINA WEB']||''};
    });

    // Auto-assign numbers to labs that paid and don't have one
    autoAssignNumbers();

    buildEstados();
    document.getElementById('loading').style.display='none';
    document.getElementById('app').style.display='block';
    const t = new Date().toLocaleTimeString('es-MX',{hour:'2-digit',minute:'2-digit'});
    document.getElementById('header-sub').textContent=`Directorio de Socios 2026 · ${getAllLabs().length} laboratorios · Actualizado ${t}`;
    applyFilters();
  } catch(e) {
    document.getElementById('loading').innerHTML=`<div style="color:#b83232;text-align:center;padding:40px">❌ Error al cargar datos.<br><small>${e.message}</small><br><br><button onclick="loadData()" class="btn btn-blue" style="margin-top:10px">Reintentar</button></div>`;
  }
}

/* ════════════════════════════════════════════
   AUTO-ASSIGN NUMBERS
════════════════════════════════════════════ */
function autoAssignNumbers() {
  // Collect all used numbers (from sheets + local)
  const usedNums = new Set();
  sheetInscritos.forEach(l => { if(l.num) usedNums.add(l.num); });
  localManual.forEach(l => { if(l.num) usedNums.add(l.num); });
  Object.values(localNums).forEach(n => { if(n) usedNums.add(n); });

  // For each lab with payment but no number
  getAllLabs().forEach(l => {
    if(!getNum(l) && hasPago(l)) {
      // assign next available number
      let next = 1;
      while(usedNums.has(next)) next++;
      localNums[l.email] = next;
      usedNums.add(next);
    }
  });
  setLocal('femlac_nums', localNums);
}

/* ════════════════════════════════════════════
   HELPERS
════════════════════════════════════════════ */
function getAllLabs() {
  const deleted = new Set(localDeleted);
  const fromSheets = sheetInscritos
    .filter(l => !deleted.has(l.email))
    .map(l => {
      const edits = localEdits[l.email] || {};
      return {...l, ...edits};
    });
  return [...fromSheets, ...localManual.filter(l => !deleted.has(l.email))];
}

function getNum(lab) {
  if(lab.num) return lab.num;
  return localNums[lab.email] || null;
}

function hasPago(lab) {
  return !!sheetPagos[(lab.email||'').toLowerCase()];
}

function getPago(lab) {
  const email = (lab.email||'').toLowerCase();
  const p = sheetPagos[email] || null;
  if(!p) return {monto:0,ficha:'',adeudo:CUOTA,status:'SIN PAGO'};
  if(p.monto>=CUOTA) return {...p,adeudo:0,status:'PAGADO'};
  return {...p,adeudo:CUOTA-p.monto,status:`ABONO $${p.monto.toLocaleString()}`};
}

function getRecon(lab) {
  const n = getNum(lab);
  return n ? sheetReconoc.has(n) : false;
}

function getLogo(lab) {
  const n = getNum(lab);
  return n ? sheetLogos[n] : null;
}

function pill(text,cls) { return `<span class="pill ${cls}">${text}</span>`; }

function pagoChip(lab) {
  const p = getPago(lab);
  if(p.status==='PAGADO') return pill('PAGADO','pill-green');
  if(p.status.startsWith('ABONO')) return pill(p.status,'pill-amber');
  return pill('SIN PAGO','pill-red');
}

function initials(s) {
  return (s||'').split(' ').slice(0,2).map(w=>w[0]||'').join('').toUpperCase();
}

/* ════════════════════════════════════════════
   BUILD ESTADOS
════════════════════════════════════════════ */
function buildEstados() {
  const sel = document.getElementById('fEst');
  const estados = [...new Set(getAllLabs().map(l=>l.estado).filter(Boolean))].sort();
  sel.innerHTML = '<option value="">Todos los estados</option>'+
    estados.map(e=>`<option value="${e}">${e}</option>`).join('');
}

/* ════════════════════════════════════════════
   TABS
════════════════════════════════════════════ */
function setTab(i) {
  currentTab = i;
  currentPage = 1;
  document.querySelectorAll('.tab').forEach((t,idx)=>t.classList.toggle('active',idx===i));
  document.getElementById('fPago').style.display = i===1?'inline-block':'none';
  document.getElementById('filters-area').style.display = i===4?'none':'flex';
  document.getElementById('table-area').style.display = i===4?'none':'block';
  document.getElementById('pag').style.display = i===4?'none':'flex';

  if(i===4) {
    document.getElementById('admin-area').style.display='block';
    renderAdmin();
  } else {
    document.getElementById('admin-area').style.display='none';
    applyFilters();
  }
}

/* ════════════════════════════════════════════
   FILTERS & RENDER
════════════════════════════════════════════ */
function applyFilters() {
  const q   = document.getElementById('search').value.toLowerCase();
  const est = document.getElementById('fEst').value;
  const pag = document.getElementById('fPago').value;
  const all = getAllLabs();

  let list = all.filter(l => {
    if(q && !l.nombre.toLowerCase().includes(q) && !(l.estado||'').toLowerCase().includes(q) && !(l.ciudad||'').toLowerCase().includes(q)) return false;
    if(est && l.estado!==est) return false;

    // Tab-specific filters
    if(currentTab===1) {
      if(!hasPago(l)) return false; // Only labs that paid
      if(pag==='PAGADO' && getPago(l).status!=='PAGADO') return false;
      if(pag==='ABONO' && !getPago(l).status.startsWith('ABONO')) return false;
    }
    if(currentTab===2) { if(!getRecon(l)) return false; } // Only recognized
    if(currentTab===3) { const ld=getLogo(l); if(!ld||(!ld.logo&&!ld.web)) return false; } // Only with logo/web
    return true;
  });

  list.sort((a,b)=>{
    const na=getNum(a), nb=getNum(b);
    if(sortKey==='num'){
      if(na===null&&nb===null) return 0;
      if(na===null) return 1; if(nb===null) return -1;
      return (na-nb)*sortDir;
    }
    return String(a[sortKey]||'').localeCompare(String(b[sortKey]||''),'es')*sortDir;
  });

  filtered = list;
  currentPage = 1;
  renderStats();
  renderTable();
  renderAlerts();
}

function srt(k){
  if(sortKey===k) sortDir*=-1; else{sortKey=k;sortDir=1;}
  applyFilters();
}
function arr(k){ return sortKey===k?(sortDir===1?' ↑':' ↓'):''; }

/* ════════════════════════════════════════════
   STATS — per tab
════════════════════════════════════════════ */
function renderStats() {
  const all = getAllLabs();
  let items = [];

  if(currentTab===0) {
    const conNum = all.filter(l=>getNum(l)).length;
    const sinNum = all.filter(l=>!getNum(l)).length;
    const acred  = all.filter(l=>l.acreditado).length;
    const estados= new Set(all.map(l=>l.estado).filter(Boolean)).size;
    items = [
      {l:'Total inscritos',  v:all.length,  c:'#3b9dd2', s:'laboratorios'},
      {l:'Con N° socio',     v:conNum,       c:'#1a5f8a', s:'asignados'},
      {l:'Sin N° socio',     v:sinNum,       c:'#89b0c8', s:'pendientes'},
      {l:'Acreditados',      v:acred,        c:'#e87722', s:'laboratorios'},
      {l:'Estados',          v:estados,      c:'#2478a8', s:'representados'},
    ];
  } else if(currentTab===1) {
    const pagados = all.filter(l=>getPago(l).status==='PAGADO').length;
    const abonos  = all.filter(l=>getPago(l).status.startsWith('ABONO')).length;
    const adeudoT = all.reduce((s,l)=>s+getPago(l).adeudo,0);
    const conPago = all.filter(l=>hasPago(l)).length;
    items = [
      {l:'Con pago registrado', v:conPago,  c:'#1a5f8a', s:'laboratorios'},
      {l:'Pagados completo',    v:pagados,  c:'#1a7a4a', s:'$7,500 MXN'},
      {l:'Con abono',           v:abonos,   c:'#916a00', s:'pago parcial'},
      {l:'Adeudo total',        v:'$'+adeudoT.toLocaleString(), c:'#b83232', s:'MXN pendiente'},
    ];
  } else if(currentTab===2) {
    const totalRecon = sheetReconoc.size;
    const conPago    = [...sheetReconoc].filter(n=>{
      const lab = all.find(l=>getNum(l)===n);
      return lab && getPago(lab).status==='PAGADO';
    }).length;
    items = [
      {l:'Reconocimientos',    v:totalRecon,              c:'#1a5f8a', s:'generados y enviados'},
      {l:'Con pago confirmado',v:conPago,                 c:'#1a7a4a', s:'coincidencia'},
      {l:'Sin pago',           v:totalRecon-conPago,      c:'#b83232', s:'verificar'},
    ];
  } else if(currentTab===3) {
    const conLogo = Object.values(sheetLogos).filter(l=>l.logo).length;
    const conWeb  = Object.values(sheetLogos).filter(l=>l.web).length;
    const ambos   = Object.values(sheetLogos).filter(l=>l.logo&&l.web).length;
    items = [
      {l:'Con logo',          v:conLogo, c:'#1a5f8a', s:'entregados'},
      {l:'Con página web',    v:conWeb,  c:'#e87722', s:'registradas'},
      {l:'Logo + Web',        v:ambos,   c:'#1a7a4a', s:'completos'},
    ];
  }

  document.getElementById('stats-area').innerHTML = items.length
    ? `<div class="stats">${items.map(s=>`<div class="stat"><div class="stat-label">${s.l}</div><div class="stat-value" style="color:${s.c}">${s.v}</div><div class="stat-sub">${s.s}</div></div>`).join('')}</div>`
    : '';

  // Banners
  let banners = '';
  if(currentTab===1) {
    const adeudoT = all.reduce((s,l)=>s+getPago(l).adeudo,0);
    const sinNumConPago = all.filter(l=>!getNum(l)&&hasPago(l));
    if(adeudoT>0) banners+=`<div class="banner">💰 <span><b>Adeudo total: $${adeudoT.toLocaleString()} MXN</b> pendiente de cobro.</span></div>`;
    if(sinNumConPago.length) banners+=`<div class="banner" style="background:#d4ecf9;border-color:#aed6ef;color:#1a5f8a">ℹ <span><b>${sinNumConPago.length} laboratorio(s) pagaron y se les asignó número automáticamente.</b> Revisa la pestaña Administrar.</span></div>`;
  }
  document.getElementById('banner-area').innerHTML = banners;
}

/* ════════════════════════════════════════════
   TABLE RENDER
════════════════════════════════════════════ */
function renderTable() {
  const start = (currentPage-1)*PER;
  const page  = filtered.slice(start,start+PER);

  // Headers
  let heads = `<th onclick="srt('num')">#${arr('num')}</th>
    <th onclick="srt('nombre')">Laboratorio${arr('nombre')}</th>
    <th onclick="srt('estado')">Estado${arr('estado')}</th>
    <th>Personal</th>`;
  if(currentTab===0) heads+=`<th>Acreditación</th>`;
  if(currentTab===1) heads+=`<th>Pago</th><th>Adeudo</th><th>Ficha</th>`;
  if(currentTab===2) heads+=`<th>Reconocimiento</th><th>Pago OK</th>`;
  if(currentTab===3) heads+=`<th>Logo</th><th>Página web</th>`;
  document.getElementById('thead').innerHTML=`<tr>${heads}</tr>`;

  if(!page.length){
    document.getElementById('tbody').innerHTML=`<tr><td colspan="8" style="padding:2rem;text-align:center;color:#89b0c8">Sin resultados.</td></tr>`;
  } else {
    document.getElementById('tbody').innerHTML=page.map((l,i)=>{
      const num   = getNum(l);
      const pago  = getPago(l);
      const recon = getRecon(l);
      const logoD = getLogo(l);
      const autoN = !l.num && localNums[l.email] ? '🔢' : '';

      let extra='';
      if(currentTab===0) extra=`<td>${l.acreditado?pill('Acreditado','pill-blue'):pill('No','pill-gray')}</td>`;
      if(currentTab===1) extra=`
        <td>${pagoChip(l)}</td>
        <td style="font-weight:${pago.adeudo>0?700:400};color:${pago.adeudo>0?'#b83232':'#89b0c8'}">${pago.adeudo>0?'$'+pago.adeudo.toLocaleString():'—'}</td>
        <td>${pago.ficha?`<a href="${pago.ficha}" target="_blank" onclick="event.stopPropagation()" style="font-size:10px;background:#d4ecf9;color:#3b9dd2;padding:2px 8px;border-radius:20px;font-weight:700;text-decoration:none">Ver 📄</a>`:'<span style="color:#89b0c8;font-size:10px">—</span>'}</td>`;
      if(currentTab===2) extra=`
        <td>${recon?pill('✓ Enviado','pill-green'):pill('Pendiente','pill-red')}</td>
        <td>${pago.status==='PAGADO'?pill('✓','pill-green'):pill('✗','pill-red')}</td>`;
      if(currentTab===3) extra=`
        <td>${logoD&&logoD.logo?`<a href="${logoD.logo}" target="_blank" onclick="event.stopPropagation()" style="font-size:10px;background:#d6f2e4;color:#1a7a4a;padding:2px 8px;border-radius:20px;font-weight:700;text-decoration:none">Ver 🖼</a>`:pill('—','pill-gray')}</td>
        <td style="font-size:11px;max-width:160px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap">${logoD&&logoD.web?`<a href="${logoD.web.startsWith('http')?logoD.web:'https://'+logoD.web}" target="_blank" onclick="event.stopPropagation()" style="color:#3b9dd2;text-decoration:none">${logoD.web}</a>`:'<span style="color:#89b0c8">—</span>'}</td>`;

      return `<tr onclick="openModal('${l.email}')">
        <td style="color:#89b0c8;font-weight:700;font-size:11px">${num||'—'} ${autoN}</td>
        <td style="font-weight:600;max-width:200px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap" title="${l.nombre}">${l.nombre}</td>
        <td style="color:#4a7fa0;font-size:11.5px">${l.estado}</td>
        <td style="color:#89b0c8;font-size:11px">${l.empleados||'—'}</td>
        ${extra}
      </tr>`;
    }).join('');
  }

  // Pagination
  const pages = Math.ceil(filtered.length/PER);
  const pag = document.getElementById('pag');
  if(pages<=1){pag.innerHTML='';return;}
  pag.innerHTML=`<span>${filtered.length} registros</span>
    <button onclick="changePage(-1)" ${currentPage===1?'disabled':''}>‹</button>
    <span>Página ${currentPage} de ${pages}</span>
    <button onclick="changePage(1)" ${currentPage===pages?'disabled':''}>›</button>`;
}

function changePage(d){
  const pages=Math.ceil(filtered.length/PER);
  currentPage=Math.max(1,Math.min(pages,currentPage+d));
  renderTable();
}

/* ════════════════════════════════════════════
   ALERTS
════════════════════════════════════════════ */
function renderAlerts(){
  let html='';
  const all=getAllLabs();
  if(currentTab===2){
    const pagadosNums=new Set(all.filter(l=>getPago(l).status==='PAGADO').map(l=>getNum(l)).filter(Boolean));
    const sinPago=[...sheetReconoc].filter(n=>!pagadosNums.has(n));
    const sinRecon=all.filter(l=>getNum(l)&&getPago(l).status==='PAGADO'&&!sheetReconoc.has(getNum(l)));
    if(!sinPago.length&&!sinRecon.length){
      html=`<div class="alert alert-green">✅ Los ${sheetReconoc.size} reconocimientos coinciden con los pagos confirmados.</div>`;
    } else {
      let msg='<b>⚠ Verificar coincidencias:</b>';
      if(sinPago.length) msg+=`<div style="margin-top:4px">Reconocimiento sin pago confirmado: números ${sinPago.join(', ')}</div>`;
      if(sinRecon.length) msg+=`<div style="margin-top:4px">Pagados sin reconocimiento: ${sinRecon.map(l=>l.nombre).join(', ')}</div>`;
      html=`<div class="alert alert-amber">${msg}</div>`;
    }
  }
  document.getElementById('alert-area').innerHTML=html;
}

/* ════════════════════════════════════════════
   DETAIL MODAL
════════════════════════════════════════════ */
function openModal(email){
  const l=getAllLabs().find(x=>x.email===email);
  if(!l) return;
  const num=getNum(l), pago=getPago(l), recon=getRecon(l), logoD=getLogo(l);
  document.getElementById('m-avatar').textContent=initials(l.nombre);
  document.getElementById('m-name').textContent=l.nombre;
  document.getElementById('m-sub').textContent=`${num?'Socio N° '+num+(localNums[l.email]?' (auto)':''):'Sin número'} · ${l.estado} · ${l.ciudad}`;

  let b=`<div style="display:flex;gap:6px;flex-wrap:wrap;margin-bottom:12px">`;
  if(pago.status==='PAGADO') b+=pill('PAGADO','pill-green');
  else if(pago.status.startsWith('ABONO')) b+=pill(pago.status,'pill-amber');
  else b+=pill('SIN PAGO','pill-red');
  if(pago.adeudo>0) b+=pill('Adeudo $'+pago.adeudo.toLocaleString(),'pill-red');
  b+=pill(recon?'Reconocimiento enviado':'Sin reconocimiento',recon?'pill-green':'pill-red');
  b+=pill(logoD?'Logo entregado':'Sin logo',logoD?'pill-green':'pill-orange');
  if(l.acreditado) b+=pill('Acreditado','pill-blue');
  if(!num) b+=pill('Sin N° socio','pill-amber');
  b+=`</div>`;

  if(l.acreditado) b+=`<div style="background:#d4ecf9;border:1px solid #aed6ef;border-radius:8px;padding:8px 12px;margin-bottom:10px;font-size:12px;color:#1a5f8a"><b>Áreas acreditadas:</b> ${l.acreditado}</div>`;
  if(pago.ficha) b+=`<div style="background:#d6f2e4;border:1px solid #a0dcc0;border-radius:8px;padding:8px 12px;margin-bottom:10px;font-size:12px;display:flex;align-items:center;gap:8px">📄 <span style="color:#1a7a4a"><b>Ficha:</b> <a href="${pago.ficha}" target="_blank" style="color:#3b9dd2">Ver en Drive</a> · <b>$${pago.monto.toLocaleString()}</b></span></div>`;
  if(logoD&&(logoD.logo||logoD.web)) b+=`<div style="background:#f4f8fb;border:1px solid #aed6ef;border-radius:8px;padding:8px 12px;margin-bottom:10px;font-size:12px">${logoD.logo?`<a href="${logoD.logo}" target="_blank" style="color:#3b9dd2;margin-right:12px">🖼 Logotipo</a>`:''}${logoD.web?`<a href="${logoD.web.startsWith('http')?logoD.web:'https://'+logoD.web}" target="_blank" style="color:#3b9dd2">🌐 ${logoD.web}</a>`:''}</div>`;

  b+=`<div class="modal-grid">`;
  [['Rep. Legal',l.rep],['Resp. Técnico',l.tec],['Ciudad',l.ciudad],['Estado',l.estado],
   ['Personal',l.empleados||'—'],['Teléfono',l.tel||l.cel||'—'],['Correo',l.email],
   ['Ubicación',l.mapa?`<a href="${l.mapa}" target="_blank" style="color:#3b9dd2">Ver mapa 📍</a>`:'—']
  ].forEach(([label,val])=>{
    b+=`<div><div class="field-label">${label}</div><div class="field-val">${val||'—'}</div></div>`;
  });
  b+=`</div>`;
  document.getElementById('m-body').innerHTML=b;
  document.getElementById('modal').classList.add('open');
}
function closeModal(e){ if(e.target===document.getElementById('modal')) document.getElementById('modal').classList.remove('open'); }
function closeEditModal(e){ if(!e||e.target===document.getElementById('edit-modal')) document.getElementById('edit-modal').classList.remove('open'); }

/* ════════════════════════════════════════════
   ADMIN PANEL
════════════════════════════════════════════ */
function renderAdmin(){
  const el=document.getElementById('admin-area');
  if(!adminUnlocked){
    el.innerHTML=`<div class="login-box">
      <div style="margin-bottom:12px"><svg viewBox="0 0 100 110" width="48" height="52" xmlns="http://www.w3.org/2000/svg">
        <circle cx="28" cy="8" r="6" fill="#f5a623"/><circle cx="50" cy="5" r="6" fill="#f5a623"/><circle cx="72" cy="8" r="6" fill="#f5a623"/>
        <rect x="14" y="20" width="72" height="12" rx="6" fill="#f5a623"/>
        <rect x="18" y="28" width="14" height="34" rx="7" fill="#f5a623"/>
        <rect x="43" y="28" width="14" height="34" rx="7" fill="#f5a623"/>
        <rect x="68" y="28" width="14" height="34" rx="7" fill="#f5a623"/>
        <text x="50" y="80" text-anchor="middle" font-family="serif" font-weight="bold" font-size="18" fill="#f5a623">FEMLAC</text>
      </svg></div>
      <h2>Panel de Administración</h2>
      <p>Ingresa tu PIN para continuar</p>
      <input type="password" id="pin-input" placeholder="••••" maxlength="10" onkeydown="if(event.key==='Enter')checkPin()">
      <button onclick="checkPin()" class="btn btn-blue" style="width:100%">Entrar</button>
      <div id="pin-error" style="color:#b83232;font-size:11px;margin-top:8px"></div>
    </div>`;
    return;
  }
  renderAdminContent();
}

function checkPin(){
  const v=document.getElementById('pin-input').value;
  if(v===ADMIN_PIN){ adminUnlocked=true; renderAdminContent(); }
  else document.getElementById('pin-error').textContent='PIN incorrecto';
}

function renderAdminContent(){
  const all=getAllLabs();
  const deleted=new Set(localDeleted);
  const el=document.getElementById('admin-area');
  el.innerHTML=`
  <div class="admin-panel">
    <h3>⚙️ Panel de Administración FEMLAC 2026</h3>
    <!-- ADD NEW -->
    <div style="margin-bottom:20px">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:12px">
        <b style="color:#1a5f8a;font-size:13px">➕ Agregar laboratorio manual</b>
      </div>
      <div class="form-grid" id="new-form">
        <div class="form-group"><label>Nombre comercial *</label><input type="text" id="nf-nombre" placeholder="Nombre del laboratorio"></div>
        <div class="form-group"><label>Correo electrónico *</label><input type="email" id="nf-email" placeholder="correo@ejemplo.com"></div>
        <div class="form-group"><label>Estado *</label><input type="text" id="nf-estado" placeholder="Estado"></div>
        <div class="form-group"><label>Ciudad</label><input type="text" id="nf-ciudad" placeholder="Ciudad"></div>
        <div class="form-group"><label>Representante legal</label><input type="text" id="nf-rep" placeholder="Nombre completo"></div>
        <div class="form-group"><label>Responsable técnico</label><input type="text" id="nf-tec" placeholder="Nombre completo"></div>
        <div class="form-group"><label>Teléfono</label><input type="text" id="nf-tel" placeholder="10 dígitos"></div>
        <div class="form-group"><label>Personal</label>
          <select id="nf-emp">
            <option value="">Seleccionar</option>
            <option>DE 1 A 10</option><option>DE 11 A 50</option>
            <option>DE 51 A 250</option><option>+ DE 251</option>
          </select>
        </div>
        <div class="form-group full"><label>Áreas acreditadas</label><input type="text" id="nf-acred" placeholder="CONCRETO, TERRACERIAS, GEOTECNIA..."></div>
      </div>
      <div style="margin-top:10px;display:flex;gap:8px">
        <button onclick="addManual()" class="btn btn-green">✓ Agregar laboratorio</button>
        <button onclick="clearNewForm()" class="btn btn-gray">Limpiar</button>
      </div>
      <div id="add-msg" style="margin-top:8px;font-size:12px"></div>
    </div>

    <!-- NUMBERS ASSIGNED -->
    <div style="margin-bottom:20px">
      <b style="color:#1a5f8a;font-size:13px">🔢 Números asignados automáticamente (${Object.keys(localNums).length})</b>
      <div style="margin-top:8px;font-size:11px;color:#4a7fa0">
        ${Object.keys(localNums).length===0?'<i>Ninguno aún</i>':
          Object.entries(localNums).map(([email,num])=>{
            const lab=all.find(l=>l.email===email);
            return `<span style="display:inline-block;background:#d4ecf9;border-radius:20px;padding:2px 10px;margin:2px;font-weight:700">
              N°${num} — ${lab?lab.nombre:email}
            </span>`;
          }).join('')}
      </div>
    </div>

    <!-- ALL LABS TABLE -->
    <div>
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:10px">
        <b style="color:#1a5f8a;font-size:13px">📋 Todos los laboratorios (${all.length})</b>
        <input type="text" id="admin-search" placeholder="Buscar…" oninput="renderAdminTable()" style="border:1px solid #aed6ef;border-radius:8px;padding:6px 10px;font-size:12px;width:200px">
      </div>
      <div class="admin-table-wrap" id="admin-table-wrap"></div>
    </div>
  </div>`;
  renderAdminTable();
}

function renderAdminTable(){
  const q=(document.getElementById('admin-search')||{value:''}).value.toLowerCase();
  const all=getAllLabs();
  const labs=all.filter(l=>!q||l.nombre.toLowerCase().includes(q)||l.email.includes(q));
  const wrap=document.getElementById('admin-table-wrap');
  if(!wrap) return;
  wrap.innerHTML=`<table class="admin-table">
    <thead><tr>
      <th>#</th><th>Laboratorio</th><th>Correo</th><th>Estado</th><th>Pago</th><th>Fuente</th><th>Acciones</th>
    </tr></thead>
    <tbody>${labs.map(l=>{
      const num=getNum(l);
      const pago=getPago(l);
      const fuente=l.fuente==='manual'?'<span style="background:#d6f2e4;color:#1a7a4a;padding:1px 6px;border-radius:10px;font-size:9px">MANUAL</span>':'<span style="background:#d4ecf9;color:#1a5f8a;padding:1px 6px;border-radius:10px;font-size:9px">SHEETS</span>';
      const numDisp=num?(localNums[l.email]?`${num} 🔢`:num):'—';
      return `<tr>
        <td style="font-weight:700;color:#4a7fa0">${numDisp}</td>
        <td style="font-weight:600;max-width:180px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap">${l.nombre}</td>
        <td style="font-size:10px;color:#89b0c8;max-width:160px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap">${l.email}</td>
        <td>${l.estado||'—'}</td>
        <td style="font-size:10px;font-weight:700;color:${pago.status==='PAGADO'?'#1a7a4a':pago.status.startsWith('ABONO')?'#916a00':'#b83232'}">${pago.status}</td>
        <td>${fuente}</td>
        <td>
          <button onclick="editLab('${l.email}')" class="btn btn-blue" style="padding:3px 8px;font-size:10px;margin-right:4px">✏️ Editar</button>
          <button onclick="deleteLab('${l.email}','${l.nombre.replace(/'/g,"\\'")}','${l.fuente}')" class="btn btn-red" style="padding:3px 8px;font-size:10px">🗑 Eliminar</button>
        </td>
      </tr>`;
    }).join('')}</tbody>
  </table>`;
}

function addManual(){
  const nombre=document.getElementById('nf-nombre').value.trim();
  const email=document.getElementById('nf-email').value.trim().toLowerCase();
  const estado=document.getElementById('nf-estado').value.trim();
  const msg=document.getElementById('add-msg');
  if(!nombre||!email||!estado){msg.innerHTML='<span style="color:#b83232">⚠ Nombre, correo y estado son obligatorios.</span>';return;}
  if(getAllLabs().find(l=>l.email===email)){msg.innerHTML='<span style="color:#b83232">⚠ Ya existe un laboratorio con ese correo.</span>';return;}
  const newLab={
    num:null, nombre, email, estado,
    ciudad:document.getElementById('nf-ciudad').value.trim(),
    rep:document.getElementById('nf-rep').value.trim(),
    tec:document.getElementById('nf-tec').value.trim(),
    tel:document.getElementById('nf-tel').value.trim(),
    empleados:document.getElementById('nf-emp').value,
    acreditado:document.getElementById('nf-acred').value.trim(),
    fuente:'manual', mapa:'', razon:'',
  };
  localManual.push(newLab);
  setLocal('femlac_manual',localManual);
  autoAssignNumbers();
  msg.innerHTML='<span style="color:#1a7a4a">✓ Laboratorio agregado correctamente.</span>';
  clearNewForm();
  renderAdminTable();
  applyFilters();
}

function clearNewForm(){
  ['nf-nombre','nf-email','nf-estado','nf-ciudad','nf-rep','nf-tec','nf-tel','nf-acred'].forEach(id=>{
    const el=document.getElementById(id);
    if(el) el.value='';
  });
  const emp=document.getElementById('nf-emp');
  if(emp) emp.value='';
}

function editLab(email){
  const l=getAllLabs().find(x=>x.email===email);
  if(!l) return;
  const num=getNum(l);
  document.getElementById('edit-title').textContent='✏️ Editar: '+l.nombre;
  document.getElementById('edit-body').innerHTML=`
    <div class="form-grid" style="padding:4px 0">
      <div class="form-group"><label>Nombre comercial</label><input type="text" id="ef-nombre" value="${l.nombre}"></div>
      <div class="form-group"><label>N° de socio${localNums[email]?' (auto asignado)':''}</label>
        <input type="number" id="ef-num" value="${num||''}" placeholder="Dejar vacío = sin número"></div>
      <div class="form-group"><label>Estado</label><input type="text" id="ef-estado" value="${l.estado}"></div>
      <div class="form-group"><label>Ciudad</label><input type="text" id="ef-ciudad" value="${l.ciudad||''}"></div>
      <div class="form-group"><label>Representante legal</label><input type="text" id="ef-rep" value="${l.rep||''}"></div>
      <div class="form-group"><label>Responsable técnico</label><input type="text" id="ef-tec" value="${l.tec||''}"></div>
      <div class="form-group"><label>Teléfono</label><input type="text" id="ef-tel" value="${l.tel||''}"></div>
      <div class="form-group"><label>Personal</label>
        <select id="ef-emp">
          <option value="">Seleccionar</option>
          ${['DE 1 A 10','DE 11 A 50','DE 51 A 250','+ DE 251'].map(o=>`<option ${l.empleados===o?'selected':''}>${o}</option>`).join('')}
        </select>
      </div>
      <div class="form-group full"><label>Áreas acreditadas</label><input type="text" id="ef-acred" value="${l.acreditado||''}"></div>
    </div>
    <div style="margin-top:14px;display:flex;gap:8px">
      <button onclick="saveEdit('${email}')" class="btn btn-green">✓ Guardar cambios</button>
      <button onclick="closeEditModal()" class="btn btn-gray">Cancelar</button>
    </div>
    <div id="edit-msg" style="margin-top:8px;font-size:12px"></div>`;
  document.getElementById('edit-modal').classList.add('open');
}

function saveEdit(email){
  const nombre=document.getElementById('ef-nombre').value.trim();
  const numVal=document.getElementById('ef-num').value.trim();
  if(!nombre){document.getElementById('edit-msg').innerHTML='<span style="color:#b83232">El nombre es obligatorio.</span>';return;}

  // Save edits
  if(!localEdits[email]) localEdits[email]={};
  localEdits[email].nombre=nombre;
  localEdits[email].estado=document.getElementById('ef-estado').value.trim();
  localEdits[email].ciudad=document.getElementById('ef-ciudad').value.trim();
  localEdits[email].rep=document.getElementById('ef-rep').value.trim();
  localEdits[email].tec=document.getElementById('ef-tec').value.trim();
  localEdits[email].tel=document.getElementById('ef-tel').value.trim();
  localEdits[email].empleados=document.getElementById('ef-emp').value;
  localEdits[email].acreditado=document.getElementById('ef-acred').value.trim();
  setLocal('femlac_edits',localEdits);

  // Manual number override
  if(numVal) { localNums[email]=parseInt(numVal); setLocal('femlac_nums',localNums); }
  else if(localNums[email]) { delete localNums[email]; setLocal('femlac_nums',localNums); }

  // Also update localManual if manual lab
  const mi=localManual.findIndex(l=>l.email===email);
  if(mi>=0) { localManual[mi]={...localManual[mi],...localEdits[email]}; setLocal('femlac_manual',localManual); }

  document.getElementById('edit-msg').innerHTML='<span style="color:#1a7a4a">✓ Guardado.</span>';
  setTimeout(()=>{ closeEditModal(); renderAdminTable(); applyFilters(); },800);
}

function deleteLab(email,nombre,fuente){
  if(!confirm(`¿Eliminar "${nombre}"?\n\nEsta acción:\n• Lo quitará del directorio\n• Eliminará su número asignado\n\nNo afecta Google Sheets.`)) return;
  // Add to deleted list
  if(!localDeleted.includes(email)) { localDeleted.push(email); setLocal('femlac_deleted',localDeleted); }
  // Remove from manual if manual
  if(fuente==='manual'){
    localManual=localManual.filter(l=>l.email!==email);
    setLocal('femlac_manual',localManual);
  }
  // Remove number
  if(localNums[email]){ delete localNums[email]; setLocal('femlac_nums',localNums); }
  renderAdminTable();
  applyFilters();
}

/* ════════════════════════════════════════════
   PRINT
════════════════════════════════════════════ */
function printResults(){
  const fecha=new Date().toLocaleDateString('es-MX',{day:'2-digit',month:'long',year:'numeric'});
  const tabNombre=['Inscritos','Pagos','Reconocimientos','Logo / Web'][currentTab];
  const rows=filtered.map((l,i)=>{
    const num=getNum(l), pago=getPago(l), recon=getRecon(l), logoD=getLogo(l);
    return `<tr style="background:${i%2===0?'#fff':'#f0f7fc'}">
      <td style="padding:3px 5px;border-bottom:1px solid #e8f1f7;color:#89b0c8;font-weight:700">${num||'—'}</td>
      <td style="padding:3px 5px;border-bottom:1px solid #e8f1f7;font-weight:600">${l.nombre}</td>
      <td style="padding:3px 5px;border-bottom:1px solid #e8f1f7">${l.estado}</td>
      <td style="padding:3px 5px;border-bottom:1px solid #e8f1f7">${l.ciudad||'—'}</td>
      <td style="padding:3px 5px;border-bottom:1px solid #e8f1f7;font-size:8px">${l.acreditado||'—'}</td>
      <td style="padding:3px 5px;border-bottom:1px solid #e8f1f7;font-weight:700;color:${pago.status==='PAGADO'?'#1a7a4a':pago.status.startsWith('ABONO')?'#916a00':'#b83232'}">${pago.status}</td>
      <td style="padding:3px 5px;border-bottom:1px solid #e8f1f7;color:${pago.adeudo>0?'#b83232':'#89b0c8'}">${pago.adeudo>0?'$'+pago.adeudo.toLocaleString():'—'}</td>
      <td style="padding:3px 5px;border-bottom:1px solid #e8f1f7;color:${recon?'#1a7a4a':'#b83232'}">${recon?'✓':'—'}</td>
      <td style="padding:3px 5px;border-bottom:1px solid #e8f1f7;color:${logoD?'#1a7a4a':'#89b0c8'}">${logoD?'✓':'—'}</td>
    </tr>`;
  }).join('');
  document.getElementById('print-content').innerHTML=`
    <div style="border-bottom:2px solid #e87722;padding-bottom:10px;margin-bottom:12px">
      <div style="font-size:13px;font-weight:bold;color:#1a5f8a">FEDERACIÓN MEXICANA DE LABORATORIOS PARA LA CONSTRUCCIÓN</div>
      <div style="font-size:11px;color:#e87722;margin-top:2px">Directorio de Socios 2026 — ${tabNombre}</div>
      <div style="font-size:10px;color:#4a7fa0;margin-top:4px"><b>${filtered.length}</b> laboratorios · ${fecha}</div>
    </div>
    <table style="width:100%;border-collapse:collapse;font-size:9.5px">
      <thead><tr style="background:#1a5f8a">
        ${['#','Laboratorio','Estado','Ciudad','Acreditación','Pago','Adeudo','Reconoc.','Logo']
          .map(h=>`<th style="color:#fff;padding:5px;text-align:left;font-size:8.5px">${h}</th>`).join('')}
      </tr></thead>
      <tbody>${rows}</tbody>
    </table>
    <div style="margin-top:14px;font-size:9px;color:#89b0c8;text-align:right">FEMLAC 2026 · ${filtered.length} registros · ${fecha}</div>`;
  document.getElementById('print-view').style.display='block';
}

/* ════════════════════════════════════════════
   START
════════════════════════════════════════════ */
loadData();
</script>
</body>
</html>
