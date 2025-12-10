<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MG Manisha Glow Ayurvedic</title>

<style>
/* -------------------- GLOBAL --------------------- */
body {
    margin: 0;
    padding: 0;
    font-family: "Poppins", sans-serif;
    background: #faf7ef;
    color: #2f3b26;
}
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
    opacity: 0.09;
    z-index: -1;
}
.header { 
    background: linear-gradient(to bottom right, #c9e7c3, #f5f0da);
    padding: 30px; 
    text-align: center; 
    border-bottom: 5px solid #8fbf7a;
    background-image: url('https://images.unsplash.com/photo-1590393804594-2b51d7c5ee54?auto=format&fit=crop&w=1400&q=60');
    background-size: cover; 
    background-position: center;
    color: white; 
    border-radius: 12px; 
    margin-bottom: 12px; 
}
.header h1 { font-size: 35px; font-weight: 700; text-shadow: 2px 2px 10px #000; margin:0 }
.header h2 { font-size: 20px; margin-top: 5px; text-shadow: 2px 2px 8px #000; margin:0; }

/* GRID & CARDS */
.container{max-width:1100px;margin:0 auto;padding:18px}
.section-title{ text-align:center; font-size:24px; color:#3e5d2c; margin:8px 0 18px; }
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:18px}
.card{
    background:rgba(255,255,255,0.95);
    padding:16px;
    border-radius:14px;
    box-shadow:0 12px 30px rgba(0,0,0,0.06);
    transition:transform .25s
}
.card:hover{transform:translateY(-6px)}
.thumb{
    height:140px;border-radius:10px;background-size:cover;background-position:center;margin-bottom:10px
}
.card h3{margin:0 0 6px 0;font-size:18px}
.small{font-size:13px;color:#6b7b5f}
.qty input{width:100%;padding:8px;border-radius:8px;border:1px solid #d6e1d0}

.order-box{
    margin:28px auto;
    padding:18px;
    border-radius:14px;
    background:rgba(255,255,255,0.97);
    max-width:720px;
    box-shadow:0 12px 30px rgba(0,0,0,0.06)
}
.order-row{display:flex;gap:10px}
.order-row > *{flex:1}
.total{font-weight:700;font-size:18px;color:#3e7b44}
.btn{
    background:#6f9e58;
    color:#fff;
    padding:12px;
    border-radius:10px;
    border:none;
    cursor:pointer;
    font-size:16px;
}
.company{
    background:rgba(255,255,255,0.95);
    padding:14px;border-radius:12px;margin-top:20px;text-align:center
}
.footer{
    text-align:center;padding:14px;margin-top:18px;background:#e6f0e0;border-radius:10px;color:#47613a 
}
@media(max-width:640px){.order-row{flex-direction:column}}
</style>
</head>

<body>

<div class="container">

<!-- 🔥 HEADER -->
<div class="header">
    <h1>🌿 MG Manisha Glow Ayurvedic</h1>
    <h2>Premium Home-Made Ayurvedic Products</h2>
</div>

<!-- 🧼 SOAP SECTION -->
<h3 class="section-title">🧼 Soap Collection — ₹50</h3>
<div class="grid">

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1582719478244-ff65d3f7b7a3?auto=format&fit=crop&w=800&q=60')"></div>
      <h3>🍃 Neem Soap</h3>
      <p class="small">Anti-bacterial, acne control.</p>
      <div class="qty"><input type="number" min="0" data-price="50" data-name="Neem Soap"></div>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1501004318641-b39e6451bec6?auto=format&fit=crop&w=800&q=60')"></div>
      <h3>🌿 Tulasi Soap</h3>
      <p class="small">Refreshing & detoxifying.</p>
      <div class="qty"><input type="number" min="0" data-price="50" data-name="Tulasi Soap"></div>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1560264280-2ace7a2b4f0f?auto=format&fit=crop&w=800&q=60')"></div>
      <h3>🍀 Aloe Vera Soap</h3>
      <p class="small">Hydrating & soothing.</p>
      <div class="qty"><input type="number" min="0" data-price="50" data-name="Aloe Vera Soap"></div>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1579710757331-0a7f9d3d1e40?auto=format&fit=crop&w=800&q=60')"></div>
      <h3>🥛 Goat Milk Soap</h3>
      <p class="small">Nourishing & gentle.</p>
      <div class="qty"><input type="number" min="0" data-price="50" data-name="Goat Milk Soap"></div>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1529921879218-1f6b61c95ef8?auto=format&fit=crop&w=800&q=60')"></div>
      <h3>🖤 Charcoal Soap</h3>
      <p class="small">Deep-clean & oil control.</p>
      <div class="qty"><input type="number" min="0" data-price="50" data-name="Charcoal Soap"></div>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1581091012184-7a7a1d0f6a6a?auto=format&fit=crop&w=800&q=60')"></div>
      <h3>✨ Turmeric Soap</h3>
      <p class="small">Brightening & glowing.</p>
      <div class="qty"><input type="number" min="0" data-price="50" data-name="Turmeric Soap"></div>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1556228453-3c9cc9f3d0b9?auto=format&fit=crop&w=800&q=60')"></div>
      <h3>🍚 Rice Potato Soap</h3>
      <p class="small">Softening & tan removal.</p>
      <div class="qty"><input type="number" min="0" data-price="50" data-name="Rice Potato Soap"></div>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1603575448399-e8a37d6b7d77?auto=format&fit=crop&w=800&q=60')"></div>
      <h3>Bheem Sen Kapur Soap</h3>
      <p class="small">Traditional alum soap.</p>
      <div class="qty"><input type="number" min="0" data-price="50" data-name="Bheem Sen Kapur Soap"></div>
    </div>

</div>

<!-- 🌸 FACE PACK SECTION -->
<h3 class="section-title">🌸 Face Pack Collection — ₹30</h3>
<div class="grid">

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1598531371365-6b7f1f6d4c9b?auto=format&fit=crop&w=800&q=60')"></div>
      <h3>🍃 Neem Leaf Powder</h3>
      <p class="small">Purifying face pack.</p>
      <div class="qty"><input type="number" min="0" data-price="30" data-name="Neem Leaf Powder"></div>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1542444459-db8a1b2d7b2a?auto=format&fit=crop&w=800&q=60')"></div>
      <h3>💧 Moisturizer Pack</h3>
      <p class="small">Hydrating & softening.</p>
      <div class="qty"><input type="number" min="0" data-price="30" data-name="Moisturizer Pack"></div>
    </div>

</div>

<!-- 📝 ORDER SUMMARY -->
<div class="order-box">
    <h3>📝 Order Summary</h3>

    <div class="order-row">
        <input id="custName" placeholder="👤 Your name">
        <input id="custPhone" placeholder="📞 Phone number">
    </div>

    <textarea id="custAddr" placeholder="🏠 Full delivery address"></textarea>

    <div style="display:flex;justify-content:space-between;margin-top:12px">
        <div class="small">Total Amount:</div>
        <div class="total" id="grandTotal">₹0</div>
    </div>

    <button class="btn" id="orderBtn" style="margin-top:12px">📩 WhatsApp Order</button>
</div>

<!-- 📞 COMPANY DETAILS -->
<div class="company">
    <p><b>Contact:</b> MG Manisha Glow Ayurvedic</p>
    <p><b>Phone / WhatsApp:</b> 8888942084</p>
    <p><b>Email:</b> mgayurvedicc@gmail.com</p>
</div>

<div class="footer">© <span id="yr"></span> MG Manisha Glow Ayurvedic — Natural Premium Care</div>

</div>

<script>
document.getElementById('yr').textContent = new Date().getFullYear();

/* AUTO TOTAL */
function calcTotal(){
  const nums = document.querySelectorAll('input[type="number"]');
  let total = 0;

  nums.forEach(n=>{
      const qty = parseInt(n.value) || 0;
      const price = parseInt(n.dataset.price) || 0;
      total += qty * price;
  });

  document.getElementById('grandTotal').textContent = '₹' + total;
  return total;
}
document.querySelectorAll('input[type="number"]').forEach(i => i.addEventListener('input', calcTotal));

/* SEND ORDER TO WHATSAPP */
document.getElementById('orderBtn').addEventListener('click', ()=>{
    const name = custName.value.trim();
    const phone = custPhone.value.trim();
    const addr = custAddr.value.trim();
    const total = calcTotal();

    if(!name || !phone || !addr){
        alert("कृपया Name, Phone और Address भरें!");
        return;
    }

    const items=[];
    document.querySelectorAll('input[type="number"]').forEach(n=>{
        const qty = parseInt(n.value) || 0;
        if(qty>0){
            items.push(n.dataset.name + ": " + qty + " x ₹" + (n.dataset.price || 0));
        }
    });

    const msg =
`🧾 *New Order*

📦 *Items:*
${items.join("\n")}

💰 *Total:* ₹${total}

👤 *Name:* ${name}
📞 *Phone:* ${phone}
🏠 *Address:* ${addr}
`;

    window.open("https://wa.me/918888942084?text=" + encodeURIComponent(msg));
});
</script>

</body>
</html>
