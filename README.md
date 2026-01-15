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
    overflow-x:hidden;
}
body::before{
    content:"";
    position:fixed;
    inset:0;
    background:url('main-logo.jpg') center/520px no-repeat;
    opacity:0.12;
    z-index:-1;
}
.container{max-width:1100px;margin:auto;padding:20px}
h1,h2{text-align:center;color:#1f3812}
.products,.facepack{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:15px}
.card{
    background:rgba(255,255,255,.92);
    border-radius:14px;
    padding:18px;
    box-shadow:0 6px 18px rgba(0,0,0,.1)
}
.card small{color:#444}
.card input{width:100%;padding:8px;margin-top:8px;border-radius:6px;border:1px solid #aaa}

.order-box{
    max-width:520px;margin:30px auto;
    background:#fff;padding:16px;border-radius:14px;
    box-shadow:0 6px 18px rgba(0,0,0,.1)
}
.order-box input,.order-box textarea{
    width:100%;padding:8px;margin-top:8px;border-radius:6px;border:1px solid #aaa
}
.btn{
    width:100%;margin-top:12px;
    background:#2f6b2f;color:#fff;
    border:none;padding:10px;border-radius:6px;cursor:pointer
}

.section{
    margin-top:40px;
    background:#ffffffeb;
    padding:20px;border-radius:14px;
    box-shadow:0 6px 18px rgba(0,0,0,.08)
}

/* FAQ */
.faq-item{border-bottom:1px solid #ccc;padding:10px 0}
.faq-q{cursor:pointer;font-weight:bold}
.faq-a{display:none;padding-top:6px;color:#333}

/* Links */
a{color:#1f6b3a;text-decoration:none;font-weight:bold}
footer{text-align:center;margin:30px 0;color:#666}
</style>
</head>

<body>
<div class="container">

<h1>🌿 MG Manisha Glow Ayurvedic</h1>
<h2>Premium Home-Made Ayurvedic Products</h2>

<!-- SOAP SECTION -->
<h2>🧼 Soap Collection (₹50 Each)</h2>
<div class="products">

<div class="card">
<h3>🍃 Neem Tulsi Ayurvedic Soap</h3>
<small>For Face & Body</small>
<p><b>Ingredients:</b> Neem Extract, Tulsi Leaves, Coconut Oil, Herbal Base</p>
<input type="number" id="neemtulsi" min="0" placeholder="Quantity">
</div>

<div class="card">
<h3>🖤 Charcoal Ayurvedic Soap</h3>
<small>For Face & Body</small>
<p><b>Ingredients:</b> Activated Charcoal, Tea Tree Oil, Coconut Oil</p>
<input type="number" id="charcoal" min="0">
</div>

<div class="card">
<h3>🧂 Alum (Turti) Ayurvedic Soap</h3>
<small>For Face & Body</small>
<p><b>Ingredients:</b> Potash Alum, Neem Oil, Herbal Base</p>
<input type="number" id="alum" min="0">
</div>

<div class="card">
<h3>Bheem Sen Kapur Ayurvedic Soap</h3>
<small>For Face & Body</small>
<p><b>Ingredients:</b> Natural Kapur, Cooling Herbs, Coconut Oil</p>
<input type="number" id="kapur" min="0">
</div>

<div class="card">
<h3>🥛 Goat Milk Ayurvedic Soap</h3>
<small>For Face & Body</small>
<p><b>Ingredients:</b> Fresh Goat Milk, Olive Oil, Shea Butter</p>
<input type="number" id="goat" min="0">
</div>

</div>

<!-- FACE PACK -->
<h2>🌸 Face Pack (₹30 Each)</h2>
<div class="facepack">
<div class="card">
<h3>Neem Leaf Powder</h3>
<input type="number" id="nfp" min="0">
</div>
<div class="card">
<h3>Moisturizer Cream</h3>
<input type="number" id="mfp" min="0">
</div>
</div>

<!-- HOW TO USE -->
<div class="section">
<h2>🧴 How To Use For Better Results</h2>
<ul>
<li><b>Lather:</b> Apply to wet face or skin</li>
<li><b>Massage:</b> Rub gently for 30 seconds</li>
<li><b>Rinse:</b> Wash thoroughly and pat dry</li>
</ul>
</div>

<!-- ORDER -->
<div class="order-box">
<h2>📝 Customer Details</h2>
<input id="name" placeholder="Your Name">
<input id="phone" placeholder="Phone Number">
<textarea id="address" placeholder="Full Address"></textarea>
<input id="total" placeholder="Total Amount (Auto)" readonly>
<button class="btn" onclick="order()">📩 WhatsApp Order</button>
</div>

<!-- TRACK ORDER -->
<div class="section">
<h2>📦 Track Your Order</h2>
<form action="https://www.indiapost.gov.in/_layouts/15/DOP.Portal.Tracking/TrackConsignment.aspx" target="_blank">
<input placeholder="Enter India Post Tracking ID">
<button class="btn" type="submit">Track Order</button>
</form>
</div>

<!-- FAQ -->
<div class="section">
<h2>❓ Frequently Asked Questions</h2>

<div class="faq-item">
<div class="faq-q" onclick="toggle(this)">▶ How are our Ayurvedic products made?</div>
<div class="faq-a">We use traditional herbs, natural oils and age-old formulations.</div>
</div>

<div class="faq-item">
<div class="faq-q" onclick="toggle(this)">▶ What skin types are suitable?</div>
<div class="faq-a">Suitable for oily, dry, sensitive & combination skin.</div>
</div>

<div class="faq-item">
<div class="faq-q" onclick="toggle(this)">▶ How long to see results?</div>
<div class="faq-a">Recommended consistent use for 6 months.</div>
</div>

<div class="faq-item">
<div class="faq-q" onclick="toggle(this)">▶ Delivery & Shipping Policy?</div>
<div class="faq-a">Processing in 2-3 days, delivery in 5-7 days.</div>
</div>

</div>

<!-- CONTACT -->
<div class="section">
<h2>📞 Contact Us</h2>
<p>📱 <a href="tel:8888942084">8888942084</a></p>
<p>💬 <a href="https://wa.me/918888942084" target="_blank">WhatsApp</a></p>
<p>📧 <a href="mailto:mgayurvedicc@gmail.com">mgayurvedicc@gmail.com</a></p>
<p>📸 <a href="https://instagram.com/mg_manisha_glow_Ayurvedic_" target="_blank">Instagram</a></p>
<p>🌐 <a href="https://mgayurvedicc-ui.github.io/MG-Manisha-Glow-Ayurvedic/" target="_blank">Website</a></p>
</div>

<footer>© MG Manisha Glow Ayurvedic 🌿</footer>

</div>

<script>
function toggle(e){
    let a=e.nextElementSibling;
    a.style.display=a.style.display==="block"?"none":"block";
}
function calc(){
let t=
(neemtulsi.value*50)+(charcoal.value*50)+(alum.value*50)+(kapur.value*50)+(goat.value*50)
+(nfp.value*30)+(mfp.value*30);
total.value=t;
}
document.querySelectorAll("input[type=number]").forEach(i=>i.oninput=calc);

function order(){
let msg=`New Order
Total ₹${total.value}
Name: ${name.value}
Phone: ${phone.value}
Address: ${address.value}`;
window.open("https://wa.me/918888942084?text="+encodeURIComponent(msg));
}
</script>
</body>
</html>
