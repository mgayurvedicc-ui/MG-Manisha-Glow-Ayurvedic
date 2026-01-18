<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>🌿 MG Manisha Glow Ayurvedic</title>

<style>
:root{
    --dark:#0f2f1f;
    --green:#1f5d3b;
    --light:#eaf6ef;
    --gold:#c9a24d;
}

body{
    margin:0;
    font-family: "Segoe UI", Arial, sans-serif;
    background:linear-gradient(180deg,#0f2f1f,#143f2a);
    color:#eaf6ef;
}

body::before{
    content:"";
    position:fixed;
    inset:0;
    background:url('main-logo.jpg') center/480px no-repeat;
    opacity:0.08;
    z-index:-1;
}

.container{
    max-width:1100px;
    margin:auto;
    padding:24px;
}

h1,h2{
    text-align:center;
    color:#eaf6ef;
}
h1{font-size:34px}
h2{margin-top:32px}

.products{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
    gap:18px;
    margin-top:20px;
}

.card{
    background:rgba(20,63,42,.95);
    border-radius:16px;
    padding:18px;
    box-shadow:0 10px 25px rgba(0,0,0,.35);
    border:1px solid rgba(201,162,77,.3);
}
.card h3{margin:0}
.small{font-size:14px;color:#cde7d7}
.ingredients{font-size:13px;margin-top:6px;color:#d8efe4}
.card input{
    width:100%;
    margin-top:10px;
    padding:8px;
    border-radius:6px;
    border:none;
}

.order-box{
    max-width:420px;
    margin:36px auto;
    background:rgba(20,63,42,.95);
    padding:16px;
    border-radius:18px;
    border:1px solid rgba(201,162,77,.4);
}
.order-box input,
.order-box textarea{
    width:100%;
    padding:8px;
    margin-top:6px;
    border-radius:6px;
    border:none;
}
.order-box textarea{height:60px}

.btn{
    background:linear-gradient(135deg,#c9a24d,#e7c76a);
    color:#0f2f1f;
    font-weight:bold;
    border:none;
    width:100%;
    padding:10px;
    margin-top:12px;
    border-radius:8px;
    cursor:pointer;
}

.section{
    max-width:700px;
    margin:40px auto;
    background:rgba(20,63,42,.95);
    padding:22px;
    border-radius:18px;
    border:1px solid rgba(201,162,77,.35);
}

.faq-item{margin-top:14px}
.faq-q{font-weight:bold;color:#e7c76a}
.faq-a{font-size:14px;color:#d8efe4;margin-top:6px}

footer{
    text-align:center;
    margin:40px 0;
    font-size:14px;
    color:#cde7d7;
}
footer a{color:#e7c76a;text-decoration:none;font-weight:bold}
</style>
</head>

<body>
<div class="container">

<h1>🌿 MG Manisha Glow Ayurvedic</h1>
<h2>Premium Home-Made Ayurvedic Products</h2>

<h2>🧼 Ayurvedic Soap Collection (₹50 Each)</h2>

<div class="products">
<div class="card">
<h3>🍃 Neem Tulsi Ayurvedic Soap</h3>
<div class="small">For Face & Body</div>
<div class="ingredients"><b>Ingredients:</b> Neem Tulsi Base, Extracts, Glycerin</div>
<input type="number" id="neem" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>🖤 Charcoal Ayurvedic Soap</h3>
<div class="small">For Face & Body</div>
<div class="ingredients"><b>Ingredients:</b> Activated Charcoal, Aloe Vera</div>
<input type="number" id="charcoal" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>Turti (Alum) Ayurvedic Soap</h3>
<div class="ingredients"><b>Ingredients:</b> Alum Base, Honey</div>
<input type="number" id="alum" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>Camphor (Kapoor) Ayurvedic Soap</h3>
<div class="ingredients"><b>Ingredients:</b> Kapoor, Coconut Oil</div>
<input type="number" id="kapoor" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>🥛 Goat Milk Ayurvedic Soap</h3>
<div class="ingredients"><b>Ingredients:</b> Goat Milk, Almond Oil</div>
<input type="number" id="goat" min="0" placeholder="Quantity">
</div>
</div>

<div class="order-box">
<h2>📝 Order Details</h2>
<input id="name" placeholder="Your Name">
<input id="phone" placeholder="Phone Number">
<textarea id="address" placeholder="Address"></textarea>
<input id="total" placeholder="Total Amount" readonly>
<button class="btn" onclick="order()">📩 WhatsApp Order</button>
</div>

<!-- TEST REPORT SECTION -->
<div class="section">
<h2 style="cursor:pointer" onclick="toggleReports()">🧪 Soap Lab Test Reports (Click)</h2>
<div id="reports" style="display:none">
<div class="faq-item"><div class="faq-q">Neem Tulsi Soap</div><div class="faq-a"><a href="Soap LAB Report.pdf" target="_blank">📄 View Test Report</a></div></div>
<div class="faq-item"><div class="faq-q">Charcoal Soap</div><div class="faq-a"><a href="Soap LAB Report.pdf" target="_blank">📄 View Test Report</a></div></div>
<div class="faq-item"><div class="faq-q">Alum Soap</div><div class="faq-a"><a href="Soap LAB Report.pdf" target="_blank">📄 View Test Report</a></div></div>
<div class="faq-item"><div class="faq-q">Kapoor Soap</div><div class="faq-a"><a href="Soap LAB Report.pdf" target="_blank">📄 View Test Report</a></div></div>
<div class="faq-item"><div class="faq-q">Goat Milk Soap</div><div class="faq-a"><a href="Soap LAB Report.pdf" target="_blank">📄 View Test Report</a></div></div>
</div>
</div>

<footer>
📞 <a href="tel:8888942084">8888942084</a> |
💬 <a href="https://wa.me/918888942084">WhatsApp</a> |
📧 <a href="mailto:mgayurvedicc@gmail.com">Email</a>
<br>© MG Manisha Glow Ayurvedic
</footer>

</div>

<script>
function calc(){
 total.value=(neem.value*50)+(charcoal.value*50)+(alum.value*50)+(kapoor.value*50)+(goat.value*50);
}
document.querySelectorAll("input[type=number]").forEach(i=>i.oninput=calc);

function order(){
 let msg=`New Order
Neem: ${neem.value}
Charcoal: ${charcoal.value}
Alum: ${alum.value}
Kapoor: ${kapoor.value}
Goat Milk: ${goat.value}
Total: ₹${total.value}
Name: ${name.value}
Phone: ${phone.value}
Address: ${address.value}`;
 window.open("https://wa.me/918888942084?text="+encodeURIComponent(msg));
}

function toggleReports(){
 let r=document.getElementById("reports");
 r.style.display=r.style.display==="none"?"block":"none";
}
</script>

</body>
</html>
