<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>🌿 MG Manisha Glow Ayurvedic</title>

<style>
body{
    margin:0;
    font-family:Arial, sans-serif;
    background:#fffdf9;
    position:relative;
}
body::before{
    content:"";
    position:fixed;
    inset:0;
    background:url('main-logo.jpg') center/500px no-repeat;
    opacity:0.1;
    z-index:-1;
}
.container{max-width:1100px;margin:auto;padding:20px}
h1,h2{text-align:center;color:#1f3812}
.products{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:16px}
.card{
    background:#ffffffee;
    border-radius:14px;
    padding:18px;
    box-shadow:0 6px 18px rgba(0,0,0,.1)
}
.card h3{margin:0;color:#2d5d2a}
.small{font-size:14px;color:#444}
.ingredients{font-size:13px;margin-top:6px;color:#333}
.card input{width:100%;padding:8px;margin-top:8px;border-radius:6px;border:1px solid #aaa}

.order-box,.section{
    max-width:600px;
    margin:30px auto;
    background:#ffffffee;
    padding:18px;
    border-radius:14px;
    box-shadow:0 6px 18px rgba(0,0,0,.1)
}
.order-box input,.order-box textarea{
    width:100%;
    padding:8px;
    margin-top:8px;
    border-radius:6px;
    border:1px solid #aaa
}
.btn{
    background:#6b8e23;
    color:#fff;
    border:none;
    width:100%;
    padding:10px;
    margin-top:12px;
    border-radius:6px;
    cursor:pointer
}
.faq-item{margin-top:10px}
.faq-q{
    cursor:pointer;
    font-weight:bold;
    color:#1f3812
}
.faq-a{display:none;font-size:14px;color:#333;margin-top:4px}
footer{text-align:center;margin:30px 0;color:#555}
a{color:#2f6d2f;text-decoration:none;font-weight:bold}
</style>
</head>

<body>
<div class="container">

<h1>🌿 MG Manisha Glow Ayurvedic</h1>
<h2>Premium Home-Made Ayurvedic Products</h2>

<h2>🧼 Soap Collection (₹50 Each)</h2>

<div class="products">

<div class="card">
<h3>🍃 Neem Tulsi Ayurvedic Soap</h3>
<div class="small">For Face & Body</div>
<div class="ingredients">
<b>Ingredients:</b> Activated Neem Tulsi Base, Neem Tulsi Juice (Extract), Glycerin,
Vitamin E Capsule, Castor Oil, Vitamin C Serum, Fragrance Oil
</div>
<input type="number" id="neem" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>🖤 Charcoal Ayurvedic Soap</h3>
<div class="small">For Face & Body</div>
<div class="ingredients">
<b>Ingredients:</b> Activated Charcoal Base, Natural Oil, Glycerin,
Vitamin E Capsule, Aloe Vera Gel, Fragrance Oil
</div>
<input type="number" id="charcoal" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>Turti (Alum / Fitkari) Ayurvedic Soap</h3>
<div class="small">For Face & Body</div>
<div class="ingredients">
<b>Ingredients:</b> Activated Turti (Alum) Base, Honey, Aloe Vera Gel, Glycerin
</div>
<input type="number" id="alum" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>Camphor (Kapoor) Ayurvedic Soap</h3>
<div class="small">For Face & Body</div>
<div class="ingredients">
<b>Ingredients:</b> Activated Kapoor Base, Bhim Seni Camphor,
Glycerin, Coconut Oil
</div>
<input type="number" id="kapoor" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>🥛 Goat Milk Ayurvedic Soap</h3>
<div class="small">For Face & Body</div>
<div class="ingredients">
<b>Ingredients:</b> Activated Goat Milk Base, Aloe Vera Gel, Castor Oil,
Raw Goat Milk, Almond Oil, Fragrance Oil
</div>
<input type="number" id="goat" min="0" placeholder="Quantity">
</div>

</div>

<div class="order-box">
<h2>📝 Order Details</h2>
<input type="text" id="name" placeholder="Your Name">
<input type="text" id="phone" placeholder="Phone Number">
<textarea id="address" placeholder="Full Address"></textarea>
<input type="text" id="total" placeholder="Total Amount (Auto)" readonly>
<button class="btn" onclick="order()">📩 WhatsApp Order</button>
</div>

<div class="section">
<h2>🌿 How to Use for Better Results</h2>
<ul>
<li><b>Lather:</b> Apply to wet face or skin</li>
<li><b>Massage:</b> Rub gently for 30 seconds</li>
<li><b>Rinse:</b> Wash off and pat dry</li>
</ul>
</div>

<div class="section">
<h2>❓ Frequently Asked Questions</h2>

<div class="faq-item">
<div class="faq-q" onclick="toggle(this)">▶ How are our Ayurvedic products made?</div>
<div class="faq-a">We use traditional herbs, natural oils and age-old formulations.</div>
</div>

<div class="faq-item">
<div class="faq-q" onclick="toggle(this)">▶ What skin types are these suitable for?</div>
<div class="faq-a">Suitable for oily, dry, sensitive & combination skin.</div>
</div>

<div class="faq-item">
<div class="faq-q" onclick="toggle(this)">▶ How long does it take to see results?</div>
<div class="faq-a">Best results with consistent use for 6 months.</div>
</div>

<div class="faq-item">
<div class="faq-q" onclick="toggle(this)">▶ Delivery & Shipping policy?</div>
<div class="faq-a">Orders processed in 2-3 days, delivered in 5-7 days.</div>
</div>
</div>

<div class="section">
<h2>📦 Track Your Order</h2>
<p>
Enter your India Post Tracking ID here:<br>
<a href="https://www.indiapost.gov.in/_layouts/15/dop.portal.tracking/trackconsignment.aspx" target="_blank">
👉 Track on India Post Website
</a>
</p>
</div>

<footer>
<p>
📞 <a href="tel:8888942084">8888942084</a> |
💬 <a href="https://wa.me/918888942084" target="_blank">WhatsApp</a> |
📧 <a href="mailto:mgayurvedicc@gmail.com">Email</a> |
📸 <a href="https://instagram.com/mg_manisha_glow_Ayurvedic_" target="_blank">Instagram</a> |
🌐 <a href="https://mgayurvedicc-ui.github.io/MG-Manisha-Glow-Ayurvedic/" target="_blank">Website</a>
</p>
© MG Manisha Glow Ayurvedic
</footer>

</div>

<script>
function calc(){
 let t =
 (neem.value*50)+(charcoal.value*50)+(alum.value*50)+(kapoor.value*50)+(goat.value*50);
 total.value=t;
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
function toggle(el){
 let a=el.nextElementSibling;
 a.style.display=a.style.display=="block"?"none":"block";
}
</script>
</body>
</html>
