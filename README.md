<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>MG Manisha Glow Ayurvedic — Order & Invoice</title>

<!-- Libraries -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>

<!-- Styles -->
<style>
:root{
  --green:#244a2e;
  --gold:#d4af37;
  --bg:#fffdf7;
}
body{font-family:Arial,Helvetica,sans-serif;margin:0;background:var(--bg);-webkit-font-smoothing:antialiased}
.container{max-width:1100px;margin:18px auto;padding:18px}
.header{display:flex;align-items:center;gap:18px}
.header img{width:110px}
.title{font-size:22px;color:var(--green);font-weight:700}
.subtitle{color:#6b5a2f;font-size:14px;margin-top:4px}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:12px;margin-top:14px}
.card{background:#fff;padding:12px;border-radius:10px;box-shadow:0 6px 18px rgba(0,0,0,0.06)}
label{display:block;font-size:13px;color:#333;margin-bottom:6px}
select,input[type="number"],input[type="text"],textarea{width:100%;padding:8px;border-radius:6px;border:1px solid #ccc;font-size:14px}
.btn{background:var(--green);color:white;padding:10px;border:none;border-radius:8px;cursor:pointer}
.btn.secondary{background:#128c7e}
.row-actions{display:flex;gap:8px;margin-top:8px}
.top-actions{display:flex;gap:8px;margin-top:12px;flex-wrap:wrap}
.small{padding:8px;font-size:14px}
.order-box{margin-top:16px;background:#fff;padding:14px;border-radius:10px;box-shadow:0 6px 18px rgba(0,0,0,0.06)}
.footer{margin-top:18px;text-align:center;color:#666}

/* Invoice preview styles (what will go to PDF) */
#invoicePreview{
  width:800px;max-width:100%;margin:12px auto;padding:18px;border-radius:12px;background:#fff;border:4px solid var(--gold);box-shadow:0 12px 36px rgba(0,0,0,0.12);display:none;
  font-size:14px;color:#222;
}
.inv-header{text-align:center;border-bottom:3px solid var(--gold);padding-bottom:12px;margin-bottom:12px}
.inv-header img{width:110px}
.inv-title{font-family:Georgia,serif;font-size:26px;color:var(--green);margin-top:6px}
.inv-sub{color:#6b5a2f;font-size:13px}
.inv-top{display:flex;justify-content:space-between;gap:12px;margin-top:12px}
.inv-left{max-width:60%}
.inv-right{text-align:right;min-width:150px}
.inv-table{width:100%;border-collapse:collapse;margin-top:12px}
.inv-table th{background:var(--green);color:#fff;padding:10px;text-align:left}
.inv-table td{padding:10px;border-bottom:1px solid #eee}
.inv-total{text-align:right;margin-top:12px;font-weight:700;color:var(--green);font-size:18px}
.stamp{display:inline-block;padding:8px 12px;border-radius:8px;border:2px dashed var(--gold);color:var(--gold);font-weight:700;margin-top:10px}
.signature{margin-top:20px;display:flex;justify-content:space-between;align-items:center}
.sign-box{width:200px;text-align:center}
.sign-line{border-top:1px solid #999;padding-top:8px;color:#555;font-size:13px}

/* responsive */
@media(max-width:720px){
  .inv-top{flex-direction:column}
  .inv-right{text-align:left}
}
</style>
</head>
<body>

<div class="container">

  <!-- Header -->
  <div class="header">
    <img src="main-logo.jpg" alt="Logo" id="pageLogo">
    <div>
      <div class="title">MG Manisha Glow Ayurvedic</div>
      <div class="subtitle">Premium Ayurvedic Home-made Soaps & Face Packs</div>
    </div>
  </div>

  <!-- Product selection area -->
  <div style="margin-top:14px">
    <div style="display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap">
      <div style="font-weight:700;color:var(--green)">Create Order (Select products below)</div>
      <div class="top-actions">
        <button class="btn small" onclick="addRow()">+ Add Item</button>
        <button class="btn small secondary" onclick="clearRows()">Reset Items</button>
      </div>
    </div>

    <div id="itemsContainer" style="margin-top:12px"></div>
  </div>

  <!-- Order & Customer details -->
  <div class="order-box">
    <div style="display:flex;gap:12px;flex-wrap:wrap">
      <div style="flex:1">
        <label>Customer Name</label>
        <input type="text" id="custName" placeholder="Customer name">
      </div>
      <div style="width:220px">
        <label>Phone</label>
        <input type="text" id="custPhone" placeholder="Phone number">
      </div>
      <div style="flex-basis:100%">
        <label>Address</label>
        <textarea id="custAddr" placeholder="Full address (for delivery)"></textarea>
      </div>
    </div>

    <div style="display:flex;justify-content:space-between;align-items:center;margin-top:12px;gap:12px;flex-wrap:wrap">
      <div style="flex:1">
        <div style="font-size:14px;color:#333">Invoice #: <strong id="invNoDisplay"></strong> &nbsp;&nbsp; Date: <strong id="invDateDisplay"></strong></div>
      </div>

      <div style="min-width:220px;text-align:right">
        <div style="font-size:14px;color:#333">Grand Total</div>
        <div style="font-size:20px;color:var(--green);font-weight:700">₹ <span id="grandTotal">0</span></div>
      </div>
    </div>

    <div style="display:flex;gap:8px;margin-top:12px;flex-wrap:wrap">
      <button class="btn" onclick="sendWhatsAppOrder()">📩 Send Order via WhatsApp</button>
      <button class="btn" onclick="generateInvoicePDF()">📄 Download Invoice (PDF)</button>
      <button class="btn secondary" onclick="shareInvoiceWhatsApp()">📤 Share Invoice Text (WhatsApp)</button>
    </div>
  </div>

  <div class="footer">© <span id="year"></span> MG Manisha Glow Ayurvedic</div>
</div>

<!-- Hidden invoice area (used to render PDF) -->
<div id="invoicePreview">
  <div class="inv-header">
    <img src="main-logo.jpg" alt="Logo">
    <div class="inv-title">MG Manisha Glow Ayurvedic</div>
    <div class="inv-sub">Premium Ayurvedic Skin Care Products</div>
  </div>

  <div class="inv-top">
    <div class="inv-left">
      <div><strong>Bill To:</strong> <span id="invCustName"></span></div>
      <div><strong>Phone:</strong> <span id="invCustPhone"></span></div>
      <div style="margin-top:6px"><strong>Address:</strong><div id="invCustAddr"></div></div>
    </div>
    <div class="inv-right">
      <div><strong>Invoice No:</strong> <span id="invNo"></span></div>
      <div><strong>Date:</strong> <span id="invDate"></span></div>
    </div>
  </div>

  <table class="inv-table" id="invTable">
    <thead>
      <tr><th style="width:55%">Product</th><th style="width:15%">Qty</th><th style="width:15%">Rate (₹)</th><th style="width:15%">Total (₹)</th></tr>
    </thead>
    <tbody id="invItems"></tbody>
  </table>

  <div class="inv-total">Grand Total: ₹ <span id="invGrand">0</span></div>

  <div style="margin-top:10px">
    <span class="stamp">PAID ON DELIVERY</span>
  </div>

  <div class="signature">
    <div class="sign-box">
      <div class="sign-line">Customer Signature</div>
    </div>
    <div class="sign-box" style="text-align:right">
      <div style="font-weight:700;color:var(--green);">Authorized Signatory</div>
      <div class="sign-line">MG Manisha Glow</div>
    </div>
  </div>
</div>

<!-- Script -->
<script>
/* ---------- Data & Init ---------- */

// product catalog (dropdown options)
const PRODUCTS = [
  {id:'Neem Soap', price:50},
  {id:'Tulasi Soap', price:50},
  {id:'Aloe Vera Soap', price:50},
  {id:'Goat Milk Soap', price:50},
  {id:'Charcoal Soap', price:50},
  {id:'Turmeric Soap', price:50},
  {id:'Rice Potato Soap', price:50},
  {id:'Bheem Sen Kapur Soap', price:50},
  {id:'Neem Leaf Powder', price:30},
  {id:'Moisturizer Cream', price:30}
];

let rowCounter = 0;
const itemsContainer = document.getElementById('itemsContainer');
const grandTotalEl = document.getElementById('grandTotal');
const invNoDisplay = document.getElementById('invNoDisplay');
const invDateDisplay = document.getElementById('invDateDisplay');
document.getElementById('year').textContent = new Date().getFullYear();

// generate invoice no & date
function generateInvoiceMeta(){
  const invNo = 'INV' + Date.now().toString().slice(-8);
  const dateStr = new Date().toLocaleDateString('en-IN', {day:'2-digit',month:'short',year:'numeric'});
  document.getElementById('invNo').innerText = invNo;
  document.getElementById('invNoDisplay').innerText = invNo;
  document.getElementById('invDate').innerText = dateStr;
  document.getElementById('invDateDisplay').innerText = dateStr;
}
generateInvoiceMeta();

/* ---------- Rows: add / remove ---------- */
function createProductSelectHtml(rowId){
  let optHtml = PRODUCTS.map(p=>`<option value="${p.id}" data-price="${p.price}">${p.id} — ₹${p.price}</option>`).join('');
  return `<div style="display:flex;gap:8px;align-items:center">
      <select onchange="onProductChange(${rowId})" id="prod_${rowId}">${optHtml}</select>
      <input type="number" id="qty_${rowId}" value="1" min="0" style="width:80px" onchange="onQtyChange(${rowId})">
      <input type="text" id="rate_${rowId}" readonly style="width:120px" value="₹0">
      <input type="text" id="ltotal_${rowId}" readonly style="width:120px" value="₹0">
      <button class="btn small" onclick="removeRow(${rowId})" style="background:#b33">Remove</button>
    </div>`;
}

function addRow(selectedId=null, qty=1){
  rowCounter++;
  const rowId = rowCounter;
  const wrapper = document.createElement('div');
  wrapper.className = 'card';
  wrapper.id = `row_${rowId}`;
  wrapper.innerHTML = `<label>Item ${rowId}</label>` + createProductSelectHtml(rowId);
  itemsContainer.appendChild(wrapper);

  // set default selection & qty then update values
  if(selectedId){
    const sel = document.getElementById(`prod_${rowId}`);
    sel.value = selectedId;
  }
  document.getElementById(`qty_${rowId}`).value = qty;
  onProductChange(rowId);
  calcGrandTotal();
}

// remove a row
function removeRow(rowId){
  const el = document.getElementById(`row_${rowId}`);
  if(el){ el.remove(); calcGrandTotal(); }
}

// clear all rows
function clearRows(){
  itemsContainer.innerHTML = '';
  rowCounter = 0;
  addRow(); // add one empty row
}

/* ---------- when product or qty changes ---------- */
function onProductChange(rowId){
  const sel = document.getElementById(`prod_${rowId}`);
  const selectedPrice = parseFloat(sel.options[sel.selectedIndex].getAttribute('data-price')) || 0;
  document.getElementById(`rate_${rowId}`).value = '₹' + selectedPrice;
  // update line total
  const qty = parseInt(document.getElementById(`qty_${rowId}`).value) || 0;
  document.getElementById(`ltotal_${rowId}`).value = '₹' + (qty * selectedPrice);
  calcGrandTotal();
}

function onQtyChange(rowId){
  const sel = document.getElementById(`prod_${rowId}`);
  const selectedPrice = parseFloat(sel.options[sel.selectedIndex].getAttribute('data-price')) || 0;
  const qty = parseInt(document.getElementById(`qty_${rowId}`).value) || 0;
  document.getElementById(`ltotal_${rowId}`).value = '₹' + (qty * selectedPrice);
  calcGrandTotal();
}

/* ---------- calculate grand total ---------- */
function calcGrandTotal(){
  let total = 0;
  for(let i=1;i<=rowCounter;i++){
    const row = document.getElementById(`row_${i}`);
    if(!row) continue;
    const sel = document.getElementById(`prod_${i}`);
    const qtyInput = document.getElementById(`qty_${i}`);
    if(!sel || !qtyInput) continue;
    const price = parseFloat(sel.options[sel.selectedIndex].getAttribute('data-price')) || 0;
    const qty = parseInt(qtyInput.value) || 0;
    total += price * qty;
  }
  grandTotalEl.innerText = total;
  return total;
}

/* ---------- initial row ---------- */
addRow();

/* ---------- WhatsApp Order message (full items list) ---------- */
function sendWhatsAppOrder(){
  const name = document.getElementById('custName').value.trim();
  const phone = document.getElementById('custPhone').value.trim();
  const addr = document.getElementById('custAddr').value.trim();
  if(!name || !phone || !addr){
    alert('कृपया Name, Phone और Address भरें।');
    return;
  }

  // build items
  let itemLines = '';
  let any=false;
  for(let i=1;i<=rowCounter;i++){
    const row = document.getElementById(`row_${i}`);
    if(!row) continue;
    const sel = document.getElementById(`prod_${i}`);
    const qty = parseInt(document.getElementById(`qty_${i}`).value) || 0;
    if(qty>0){
      const price = parseFloat(sel.options[sel.selectedIndex].getAttribute('data-price')) || 0;
      const lineTotal = price * qty;
      itemLines += `• ${sel.value} — ${qty} pcs = ₹${lineTotal}\n`;
      any = true;
    }
  }
  if(!any){
    alert('कृपया कम से कम एक item चुनें और quantity डालें।');
    return;
  }

  const total = calcGrandTotal();
  const invNo = document.getElementById('invNo').innerText || document.getElementById('invNoDisplay').innerText;

  const msg = `🧾 *New Order — ${invNo}*\n\n👤 *Name:* ${name}\n📞 *Phone:* ${phone}\n🏠 *Address:* ${addr}\n\n📦 *Order Items:*\n${itemLines}\n💵 *Grand Total:* ₹${total}\n\nधन्यवाद 🌿`;
  // Open WhatsApp (to your number). Change number if needed.
  window.open('https://wa.me/918888942084?text=' + encodeURIComponent(msg));
}

/* ---------- Build invoice area then generate PDF ---------- */
async function generateInvoicePDF(){
  // validate basic
  const name = document.getElementById('custName').value.trim();
  const phone = document.getElementById('custPhone').value.trim();
  const addr = document.getElementById('custAddr').value.trim();
  if(!name || !phone || !addr){
    alert('कृपया Name, Phone और Address भरें।');
    return;
  }

  // collect order
  const items = [];
  for(let i=1;i<=rowCounter;i++){
    const row = document.getElementById(`row_${i}`);
    if(!row) continue;
    const sel = document.getElementById(`prod_${i}`);
    const qty = parseInt(document.getElementById(`qty_${i}`).value) || 0;
    if(qty>0){
      const price = parseFloat(sel.options[sel.selectedIndex].getAttribute('data-price')) || 0;
      items.push({name: sel.value, qty, price, total: price*qty});
    }
  }
  if(items.length===0){
    alert('कृपया कम से कम एक item चुनें और quantity डालें।');
    return;
  }

  // populate invoice preview
  document.getElementById('invCustName').innerText = name;
  document.getElementById('invCustPhone').innerText = phone;
  document.getElementById('invCustAddr').innerText = addr;
  generateInvoiceMeta(); // refresh invoice no/date

  const tbody = document.getElementById('invItems');
  tbody.innerHTML = '';
  let grand = 0;
  items.forEach(it=>{
    const tr = document.createElement('tr');
    tr.innerHTML = `<td>${it.name}</td><td style="text-align:center">${it.qty}</td><td style="text-align:right">${it.price}</td><td style="text-align:right">${it.total}</td>`;
    tbody.appendChild(tr);
    grand += it.total;
  });
  document.getElementById('invGrand').innerText = grand;

  // show invoice preview for rendering
  const preview = document.getElementById('invoicePreview');
  preview.style.display = 'block';

  // small delay to ensure images/styles loaded
  await new Promise(r=>setTimeout(r,300));

  // render to canvas & pdf
  try{
    const canvas = await html2canvas(preview, {scale:2, useCORS:true, logging:false});
    const imgData = canvas.toDataURL('image/png', 1.0);
    const { jsPDF } = window.jspdf;
    const pdf = new jsPDF('p','mm','a4');
    const pageWidth = pdf.internal.pageSize.getWidth();
    const pageHeight = pdf.internal.pageSize.getHeight();
    // calculate image size to fit A4 width with aspect ratio
    const imgProps = pdf.getImageProperties(imgData);
    const imgWidth = pageWidth - 20; // margins
    const imgHeight = (imgProps.height * imgWidth) / imgProps.width;
    let y = 10;
    pdf.addImage(imgData, 'PNG', 10, y, imgWidth, imgHeight);
    // filename
    const invNo = document.getElementById('invNo').innerText || 'INV';
    const filename = `${invNo}_MG_Invoice.pdf`;
    pdf.save(filename);
  }catch(err){
    console.error(err);
    alert('PDF generate करते समय error आया — console देखें।');
  }finally{
    // hide preview again
    preview.style.display = 'none';
  }
}

/* ---------- Share invoice text (WhatsApp) ---------- */
function shareInvoiceWhatsApp(){
  const name = document.getElementById('custName').value.trim();
  const phone = document.getElementById('custPhone').value.trim();
  const addr = document.getElementById('custAddr').value.trim();
  if(!name || !phone || !addr){
    alert('कृपया Name, Phone और Address भरें।');
    return;
  }
  let itemLines = '';
  for(let i=1;i<=rowCounter;i++){
    const row = document.getElementById(`row_${i}`);
    if(!row) continue;
    const sel = document.getElementById(`prod_${i}`);
    const qty = parseInt(document.getElementById(`qty_${i}`).value) || 0;
    if(qty>0){
      const price = parseFloat(sel.options[sel.selectedIndex].getAttribute('data-price')) || 0;
      itemLines += `• ${sel.value} x ${qty} = ₹${price*qty}\n`;
    }
  }
  if(!itemLines){
    alert('कृपया कम से कम एक item चुनें और quantity डालें।');
    return;
  }
  const total = calcGrandTotal();
  const invNo = document.getElementById('invNo').innerText || document.getElementById('invNoDisplay').innerText;
  const msg = `🧾 Invoice ${invNo}\n\nCustomer: ${name}\nPhone: ${phone}\nAddress:\n${addr}\n\nItems:\n${itemLines}\nGrand Total: ₹${total}\n\nThanks 🌿`;
  window.open('https://wa.me/?text=' + encodeURIComponent(msg));
}

</script>

</body>
</html>
