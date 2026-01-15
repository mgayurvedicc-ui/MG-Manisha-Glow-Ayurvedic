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

/* watermark logo */
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
.card h3{
    margin:0;
    color:#eaf6ef;
}
.small{
    font-size:14px;
    color:#cde7d7;
}
.ingredients{
    font-size:13px;
    margin-top:6px;
    color:#d8efe4;
}
.card input{
    width:100%;
    margin-top:10px;
    padding:8px;
    border-radius:6px;
    border:none;
}

/* smaller order box */
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
    font-size:14px;
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

/* sections */
.section{
    max-width:700px;
    margin:40px auto;
    background:rgba(20,63,42,.95);
    padding:22px;
    border-radius:18px;
    border:1px solid rgba(201,162,77,.35);
}

/* FAQ visible answers */
.faq-item{
    margin-top:14px;
}
.faq-q{
    font-weight:bold;
    color:#e7c76a;
}
.faq-a{
    font-size:14px;
    color:#d8efe4;
    margin-top:6px;
    line-height:1.6;
}

footer{
    text-align:center;
    margin:40px 0;
    font-size:14px;
    color:#cde7d7;
}
footer a{
    color:#e7c76a;
    text-decoration:none;
    font-weight:bold;
}
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
<div class="ingredients">
<b>Ingredients:</b> Activated Neem Tulsi Base, Neem Tulsi Extract, Glycerin,
Vitamin E, Castor Oil, Vitamin C Serum, Fragrance Oil
</div>
<input type="number" id="neem" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>🖤 Charcoal Ayurvedic Soap</h3>
<div class="small">For Face & Body</div>
<div class="ingredients">
<b>Ingredients:</b> Activated Charcoal Base, Natural Oils, Glycerin,
Aloe Vera Gel, Vitamin E
</div>
<input type="number" id="charcoal" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>Turti (Alum) Ayurvedic Soap</h3>
<div class="small">For Face & Body</div>
<div class="ingredients">
<b>Ingredients:</b> Activated Alum Base, Honey, Aloe Vera Gel, Glycerin
</div>
<input type="number" id="alum" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>Camphor (Kapoor) Ayurvedic Soap</h3>
<div class="small">For Face & Body</div>
<div class="ingredients">
<b>Ingredients:</b> Activated Kapoor Base, Bhim Seni Camphor,
Coconut Oil, Glycerin
</div>
<input type="number" id="kapoor" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>🥛 Goat Milk Ayurvedic Soap</h3>
<div class="small">For Face & Body</div>
<div class="ingredients">
<b>Ingredients:</b> Activated Goat Milk Base, Raw Goat Milk,
Aloe Vera Gel, Almond Oil, Castor Oil
</div>
<input type="number" id="goat" min="0" placeholder="Quantity">
</div>

</div>

<!-- ORDER -->
<div class="order-box">
<h2>📝 Order Details</h2>
<input type="text" id="name" placeholder="Your Name">
<input type="text" id="phone" placeholder="Phone Number">
<textarea id="address" placeholder="Full Address"></textarea>
<input type="text" id="total" placeholder="Total Amount (Auto)" readonly>
<button class="btn" onclick="order()">📩 WhatsApp Order</button>
</div>

<!-- HOW TO USE -->
<div class="section">
<h2>🌿 How to Use for Better Results</h2>
<ul>
<li><b>Lather:</b> Apply to wet face or skin</li>
<li><b>Massage:</b> Rub gently for 30 seconds</li>
<li><b>Rinse:</b> Wash off thoroughly and pat dry</li>
</ul>
</div>

<!-- FAQ -->
<div class="section">
<h2>❓ Frequently Asked Questions</h2>

<div class="faq-item">
<div class="faq-q">How are our Ayurvedic products made?</div>
<div class="faq-a">
We make our Ayurvedic products using traditional herbs, natural oils,
and pure ingredients following age-old formulations.
</div>
</div>

<div class="faq-item">
<div class="faq-q">What skin types are our products suitable for?</div>
<div class="faq-a">
Our products are suitable for oily, dry, sensitive and combination skin
without causing irritation.
</div>
</div>

<div class="faq-item">
<div class="faq-q">How long does it take to see results?</div>
<div class="faq-a">
For best results, use consistently for 6 months. Many customers notice
visible improvement within a few weeks.
</div>
</div>

<div class="faq-item">
<div class="faq-q">What is your delivery and shipping policy?</div>
<div class="faq-a">
Orders are processed in 2–3 business days and delivered within 5–7 days
depending on location.
</div>
</div>
</div>

<!-- TRACK ORDER -->
<div class="section">
<h2>📦 Track Your Order</h2>
<p>
<a href="https://www.indiapost.gov.in/home" target="_blank">
👉 Track Order via India Post
</a>
</p>
</div>

<footer>
📞 <a href="tel:8888942084">8888942084</a> |
💬 <a href="https://wa.me/918888942084" target="_blank">WhatsApp</a> |
📧 <a href="mailto:mgayurvedicc@gmail.com">Email</a> |
📸 <a href="https://instagram.com/mg_manisha_glow_Ayurvedic_" target="_blank">Instagram</a> |
🌐 <a href="https://mgayurvedicc-ui.github.io/MG-Manisha-Glow-Ayurvedic/" target="_blank">Website</a>
<br><br>
© MG Manisha Glow Ayurvedic
</footer>

</div>

<script>
function calc(){
 total.value =
 (neem.value*50)+(charcoal.value*50)+(alum.value*50)+(kapoor.value*50)+(goat.value*50);
}
document.querySelectorAll("input[type=number]").forEach(i=>i.oninput=calc);

function order(){
 let msg=`New Order
Neem Tulsi: ${neem.value}
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
</script>

</body>
</html>
