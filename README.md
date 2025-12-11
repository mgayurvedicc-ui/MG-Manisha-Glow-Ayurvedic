<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>🌿 MG Manisha Glow Ayurvedic</title>

<style>

body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background: #fffdf9;
    position: relative;
    overflow-x: hidden;
}

/* Background Logo Watermark */
body::before {
    content: "";
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('main-logo.jpg');
    background-repeat: no-repeat;
    background-position: center;
    background-size: 520px;
    opacity: 0.13;
    z-index: -1;
}

.top-logo, .bottom-logo {
    display: block;
    margin: 20px auto;
}
.top-logo { width: 130px; }
.bottom-logo { width: 110px; }

.container {
    max-width: 1100px;
    margin: auto;
    padding: 20px;
}

h1, h2 {
    text-align: center;
    color: #1f3812;
    font-weight: 700;
}

.products, .facepack {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 15px;
    margin-top: 20px;
}

.card {
    background: rgba(255,255,255,0.90);
    border-radius: 12px;
    padding: 18px;
    box-shadow: 0 6px 18px rgba(0,0,0,0.10);
    text-align: center;
}

.card input {
    width: 100%;
    padding: 8px;
    margin-top: 8px;
    border-radius: 6px;
    border: 1px solid #aaa;
}

.btn {
    background: #6b8e23;
    color: white;
    padding: 10px;
    border: none;
    width: 100%;
    margin-top: 12px;
    border-radius: 6px;
    cursor: pointer;
    font-size: 15px;
}

/* ORDER BOX */
.order-box {
    background: rgba(255,255,255,0.95);
    padding: 15px;
    border-radius: 12px;
    margin-top: 25px;
    width: 100%;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
    box-shadow: 0 6px 18px rgba(0,0,0,0.10);
}

.order-box input, .order-box textarea {
    width: 100%;
    padding: 8px;
    margin-top: 8px;
    border-radius: 6px;
    border: 1px solid #aaa;
    font-size: 14px;
}

.order-box textarea {
    height: 60px;
}

/* COMPANY DETAILS */
.company-details {
    text-align: center;
    margin-top: 35px;
    background: rgba(255,255,255,0.90);
    padding: 18px;
    border-radius: 12px;
    box-shadow: 0 6px 18px rgba(0,0,0,0.08);
}
.company-details p {
    margin: 6px 0;
    font-size: 15px;
}

footer {
    text-align: center;
    margin-top: 40px;
    padding-bottom: 20px;
    color: #666;
}

/* =============BOTTOM SHEET============ */
.sheet-overlay {
    position: fixed;
    inset: 0;
    display: none;
    justify-content: flex-end;
    z-index: 9999;
    background: rgba(0,0,0,0.40);
    backdrop-filter: blur(4px);
}

.sheet {
    width: 100%;
    max-width: 1100px;
    background: #ffffffee;
    border-radius: 18px 18px 0 0;
    box-shadow: 0 -12px 36px rgba(0,0,0,0.25);
    max-height: 70vh;
    overflow-y: auto;
    padding: 18px;
    transform: translateY(100%);
    transition: transform 300ms ease;
}

.sheet.open { transform: translateY(0%); }

.sheet-header {
    display:flex;
    align-items:center;
    justify-content:space-between;
    margin-bottom:10px;
}

.sheet-title {
    font-weight:700;
    font-size:18px;
    color:#16360f;
}

.close {
    background: #2c5f2d;
    color:#fff;
    border:none;
    padding:8px 12px;
    border-radius:8px;
    cursor:pointer;
}

.sheet table {
    width:100%;
    border-collapse:collapse;
}
.sheet td {
    padding:8px 6px;
    border-bottom:1px solid #eee;
    font-size:14px;
}

.share-btn {
    margin-top: 12px;
    width: 100%;
    padding: 10px;
    border: none;
    background: #128c7e;
    color: white;
    border-radius: 8px;
    cursor: pointer;
    font-size: 16px;
}

.pdf-btn {
    margin-top: 10px;
    width: 100%;
    padding: 10px;
    border: none;
    background: #444;
    color: white;
    border-radius: 8px;
    cursor: pointer;
    font-size: 15px;
}

</style>
</head>
<body>

<div class="container">

<img src="main-logo.jpg" class="top-logo">

<h1>🌿 MG Manisha Glow Ayurvedic</h1>
<h2>✨ Premium Home-Made Ayurvedic Products</h2>

<!-- SOAP SECTION -->
<h2>🧼 Soap Collection (₹50 Each)</h2>

<div class="products">

<div class="card">
    <h3>🍃 Neem Soap</h3>
    <input type="number" id="Neem" min="0" placeholder="Quantity">
    <button class="btn" onclick="openSheet('neem')">View Chemical Parameters Report</button>
</div>

<div class="card">
    <h3>🌿 Tulasi Soap</h3>
    <input type="number" id="Tulasi" min="0" placeholder="Quantity">
    <button class="btn" onclick="openSheet('tulasi')">View Chemical Parameters Report</button>
</div>

<div class="card">
    <h3>🍀 Aloe Vera Soap</h3>
    <input type="number" id="Aloe" min="0" placeholder="Quantity">
</div>

<div class="card">
    <h3>🥛 Goat Milk Soap</h3>
    <input type="number" id="Goat" min="0" placeholder="Quantity">
</div>

<div class="card">
    <h3>🖤 Charcoal Soap</h3>
    <input type="number" id="Charcoal" min="0" placeholder="Quantity">
    <button class="btn" onclick="openSheet('charcoal')">View Chemical Parameters Report</button>
</div>

<div class="card">
    <h3>✨ Turmeric Soap</h3>
    <input type="number" id="Turmeric" min="0" placeholder="Quantity">
    <button class="btn" onclick="openSheet('turmeric')">View Chemical Parameters Report</button>
</div>

<div class="card">
    <h3>🍚 Rice Potato Soap</h3>
    <input type="number" id="Rice" min="0" placeholder="Quantity">
</div>

<div class="card">
    <h3>Bheem Sen Kapur Soap</h3>
    <input type="number" id="Bheem" min="0" placeholder="Quantity">
</div>

</div>

<!-- FACE PACK -->
<h2>🌸 Face Pack Collection (₹30 Each)</h2>

<div class="facepack">

<div class="card">
    <h3>🍃 Neem Leaf Powder</h3>
    <input type="number" id="NFP" min="0" placeholder="Quantity">
</div>

<div class="card">
    <h3>💧 Moisturizer Cream</h3>
    <input type="number" id="MFP" min="0" placeholder="Quantity">
</div>

</div>

<!-- ORDER FORM -->
<div class="order-box">
<h2>📝 Customer Details</h2>

<input type="text" id="custName" placeholder="👤 Your Name">
<input type="text" id="custPhone" placeholder="📞 Phone Number">
<textarea id="custAddr" placeholder="🏠 Full Address"></textarea>

<input type="text" id="totalAmount" placeholder="💵 Total Amount (Auto)" readonly>

<button class="btn" onclick="placeOrder()">📩 WhatsApp Order भेजें</button>
</div>

<!-- COMPANY DETAILS -->
<div class="company-details">
<p><b>🏢 Contact Name:</b> MG Manisha Glow Ayurvedic</p>
<p><b>📞 Mobile:</b> 8888942084</p>
<p><b>💬 WhatsApp:</b> 8888942084</p>
<p><b>📍 Address:</b> Rawande, Kopargaon, Ahilyanagar 423601</p>
<p><b>📧 Email:</b> mgayurvedicc@gmail.com</p>
<p><b>📸 Instagram:</b> @mg_manisha_glow_Ayurvedic_</p>
<p><b>🌐 Website:</b> https://mgayurvedicc-ui.github.io/MG-Manisha-Glow-Ayurvedic/</p>
</div>

<img src="main-logo.jpg" class="bottom-logo">

<footer>
© <span id="year"></span> MG Manisha Glow Ayurvedic 🌿
</footer>

</div>


<!-- ============== BOTTOM SHEET ============== -->
<div class="sheet-overlay" id="sheetOverlay">
    <div class="sheet" id="sheet">
        <div class="sheet-header">
            <div class="sheet-title" id="sheetTitle">Report</div>
            <button class="close" onclick="closeSheet()">Close</button>
        </div>
        <div id="sheetContent"></div>

        <button class="share-btn" id="shareBtn">📤 Share Report</button>
        <button class="pdf-btn" id="pdfBtn">📄 Download Report</button>
    </div>
</div>


<script>

/* YEAR SET */
document.getElementById('year').textContent = new Date().getFullYear();


/* AUTO TOTAL CALCULATION */
function calcTotal() {
    const pricing = {
        Neem:50, Tulasi:50, Aloe:50, Goat:50,
        Charcoal:50, Turmeric:50, Rice:50, Bheem:50,
        NFP:30, MFP:30
    };

    let total = 0;

    for (let id in pricing) {
        let qty = parseInt(document.getElementById(id).value) || 0;
        total += qty * pricing[id];
    }

    document.getElementById("totalAmount").value = total ? "₹ " + total : "";
}

document.querySelectorAll("input[type='number']").forEach(i =>
    i.addEventListener("input", calcTotal)
);


/* REPORT DATA */
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


/* OPEN SHEET */
function openSheet(key){
    const r = REPORTS[key];
    document.getElementById("sheetTitle").innerText = r.title;

    let html = "<table>";
    r.data.split("\n").forEach(line=>{
        const [k,v] = line.split(":");
        html += `<tr><td>${k}</td><td>${v}</td></tr>`;
    });
    html += "</table>";

    document.getElementById("sheetContent").innerHTML = html;

    document.getElementById("sheetOverlay").style.display="flex";
    setTimeout(()=>document.getElementById("sheet").classList.add("open"),20);

    /* Share on WhatsApp */
    document.getElementById("shareBtn").onclick = ()=>{
        const msg = r.title + "\n\n" + r.data;
        window.open("https://wa.me/?text="+encodeURIComponent(msg));
    };

    /* Download TXT */
    document.getElementById("pdfBtn").onclick = ()=>{
        const blob = new Blob([r.title+"\n\n"+r.data], {type:"text/plain"});
        const url = URL.createObjectURL(blob);
        const a=document.createElement("a");
        a.href=url;
        a.download=r.title+".txt";
        a.click();
    };
}

/* CLOSE SHEET */
function closeSheet(){
    document.getElementById("sheet").classList.remove("open");
    setTimeout(()=>document.getElementById("sheetOverlay").style.display="none",250);
}

document.getElementById("sheetOverlay").addEventListener("click",(e)=>{
    if(e.target.id==="sheetOverlay") closeSheet();
});


/* PLACE ORDER */
function placeOrder(){
    let name=custName.value.trim();
    let phone=custPhone.value.trim();
    let addr=custAddr.value.trim();
    let total=totalAmount.value || "₹0";

    if(!name||!phone||!addr){
        alert("❗ कृपया Name, Phone और Address भरें!");
        return;
    }

    let msg = 
`🧾 New Order

Name: ${name}
Phone: ${phone}
Address:
${addr}

Total: ${total}`;

    window.open("https://wa.me/918888942084?text="+encodeURIComponent(msg));
}

</script>

</body>
</html>
