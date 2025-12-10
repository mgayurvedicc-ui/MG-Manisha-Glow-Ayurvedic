<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MG Manisha Glow Ayurvedic</title>

<!-- Premium Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600;700&family=Playfair+Display:wght@500;700&display=swap" rel="stylesheet">

<style>

/* ROOT COLORS */
:root {
  --bg1: #e9f3ea;
  --bg2: #d0e8d2;
  --bg3: #e8f8e5;
  --text: #1f3b1f;
  --accent: #4b7f39;
  --accent2: #2f5e28;
  --card: rgba(255,255,255,0.93);
  --gold: #b58e43;
}

/* BODY STYLING */
body {
  margin: 0;
  padding: 0;
  font-family: "Cormorant Garamond", serif;
  background: var(--bg1);
  color: var(--text);
  overflow-x: hidden;
}

/* MOVING GRADIENT LIGHT FLOW */
body::before {
  content: "";
  position: fixed;
  inset: 0;
  background: linear-gradient(
     120deg,
     rgba(200,255,200,0.25),
     rgba(150,200,150,0.25),
     rgba(220,255,220,0.25)
  );
  animation: glow 10s infinite alternate ease-in-out;
  z-index: -2;
}
@keyframes glow {
  0% { filter: blur(40px); opacity: .6; }
  100% { filter: blur(70px); opacity: .9; }
}

/* Background Logo Watermark */
body::after {
  content: "";
  position: fixed;
  inset: 0;
  background-image: url('main-logo.jpg');
  background-size: 650px;
  background-repeat: no-repeat;
  background-position: center;
  opacity: 0.10;
  z-index: -1;
}

/* HEADER */
.header {
  text-align: center;
  padding: 45px 20px;
  background: transparent;
}

.header h1 {
  font-size: 48px;
  font-weight: 700;
  color: var(--accent2);
  text-shadow: 0 3px 10px rgba(0,0,0,.15);
  font-family: "Playfair Display", serif;
}

.header h2 {
  margin-top: 5px;
  font-size: 20px;
  color: var(--accent);
}

/* CONTAINER */
.container {
  max-width: 1150px;
  margin: auto;
  padding: 20px;
}

/* TITLES */
.section-title {
  text-align: center;
  font-size: 28px;
  margin-top: 40px;
  color: var(--accent2);
  font-weight: 700;
}

/* GRID */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px,1fr));
  gap: 22px;
}

/* CARDS */
.card {
  background: var(--card);
  padding: 16px;
  border-radius: 14px;
  box-shadow: 0 10px 25px rgba(0,0,0,.10);
  transition: .3s;
  border: 1px solid rgba(120,150,120,0.3);
}
.card:hover { transform: translateY(-6px); }

/* PRODUCT THUMBNAILS */
.thumb {
  height: 150px;
  border-radius: 14px;
  background-size: cover;
  background-position: center;
  margin-bottom: 12px;
}

/* INPUT */
.card input {
  width: 100%;
  padding: 10px;
  border-radius: 10px;
  border: 1px solid #bbb;
  font-size: 16px;
  font-family: "Poppins", sans-serif;
}

/* ORDER BOX */
.order-box {
  background: var(--card);
  padding: 22px;
  border-radius: 16px;
  margin: 40px auto;
  max-width: 720px;
  box-shadow: 0 10px 25px rgba(0,0,0,.1);
  border: 1px solid rgba(120,150,120,0.3);
}

.order-box input,
.order-box textarea {
  width: 100%;
  padding: 12px;
  margin-top: 10px;
  border-radius: 10px;
  border: 1px solid #bbb;
  background: #f9f9f9;
  font-family: "Poppins", sans-serif;
  font-size: 16px;
}

textarea { height: 75px; }

.total-line {
  font-size: 24px;
  margin-top: 15px;
  font-weight: 600;
  color: var(--accent2);
}

/* BUTTON */
.btn {
  width: 100%;
  background: var(--accent);
  color: white;
  padding: 14px;
  border: none;
  border-radius: 12px;
  margin-top: 18px;
  font-size: 18px;
  cursor: pointer;
  transition: .3s;
}
.btn:hover { background: var(--accent2); }

/* CONTACT DETAILS - PREMIUM STYLE */
.contact-box {
  margin-top: 50px;
  padding: 25px;
  border-radius: 16px;
  background: var(--card);
  box-shadow: 0 10px 25px rgba(0,0,0,.12);
  border-left: 5px solid var(--gold);
  border-right: 5px solid var(--gold);
  font-size: 18px;
  line-height: 1.8;
}

.contact-box b {
  color: var(--accent2);
  font-size: 20px;
}

/* FOOTER */
.footer {
  text-align: center;
  padding: 25px;
  font-size: 17px;
  color: var(--accent2);
}

</style>
</head>

<body>

<!-- HEADER -->
<div class="header">
  <h1>MG Manisha Glow Ayurvedic</h1>
  <h2>Pure • Natural • Herbal Wellness</h2>
</div>

<div class="container">

<!-- SOAP SECTION -->
<h3 class="section-title">🧼 Soap Collection — ₹50</h3>

<div class="grid">

<!-- Neem -->
<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1582719478244-ff65d3f7b7a3?auto=format&fit=crop&w=800')"></div>
<h3>🍃 Neem Soap</h3>
<input type="number" data-price="50" data-name="Neem Soap" min="0">
</div>

<!-- Tulasi -->
<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1501004318641-b39e6451bec6?auto=format&fit=crop&w=800')"></div>
<h3>🌿 Tulasi Soap</h3>
<input type="number" data-price="50" data-name="Tulasi Soap" min="0">
</div>

<!-- Aloe -->
<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1560264280-2ace7a2b4f0f?auto=format&fit=crop&w=800')"></div>
<h3>🍀 Aloe Vera Soap</h3>
<input type="number" data-price="50" data-name="Aloe Vera Soap" min="0">
</div>

<!-- Goat -->
<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1579710757331-0a7f9d3d1e40?auto=format&fit=crop&w=800')"></div>
<h3>🥛 Goat Milk Soap</h3>
<input type="number" data-price="50" data-name="Goat Milk Soap" min="0">
</div>

<!-- Charcoal -->
<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1529921879218-1f6b61c95ef8?auto=format&fit=crop&w=800')"></div>
<h3>🖤 Charcoal Soap</h3>
<input type="number" data-price="50" data-name="Charcoal Soap" min="0">
</div>

<!-- Turmeric -->
<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1581091012184-7a7f9d3d1e40?auto=format&fit=crop&w=800')"></div>
<h3>✨ Turmeric Soap</h3>
<input type="number" data-price="50" data-name="Turmeric Soap" min="0">
</div>

<!-- Rice -->
<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1556228453-3c9cc9f7d7b9?auto=format&fit=crop&w=800')"></div>
<h3>🍚 Rice Potato Soap</h3>
<input type="number" data-price="50" data-name="Rice Potato Soap" min="0">
</div>

<!-- Bheem -->
<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1603575448399-e8a37d6b7d77?auto=format&fit=crop&w=800')"></div>
<h3>Bheem Sen Kapur Soap</h3>
<input type="number" data-price="50" data-name="Bheem Sen Kapur Soap" min="0">
</div>

</div>

<!-- FACE PACK -->
<h3 class="section-title">🌸 Face Pack Collection — ₹30</h3>

<div class="grid">

<!-- Neem Face Pack -->
<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1598531371365-6b7f1f6d4c9b?auto=format&fit=crop&w=800')"></div>
<h3>🍃 Neem Leaf Powder</h3>
<input type="number" data-price="30" data-name="Neem Leaf Powder" min="0">
</div>

<!-- Moisturizer Cream -->
<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1542444459-db8a1b2d7b2a?auto=format&fit=crop&w=800')"></div>
<h3>💧 Moisturizer Cream</h3>
<input type="number" data-price="30" data-name="Moisturizer Cream" min="0">
</div>

</div>

<!-- ORDER BOX -->
<div class="order-box">
<h3 style="text-align:center;">📝 Order Summary</h3>

<input id="custName" placeholder="👤 Your Name">
<input id="custPhone" placeholder="📞 Phone Number">
<textarea id="custAddr" placeholder="🏠 Full Delivery Address"></textarea>

<div class="total-line">Total: <span id="grandTotal">₹0</span></div>

<button class="btn" onclick="placeOrder()">📩 WhatsApp Order</button>
</div>

<!-- CONTACT BOX -->
<div class="contact-box">
<b>MG Manisha Glow Ayurvedic</b><br>
📞 Mobile: 8888942084<br>
💬 WhatsApp: 8888942084<br>
📍 Address: At Post Rawande, Tal Kopargaon, Dist Ahilyanagar 423601<br>
✉ Email: mgayurvedicc@gmail.com <br>
📸 Instagram: @mg_manisha_glow_Ayurvedic_ <br>
🌐 Website: https://mgayurvedicc-ui.github.io/MG-Manisha-Glow-Ayurvedic/
</div>

<div class="footer">
© <span id="yr"></span> MG Manisha Glow Ayurvedic 🌿
</div>

</div>


<script>
document.getElementById("yr").textContent = new Date().getFullYear();

/* AUTO TOTAL CALCULATION */
function calcTotal() {
  let total = 0;
  document.querySelectorAll("input[type='number']").forEach(i => {
    total += (parseInt(i.value) || 0) * parseInt(i.dataset.price);
  });
  document.getElementById("grandTotal").innerText = "₹" + total;
  return total;
}

document.querySelectorAll("input[type='number']").forEach(i =>
  i.addEventListener("input", calcTotal)
);

/* SEND ORDER */
function placeOrder() {
  const name = custName.value.trim();
  const phone = custPhone.value.trim();
  const addr = custAddr.value.trim();
  const total = calcTotal();

  if(!name || !phone || !addr){
    alert("कृपया Name, Phone और Address भरें!");
    return;
  }

  let items = [];
  document.querySelectorAll("input[type='number']").forEach(i=>{
    if(parseInt(i.value) > 0) {
      items.push(i.dataset.name + " — " + i.value);
    }
  });

  let msg =
`🧾 *New Order*
--------------------
${items.join("\n")}
--------------------
💰 *Total:* ₹${total}

👤 *Name:* ${name}
📞 *Phone:* ${phone}
🏠 *Address:* ${addr}`;

  window.open("https://wa.me/918888942084?text=" + encodeURIComponent(msg));
}
</script>

</body>
</html>
