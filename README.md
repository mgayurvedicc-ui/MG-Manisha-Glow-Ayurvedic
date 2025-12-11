<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>🌿 MG Manisha Glow Ayurvedic</title>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Marcellus&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>
/* ---------- Page styles ---------- */
:root{
  --green:#2e4a27;
  --gold:#d4b36a;
  --bg:#fffdf9;
}

body{
  margin:0;
  font-family: 'Poppins', sans-serif;
  background: var(--bg);
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
}

/* Watermark */
body::before{
  content:"";
  position:fixed;
  inset:0;
  background-image:url('main-logo.jpg');
  background-position:center;
  background-repeat:no-repeat;
  background-size:520px;
  opacity:0.08;
  z-index:-1;
}

.container{
  max-width:1100px;
  margin:18px auto;
  padding:18px;
}

/* Header */
.top-logo{ display:block; margin:10px auto; width:130px; }
h1,h2{ text-align:center; color:var(--green); margin:6px 0; }
h1{ font-family:'Marcellus', serif; font-size:30px; }

/* Grid cards */
.products, .facepack{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
  gap:14px;
  margin-top:18px;
}
.card{
  background: rgba(255,255,255,0.95);
  border-radius:12px;
  padding:16px;
  box-shadow:0 6px 18px rgba(0,0,0,0.08);
  text-align:center;
}
.card input[type="number"]{
  width:100%;
  padding:8px;
  margin-top:10px;
  border-radius:8px;
  border:1px solid #cfcfcf;
}

/* Buttons */
.btn{
  background: var(--green);
  color:white;
  border: none;
  padding:10px;
  width:100%;
  margin-top:12px;
  border-radius:8px;
  cursor:pointer;
  font-size:15px;
}
.btn.secondary{ background:#128c7e; }

/* Order box */
.order-box{
  max-width:680px;
  margin:24px auto;
  background: rgba(255,255,255,0.96);
  padding:16px;
  border-radius:12px;
  box-shadow:0 6px 18px rgba(0,0,0,0.08);
}
.order-box input, .order-box textarea{
  width:100%;
  padding:10px;
  border-radius:8px;
  border:1px solid #d0d0d0;
  margin-top:10px;
  font-size:14px;
}
.order-box textarea{ min-height:64px; resize:vertical; }

/* company details */
.company-details{
  margin-top:22px;
  text-align:center;
  background: rgba(255,255,255,0.95);
  padding:14px;
  border-radius:12px;
  box-shadow:0 6px 18px rgba(0,0,0,0.06);
}

/* footer */
footer{ text-align:center; color:#666; margin-top:22px; padding-bottom:20px; }

/* Bottom sheet (reports) */
.sheet-overlay{ position:fixed; inset:0; display:none; background:rgba(0,0,0,0.35); justify-content:flex-end; z-index:9999; }
.sheet{ width:100%; max-width:1100px; background:#fff; border-radius:18px 18px 0 0; padding:18px; transform:translateY(100%); transition:transform 240ms ease; box-shadow:0 -12px 40px rgba(0,0,0,0.25); max-height:70vh; overflow:auto; }
.sheet.open{ transform:translateY(0%); }

/* small helpers */
.table-simple{ width:100%; border-collapse:collapse; }
.table-simple td, .table-simple th{ padding:8px; border-bottom:1px solid #eee; font-size:14px; }

/* ---------- Invoice (hidden) premium gold style ---------- */
#invoiceArea{
  width:800px;
  max-width:100%;
  margin:0 auto;
  background:#fff;
  border-radius:14px;
  padding:24px;
  box-shadow:0 10px 34px rgba(0,0,0,0.12);
  border:4px solid var(--gold);
  font-family: 'Poppins', sans-serif;
  color:#222;
}
.inv-header{ text-align:center; border-bottom:3px solid var(--gold); padding-bottom:14px; margin-bottom:12px; }
.inv-header img{ width:110px; display:block; margin:0 auto 6px; }
.inv-brand{ font-family:'Marcellus', serif; font-size:28px; color:var(--green); margin-bottom:4px; }
.inv-tag{ color:#775f2b; font-size:13px; }

/* invoice top info */
.inv-top{ display:flex; justify-content:space-between; gap:12px; margin-top:12px; }
.inv-left{ max-width:58%; }
.inv-right{ text-align:right; min-width:150px; font-size:14px; }

/* items table */
.inv-table{ width:100%; border-collapse:collapse; margin-top:12px; }
.inv-table th{ background:var(--green); color:#fff; padding:10px; text-align:left; font-weight:600; }
.inv-table td{ padding:10px; border-bottom:1px solid #eee; }

/* total box */
.inv-total{ text-align:right; margin-top:12px; font-weight:700; font-size:18px; color:var(--green); }

/* hide invoice area visually on page but keep for PDF generation */
.hidden-print { display:none; }

/* responsive */
@media(max-width:720px){
  .inv-top{ flex-direction:column; align-items:flex-start; }
  .inv-right{ text-align:left; }
}
</style>
</head>
<body>

<div class="container">

  <img src="main-logo.jpg" class="top-logo" alt="Logo">

  <h1>🌿 MG Manisha Glow Ayurvedic</h1>
  <h2>✨ Premium Home-Made Ayurvedic Products</h2>

  <!-- SOAPS -->
  <h2>🧼 Soap Collection (₹50 Each)</h2>
  <div class="products">
    <div class="card"><h3>🍃 Neem Soap</h3><input type="number" id="Neem" min="0" placeholder="Quantity"><button class="btn" onclick="openSheet('neem')">View Report</button></div>
    <div class="card"><h3>🌿 Tulasi Soap</h3><input type="number" id="Tulasi" min="0" placeholder="Quantity"><button class="btn" onclick="openSheet('tulasi')">View Report</button></div>
    <div class="card"><h3>🍀 Aloe Vera Soap</h3><input type="number" id="Aloe" min="0" placeholder="Quantity"></div>
    <div class="card"><h3>🥛 Goat Milk Soap</h3><input type="number" id="Goat" min="0" placeholder="Quantity"></div>
    <div class="card"><h3>🖤 Charcoal Soap</h3><input type="number" id="Charcoal" min="0" placeholder="Quantity"><button class="btn" onclick="openSheet('charcoal')">View Report</button></div>
    <div class="card"><h3>✨ Turmeric Soap</h3><input type="number" id="Turmeric" min="0" placeholder="Quantity"><button class="btn" onclick="openSheet('turmeric')">View Report</button></div>
    <div class="card"><h3>🍚 Rice Potato Soap</h3><input type="number" id="Rice" min="0" placeholder="Quantity"></div>
    <div class="card"><h3>Bheem Sen Kapur Soap</h3><input type="number" id="Bheem" min="0" placeholder="Quantity"></div>
  </div>

  <!-- facepack -->
  <h2>🌸 Face Pack Collection (₹30 Each)</h2>
  <div class="facepack">
    <div class="card"><h3>🍃 Neem Leaf Powder</h3><input type="number" id="NFP" min="0" placeholder="Quantity"></div>
    <div class="card"><h3>💧 Moisturizer Cream</h3><input type="number" id="MFP" min="0" placeholder="Quantity"></div>
  </div>

  <!-- Order -->
  <div class="order-box">
    <h2>📝 Customer Details</h2>
    <input type="text" id="custName" placeholder="👤 Your Name">
    <input type="text" id="custPhone" placeholder="📞 Phone Number">
    <textarea id="custAddr" placeholder="🏠 Full Address"></textarea>

    <input type="text" id="totalAmount" placeholder="💵 Total Amount (Auto)" readonly>

    <div style="display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin-top:12px;">
      <button class="btn" onclick="placeOrder()">📩 WhatsApp Order भेजें</button>
      <button class="btn secondary" onclick="generateInvoicePDF()">📄 Download Invoice PDF</button>
      <button class="btn" style="background:#128c7e" onclick="shareInvoiceWhatsApp()">📤 Share Invoice (WhatsApp)</button>
    </div>
  </div>

  <!-- Company details -->
  <div class="company-details">
    <p><b>🏢 Contact Name:</b> MG Manisha Glow Ayurvedic</p>
    <p><b>📞 Mobile:</b> 8888942084</p>
    <p><b>💬 WhatsApp:</b> 8888942084</p>
    <p><b>📍 Address:</b> Rawande, Kopargaon, Ahilyanagar 423601</p>
    <p><b>📧 Email:</b> mgayurvedicc@gmail.com</p>
  </div>

  <img src="main-logo.jpg" class="top-logo" style="width:110px;margin-top:16px" alt="logo">

  <footer>© <span id="year"></span> MG Manisha Glow Ayurvedic 🌿</footer>
</div>

<!-- bottom sheet for reports -->
<div class="sheet-overlay" id="sheetOverlay">
  <div class="sheet" id="sheet">
    <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:10px">
      <strong id="sheetTitle">Report</strong>
      <button class="btn" onclick="closeSheet()" style="width:auto;background:#2c5f2d">Close</button>
    </div>
    <div id="sheetContent"></div>
    <div style="margin-top:12px">
      <button class="btn" id="shareBtn">📤 Share Report</button>
      <button class="btn" id="pdfBtn" style="background:#444">📄 Download Report</button>
    </div>
  </div>
</div>

<!-- ================= Hidden Invoice Area (for PDF) ================= -->
<div id="invoiceArea" class="hidden-print" style="display:none;">
  <div class="inv-header">
    <img src="main-logo.jpg" alt="Logo">
    <div class="inv-brand">MG Manisha Glow Ayurvedic</div>
    <div class="inv-tag">Premium Ayurvedic Skin Care Products</div>
  </div>

  <div class="inv-top">
    <div class="inv-left">
      <div><strong>To:</strong> <span id="invCustName"></span></div>
      <div><strong>Phone:</strong> <span id="invCustPhone"></span></div>
      <div><strong>Address:</strong> <div id="invCustAddr" style="margin-top:6px"></div></div>
    </div>
    <div class="inv-right">
      <div><strong>Invoice No:</strong> <span id="invNo"></span></div>
      <div><strong>Date:</strong> <span id="invDate"></span></div>
    </div>
  </div>

  <table class="inv-table" id="invTable" style="margin-top:14px;">
    <thead>
      <tr>
        <th style="width:55%;">Product</th>
        <th style="width:15%;">Qty</th>
        <th style="width:15%;">Rate (₹)</th>
        <th style="width:15%;">Total (₹)</th>
      </tr>
    </thead>
    <tbody id="invItems"></tbody>
  </table>

  <div class="inv-total">Grand Total: ₹ <span id="invGrand">0</span></div>
</div>

<!-- html2pdf library -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>

<script>
/* =========== INIT =========== */
document.getElementById('year').textContent = new Date().getFullYear();

/* Pricing map */
const PRICING = {
  Neem:50, Tulasi:50, Aloe:50, Goat:50, Charcoal:50, Turmeric:50, Rice:50, Bheem:50,
  NFP:30, MFP:30
};

/* Bind calcTotal to number inputs */
document.querySelectorAll("input[type='number']").forEach(i => i.addEventListener("input", calcTotal));
calcTotal(); // initial

function calcTotal(){
  let total=0;
  for(let key in PRICING){
    const el=document.getElementById(key);
    if(!el) continue;
    const q=parseInt(el.value)||0;
    total += q * PRICING[key];
  }
  document.getElementById("totalAmount").value = total ? "₹ " + total : "";
}

/* ========== Reports data ========== */
const REPORTS = {
  neem:{
    title:"🍃 Neem Soap - Lab Report",
    data:`PH at 25°C: 6.13
Lather: 212 ml
Mush: 18.5 g
Free Caustic Alkali: Absent
Free Carbonated Alkali: Absent
Grittiness: Passed
Cracking: Passed
Cleaning Efficiency: Passed
Total Fatty Matter: 56.52%
Synthetic Surface Active Agent: 52.14
Fatty Matter From Dissolved Actives: 10.13`
  },
  tulasi:{
    title:"🌿 Tulasi Soap - Lab Report",
    data:`PH at 25°C: 5.89
Lather: 204.3 ml
Mush: 18.5 g
Free Caustic Alkali: Absent
Free Carbonated Alkali: Absent
Grittiness: Passed
Cracking: Passed
Cleaning Efficiency: Passed
Total Fatty Matter: 54.6%
Synthetic Surface Active Agent: 46.2
Fatty Matter From Dissolved Actives: 8.72`
  },
  charcoal:{
    title:"🖤 Charcoal Soap - Lab Report",
    data:`PH at 25°C: 6.64
Lather: 202 ml
Mush: 16.1 g
Free Caustic Alkali: Absent
Free Carbonated Alkali: Absent
Grittiness: Passed
Cracking: Passed
Cleaning Efficiency: Passed
Total Fatty Matter: 43%
Synthetic Surface Active Agent: 44.8
Fatty Matter From Dissolved Actives: 11.02`
  },
  turmeric:{
    title:"✨ Turmeric Soap - Lab Report",
    data:`PH at 25°C: 6.28
Lather: 216.5 ml
Mush: 22.3 g
Free Caustic Alkali: Absent
Free Carbonated Alkali: Absent
Grittiness: Passed
Cracking: Passed
Cleaning Efficiency: Passed
Total Fatty Matter: 64%
Synthetic Surface Active Agent: 45.1
Fatty Matter From Dissolved Actives: 18.0`
  }
};

/* ========== Bottom sheet functions ========== */
function openSheet(key){
  const r = REPORTS[key];
  if(!r) return;
  document.getElementById("sheetTitle").innerText = r.title;
  let html = "<table class='table-simple'>";
  r.data.split("\n").forEach(line=>{
    const parts = line.split(":");
    const k = parts.shift();
    const v = parts.join(":");
    html += `<tr><td style="width:50%"><strong>${k}</strong></td><td>${v || ''}</td></tr>`;
  });
  html += "</table>";
  document.getElementById("sheetContent").innerHTML = html;

  document.getElementById("sheetOverlay").style.display = "flex";
  setTimeout(()=>document.getElementById("sheet").classList.add("open"),20);

  document.getElementById("shareBtn").onclick = ()=>{
    const msg = r.title + "\n\n" + r.data;
    window.open("https://wa.me/?text="+encodeURIComponent(msg));
  };

  document.getElementById("pdfBtn").onclick = ()=>{
    const blob = new Blob([r.title+"\n\n"+r.data], {type:'text/plain'});
    const url=URL.createObjectURL(blob);
    const a=document.createElement('a');
    a.href=url; a.download = (r.title || 'report') + '.txt';
    a.click();
  };
}
function closeSheet(){
  document.getElementById("sheet").classList.remove("open");
  setTimeout(()=>document.getElementById("sheetOverlay").style.display="none",220);
}
document.getElementById("sheetOverlay").addEventListener("click",(e)=>{ if(e.target.id==="sheetOverlay") closeSheet(); });

/* ========== Order sending ========== */
function placeOrder(){
  const name = document.getElementById('custName').value.trim();
  const phone= document.getElementById('custPhone').value.trim();
  const addr = document.getElementById('custAddr').value.trim();
  const total = document.getElementById('totalAmount').value || "₹0";

  if(!name || !phone || !addr){ alert("❗ कृपया Name, Phone और Address भरें!"); return; }

  // Build order summary
  let summary = "🧾 New Order\n\nName: " + name + "\nPhone: " + phone + "\nAddress:\n" + addr + "\n\nItems:\n";
  for(let key in PRICING){
    const qty = parseInt(document.getElementById(key).value) || 0;
    if(qty>0){
      summary += `${key} x ${qty} = ₹${qty * PRICING[key]}\n`;
    }
  }
  summary += `\nTotal: ${total}\n\nThank you! 🌿`;

  // Open WhatsApp with prefilled message
  window.open("https://wa.me/918888942084?text="+encodeURIComponent(summary));
}

/* ========== Invoice (PDF) generation ========== */
function gatherOrderForInvoice(){
  const cust = {
    name: document.getElementById('custName').value.trim() || 'Customer',
    phone: document.getElementById('custPhone').value.trim() || '',
    addr: document.getElementById('custAddr').value.trim() || ''
  };
  const items = [];
  let grand = 0;
  for(let key in PRICING){
    const qty = parseInt(document.getElementById(key).value) || 0;
    if(qty>0){
      const rate = PRICING[key];
      const total = qty*rate;
      items.push({name:key, qty, rate, total});
      grand += total;
    }
  }
  return {cust, items, grand};
}

function populateInvoiceArea(orderData){
  // invoice no + date
  const invNo = 'INV' + Date.now().toString().slice(-8);
  const invDate = new Date().toLocaleString('en-IN', {year:'numeric',month:'short',day:'numeric'});

  document.getElementById('invNo').innerText = invNo;
  document.getElementById('invDate').innerText = invDate;

  document.getElementById('invCustName').innerText = orderData.cust.name;
  document.getElementById('invCustPhone').innerText = orderData.cust.phone;
  document.getElementById('invCustAddr').innerText = orderData.cust.addr;

  // items
  const tbody = document.getElementById('invItems');
  tbody.innerHTML = '';
  orderData.items.forEach(it=>{
    const tr = document.createElement('tr');
    tr.innerHTML = `<td>${it.name}</td><td style="text-align:center">${it.qty}</td><td style="text-align:right">${it.rate}</td><td style="text-align:right">${it.total}</td>`;
    tbody.appendChild(tr);
  });

  document.getElementById('invGrand').innerText = orderData.grand;
}

function generateInvoicePDF(){
  const order = gatherOrderForInvoice();
  if(order.items.length === 0){
    alert("❗ कोई item selected नहीं है — पहले कुछ quantity डालें।");
    return;
  }
  populateInvoiceArea(order);

  // show invoice area (temporarily) so styles apply, then generate
  const inv = document.getElementById('invoiceArea');
  inv.style.display = 'block';

  const nameSafe = (order.cust.name || 'customer').replace(/\s+/g,'_').replace(/[^\w\-]/g,'');
  const filename = `${nameSafe}_Invoice_${new Date().toISOString().slice(0,10)}.pdf`;

  const opt = {
    margin: [8,10],
    filename: filename,
    image: { type: 'jpeg', quality: 0.98 },
    html2canvas: { scale: 2, useCORS:true },
    jsPDF: { unit: 'mm', format:'a4', orientation: 'portrait' }
  };

  // generate PDF
  html2pdf().set(opt).from(inv).save().then(()=>{
    // hide again
    inv.style.display = 'none';
  }).catch((err)=>{
    console.error(err);
    inv.style.display = 'none';
    alert('PDF generate करते समय error आया — console देखें।');
  });
}

/* ========== Share invoice summary on WhatsApp (text only) ========== */
function shareInvoiceWhatsApp(){
  const order = gatherOrderForInvoice();
  if(order.items.length === 0){
    alert("❗ कोई item selected नहीं है — पहले कुछ quantity डालें।");
    return;
  }
  let text = `🧾 MG Manisha Glow - Invoice\n\nCustomer: ${order.cust.name}\nPhone: ${order.cust.phone}\nAddress:\n${order.cust.addr}\n\nItems:\n`;
  order.items.forEach(it=>{
    text += `${it.name} x ${it.qty} = ₹${it.total}\n`;
  });
  text += `\nGrand Total: ₹${order.grand}\n\nThank you 🌿`;
  window.open("https://wa.me/?text="+encodeURIComponent(text));
}
</script>

</body>
</html>
