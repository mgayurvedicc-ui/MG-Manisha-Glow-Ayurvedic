<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>🌿 MG Manisha Glow Ayurvedic</title>

<style>
body{
    margin:0;
    font-family:Arial,sans-serif;
    background:#fffdf9;
}
body::before{
    content:"";
    position:fixed;
    inset:0;
    background:url('main-logo.jpg') center/520px no-repeat;
    opacity:.13;
    z-index:-1;
}
.container{max-width:1100px;margin:auto;padding:20px}
h1,h2{text-align:center;color:#1f3812}
.products,.facepack{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:15px;
}
.card{
    background:#fff;
    border-radius:12px;
    padding:18px;
    box-shadow:0 6px 18px rgba(0,0,0,.1);
    text-align:center;
}
.card input{
    width:100%;
    padding:8px;
    margin-top:8px;
}
.btn{
    background:#6b8e23;
    color:#fff;
    border:none;
    padding:10px;
    width:100%;
    border-radius:6px;
    cursor:pointer;
}
.order-box{
    max-width:600px;
    margin:25px auto;
    background:#fff;
    padding:15px;
    border-radius:12px;
}
.order-box input,textarea{
    width:100%;
    padding:8px;
    margin-top:8px;
}
.sheet-overlay{
    position:fixed;
    inset:0;
    display:none;
    justify-content:flex-end;
    background:rgba(0,0,0,.4);
}
.sheet{
    background:#fff;
    width:100%;
    max-width:1100px;
    border-radius:18px 18px 0 0;
    padding:18px;
    transform:translateY(100%);
    transition:.3s;
}
.sheet.open{transform:translateY(0)}
.sheet table{width:100%;border-collapse:collapse}
.sheet td{padding:8px;border-bottom:1px solid #ddd}
.close{background:#2c5f2d;color:#fff;border:none;padding:8px}
</style>
</head>

<body>
<div class="container">

<h1>🌿 MG Manisha Glow Ayurvedic</h1>
<h2>Premium Home-Made Ayurvedic Products</h2>

<h2>🧼 Soap Collection (₹50 Each)</h2>
<div class="products">
<div class="card"><h3>Neem Soap</h3><input type="number" id="Neem" min="0"><button class="btn" onclick="openSheet('neem')">View Report</button></div>
<div class="card"><h3>Tulasi Soap</h3><input type="number" id="Tulasi" min="0"><button class="btn" onclick="openSheet('tulasi')">View Report</button></div>
<div class="card"><h3>Aloe Soap</h3><input type="number" id="Aloe" min="0"></div>
<div class="card"><h3>Goat Milk</h3><input type="number" id="Goat" min="0"></div>
<div class="card"><h3>Charcoal</h3><input type="number" id="Charcoal" min="0"><button class="btn" onclick="openSheet('charcoal')">View Report</button></div>
<div class="card"><h3>Turmeric</h3><input type="number" id="Turmeric" min="0"><button class="btn" onclick="openSheet('turmeric')">View Report</button></div>
</div>

<h2>🌸 Face Pack (₹30)</h2>
<div class="facepack">
<div class="card"><h3>Neem Powder</h3><input type="number" id="NFP" min="0"></div>
<div class="card"><h3>Moisturizer</h3><input type="number" id="MFP" min="0"></div>
</div>

<div class="order-box">
<h2>Customer Details</h2>
<input id="custName" placeholder="Name">
<input id="custPhone" placeholder="Phone">
<textarea id="custAddr" placeholder="Address"></textarea>
<input id="totalAmount" readonly placeholder="Total Amount">
<button class="btn" onclick="placeOrder()">Send WhatsApp Order</button>
</div>

</div>

<!-- REPORT SHEET -->
<div class="sheet-overlay" id="sheetOverlay">
<div class="sheet" id="sheet">
<h3 id="sheetTitle"></h3>
<div id="sheetContent"></div>
<button class="close" onclick="closeSheet()">Close</button>
</div>
</div>

<script>
/* AUTO TOTAL */
const prices={Neem:50,Tulasi:50,Aloe:50,Goat:50,Charcoal:50,Turmeric:50,NFP:30,MFP:30};
document.querySelectorAll("input[type='number']").forEach(i=>i.addEventListener("input",()=>{
    let total=0;
    for(let id in prices){
        total+=(parseInt(document.getElementById(id)?.value)||0)*prices[id];
    }
    totalAmount.value=total?`₹ ${total}`:"";
}));

/* REPORT DATA */
const REPORTS={
neem:{title:"Neem Soap Report",data:`PH:6.1\nLather:212 ml\nAlkali:Absent`},
tulasi:{title:"Tulasi Soap Report",data:`PH:5.8\nLather:204 ml\nAlkali:Absent`},
charcoal:{title:"Charcoal Soap Report",data:`PH:6.6\nLather:202 ml\nAlkali:Absent`},
turmeric:{title:"Turmeric Soap Report",data:`PH:6.2\nLather:216 ml\nAlkali:Absent`}
};

function openSheet(key){
    const r=REPORTS[key];
    sheetTitle.innerText=r.title;
    let html="<table>";
    r.data.split("\n").forEach(l=>{
        const p=l.split(":");
        html+=`<tr><td>${p[0]}</td><td>${p[1]}</td></tr>`;
    });
    html+="</table>";
    sheetContent.innerHTML=html;
    sheetOverlay.style.display="flex";
    setTimeout(()=>sheet.classList.add("open"),20);
}
function closeSheet(){
    sheet.classList.remove("open");
    setTimeout(()=>sheetOverlay.style.display="none",300);
}

/* WHATSAPP */
function placeOrder(){
let msg=`New Order\nName:${custName.value}\nPhone:${custPhone.value}\nAddress:${custAddr.value}\nTotal:${totalAmount.value}`;
window.open("https://wa.me/918888942084?text="+encodeURIComponent(msg));
}
</script>
</body>
</html>
