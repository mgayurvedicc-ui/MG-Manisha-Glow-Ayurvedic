<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MG Manisha Glow Ayurvedic</title>

<style>

/* FONT */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap');

/* ROOT COLORS */
:root {
  --bg: #faf7ef;
  --text: #2f3b26;
  --card: rgba(255,255,255,0.95);
  --shadow: rgba(0,0,0,0.1);
  --accent: #75a96c;
  --accent2: #4a6d3c;
}

body.dark {
  --bg: #1c1f1d;
  --text: #e9f5e1;
  --card: rgba(32,35,33,0.95);
  --shadow: rgba(0,0,0,0.4);
  --accent: #8bd48e;
  --accent2: #5ebf69;
}

/* BODY */
body {
    margin: 0;
    padding: 0;
    background: var(--bg);
    font-family: "Poppins", sans-serif;
    color: var(--text);
    transition: 0.4s;
}

/* BACKGROUND LOGO WATERMARK */
body::before {
    content: "";
    position: fixed;
    inset: 0;
    background-image: url('main-logo.jpg'); /* ← आपका दिया हुआ LOGO */
    background-position: center;
    background-repeat: no-repeat;
    background-size: 650px;
    opacity: 0.11;  /* Light watermark effect */
    z-index: -1;
}

/* DARK MODE BUTTON */
.toggle-btn {
    position: fixed;
    top: 15px;
    right: 15px;
    background: var(--accent);
    padding: 10px 16px;
    border-radius: 50px;
    color: white;
    cursor: pointer;
    font-size: 14px;
    font-weight: 600;
    box-shadow: 0 4px 12px var(--shadow);
    z-index: 10;
}

/* HEADER */
.header {
    background-image: url('https://images.unsplash.com/photo-1590393804594-2b51d7c5ee54?auto=format&fit=crop&w=1400&q=60');
    background-size: cover;
    background-position: center;
    padding: 45px 20px;
    text-align: center;
    color: white;
    border-radius: 0 0 18px 18px;
}
.header h1 { font-size: 36px; font-weight: 700; }
.header h2 { margin-top: 8px; font-size: 20px; }

/* CONTAINER */
.container { max-width: 1150px; margin: auto; padding: 20px; }

.section-title { text-align:center; font-size:24px; color:var(--accent2); }

/* GRID */
.grid {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
  gap:20px;
}

/* CARD */
.card {
  background: var(--card);
  padding: 16px;
  border-radius: 14px;
  box-shadow: 0 10px 25px var(--shadow);
  transition: .3s;
}
.card:hover { transform: translateY(-6px); }

.thumb {
  height: 140px;
  border-radius: 12px;
  background-size: cover;
  background-position: center;
  margin-bottom: 10px;
}

/* INPUT */
.card input {
  width: 100%;
  padding: 10px;
  border-radius: 8px;
  border: 1px solid #ccc;
  background: var(--bg);
  color: var(--text);
}

/* ORDER BOX */
.order-box {
  margin: 30px auto;
  background: var(--card);
  padding: 20px;
  border-radius: 15px;
  width: 100%;
  max-width: 720px;
  box-shadow: 0 10px 25px var(--shadow);
}

.order-box input, .order-box textarea {
  width: 100%;
  padding: 10px;
  border-radius: 10px;
  border: 1px solid #ccc;
  background: var(--bg);
  color: var(--text);
}

textarea { height: 65px; }

.btn {
  width: 100%;
  background: var(--accent);
  color: white;
  border: none;
  padding: 14px;
  margin-top: 15px;
  border-radius: 10px;
  font-size: 17px;
  cursor: pointer;
}
.btn:hover { background: var(--accent2); }

/* COMPANY DETAILS */
.company-full {
  margin-top: 40px;
  padding: 25px;
  border-radius: 14px;
  background: var(--card);
  box-shadow: 0 10px 25px var(--shadow);
}
.company-full b { color: var(--accent2); }

/* FOOTER */
.footer {
  text-align:center;
  padding: 15px;
  color: var(--accent2);
}

</style>
</head>

<body>

<div class="toggle-btn" onclick="toggleDark()">🌙 Dark / ☀️ Light</div>

<!-- HEADER -->
<div class="header">
    <h1>🌿 MG Manisha Glow Ayurvedic</h1>
    <h2>Pure · Natural · Herbal Wellness</h2>
</div>

<div class="container">

<!-- SOAP -->
<h3 class="section-title">🧼 Soap Collection — ₹50</h3>

<div class="grid">

<!-- Soap Cards Same -->
<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1582719478244-ff65d3f7b7a3?auto=format&fit=crop&w=800&q=60')"></div>
<h3>🍃 Neem Soap</h3>
<input type="number" data-price="50" data-name="Neem Soap" min="0">
</div>

<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1501004318641-b39e6451bec6?auto=format&fit=crop&w=800&q=60')"></div>
<h3>🌿 Tulasi Soap</h3>
<input type="number" data-price="50" data-name="Tulasi Soap" min="0">
</div>

<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1560264280-2ace7a2b4f0f?auto=format&fit=crop&w=800&q=60')"></div>
<h3>🍀 Aloe Vera Soap</h3>
<input type="number" data-price="50" data-name="Aloe Vera Soap" min="0">
</div>

<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1579710757331-0a7f9d3d1e40?auto=format&fit=crop&w=800&q=60')"></div>
<h3>🥛 Goat Milk Soap</h3>
<input type="number" data-price="50" data-name="Goat Milk Soap" min="0">
</div>

<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1529921879218-1f6b61c95ef8?auto=format&fit=crop&w=800&q=60')"></div>
<h3>🖤 Charcoal Soap</h3>
<input type="number" data-price="50" data-name="Charcoal Soap" min="0">
</div>

<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1581091012184-7a7a1d0f6a6a?auto=format&fit=crop&w=800&q=60')"></div>
<h3>✨ Turmeric Soap</h3>
<input type="number" data-price="50" data-name="Turmeric Soap" min="0">
</div>

<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1556228453-3c9cc9f3d0b9?auto=format&fit=crop&w=800&q=60')"></div>
<h3>🍚 Rice Potato Soap</h3>
<input type="number" data-price="50" data-name="Rice Potato Soap" min="0">
</div>

<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1603575448399-e8a37d6b7d77?auto=format&fit=crop&w=800&q=60')"></div>
<h3>Bheem Sen Kapur Soap</h3>
<input type="number" data-price="50" data-name="Bheem Sen Kapur Soap" min="0">
</div>

</div>

<!-- FACE PACK -->
<h3 class="section-title">🌸 Face Pack Collection — ₹30</h3>

<div class="grid">

<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1598531371365-6b7f1f6d4c9b?auto=format&fit=crop&w=800&q=60')"></div>
<h3>🍃 Neem Leaf Powder</h3>
<input type="number" data-price="30" data-name="Neem Leaf Powder" min="0">
</div>

<div class="card">
<div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1542444459-db8a1b2d7b2a?auto=format&fit=crop&w=800&q=60')"></div>
<h3>💧 Moisturizer Cream</h3> <!-- UPDATED NAME -->
<input type="number" data-price="30" data-name="Moisturizer Cream" min="0">
</div>

</div>

<!-- ORDER BOX -->
<div class="order-box">
<h3>📝 Order Summary</h3>

<input id="custName" placeholder="👤 Your Name">
<input id="custPhone" placeholder="📞 Phone Number">
<textarea id="custAddr" placeholder="🏠 Full Delivery Address"></textarea>

<div style="margin-top:12px;font-size:20px;">
<b>Total: </b><span id="grandTotal">₹0</span>
</div>

<button class="btn" onclick="placeOrder()">📩 WhatsApp Order</button>
</div>

<!-- COMPANY DETAILS -->
<div class="company-full">

<b>✔ Contact Name:</b> MG Manisha Glow Ayurvedic<br>
<b>✔ Mobile Number:</b> 8888942084<br>
<b>✔ WhatsApp Number:</b> 8888942084<br>
<b>✔ Address:</b> At Post Rawande, Tal Kopargaon, Dist Ahilyanagar 423601<br>
<b>✔ Email:</b> mgayurvedicc@gmail.com<br>
<b>✔ Instagram ID:</b> @mg_manisha_glow_Ayurvedic_<br>
<b>✔ Website:</b> https://mgayurvedicc-ui.github.io/MG-Manisha-Glow-Ayurvedic/

</div>

<div class="footer">
© <span id="yr"></span> MG Manisha Glow Ayurvedic 🌿
</div>

</div>

<script>
document.getElementById("yr").textContent = new Date().getFullYear();

/* AUTO TOTAL */
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
`🧾 *New Order Received*

📦 *Products:*
${items.join("\n")}

💰 *Total:* ₹${total}

👤 *Name:* ${name}
📞 *Phone:* ${phone}
🏠 *Address:* ${addr}`;

  window.open("https://wa.me/918888942084?text=" + encodeURIComponent(msg));
}

/* DARK MODE */
function toggleDark() {
  document.body.classList.toggle("dark");
}
</script>

</body>
</html>
