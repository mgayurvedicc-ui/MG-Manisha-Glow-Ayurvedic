<!doctype html>
<html lang="hi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>MG Manisha Glow Ayurvedic — Premium Handmade Soaps</title>
  <meta name="description" content="MG Manisha Glow — Premium Home Made Ayurvedic Soap. Cold-process, Natural Ingredients." />
  <style>
    :root{
      --bg:#fffdf9; --accent:#6b8e23; --muted:#666; --card:#fff;
      --radius:12px; --maxw:1100px;
    }
    *{box-sizing:border-box}
    body{margin:0;font-family:Inter, system-ui, Arial; background:var(--bg); color:#222}
    .wrap{max-width:var(--maxw);margin:0 auto;padding:28px}
    header{display:flex;align-items:center;justify-content:space-between}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:64px;height:64px;border-radius:14px;background:linear-gradient(135deg,#9bcc5a,#5b8a2f);display:flex;align-items:center;justify-content:center;color:white;font-weight:800}
    nav a{margin-left:12px;text-decoration:none;color:var(--muted)}
    .hero{display:grid;grid-template-columns:1fr 360px;gap:24px;margin-top:22px;align-items:start}
    .card{background:var(--card);padding:18px;border-radius:var(--radius);box-shadow:0 8px 28px rgba(20,20,20,0.06)}
    .btn{padding:10px 14px;border-radius:10px;border:0;cursor:pointer}
    .btn-primary{background:var(--accent);color:white}
    .grid-2{display:grid;grid-template-columns:1fr 1fr;gap:16px}
    input,textarea,select{padding:10px;border-radius:8px;border:1px solid #e8e8e8;width:100%}
    footer{text-align:center;color:#777;margin-top:28px}
    @media(max-width:900px){.hero{grid-template-columns:1fr}.grid-2{grid-template-columns:1fr}}
  </style>
</head>
<body>
<div class="wrap">

<header>
  <div class="brand">
    <div class="logo">MG</div>
    <div>
      <div style="font-weight:800">MG Manisha Glow Ayurvedic</div>
      <div style="font-size:13px;color:#777">Premium · Handmade · Ayurvedic</div>
    </div>
  </div>
  <nav>
    <a href="#products">Products</a>
    <a href="#benefits">Benefits</a>
    <a href="#order">Order</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<!-- HERO -->
<div class="hero">
  <div class="card">
    <h1>Premium Home-made Ayurvedic Soaps</h1>
    <p style="color:#777">Handcrafted Ayurvedic soaps for glow, acne control & hydration.</p>
    <button class="btn btn-primary" onclick="location.hash='#order'">Order via WhatsApp</button>
  </div>

  <div class="card">
    <strong>Key Ingredients</strong>
    <ul style="color:#777; margin-top:8px">
      <li>Neem — Antibacterial</li>
      <li>Tulsi — Detox</li>
      <li>Aloe Vera — Moisturizing</li>
      <li>Goat Milk — Nourishing</li>
      <li>Turmeric — Brightening</li>
      <li>Vitamin D — Glow</li>
    </ul>
  </div>
</div>

<!-- PRODUCTS -->
<section id="products">
  <h2>Our Products (₹50 Each)</h2>
  <div class="grid-2" style="margin-top:12px">

    <div class="card">
      <h3>Neem + Tulsi</h3>
      <p style="color:#777">Acne Control • Detox • Fresh Skin</p>
      <strong>₹50</strong>
      <br><br>
      <button class="btn btn-primary" onclick="orderNow('Neem + Tulsi')">Order</button>
    </div>

    <div class="card">
      <h3>Aloe Vera + Goat Milk</h3>
      <p style="color:#777">Moisturizing • Gentle • Hydrating</p>
      <strong>₹50</strong>
      <br><br>
      <button class="btn btn-primary" onclick="orderNow('Aloe Vera + Goat Milk')">Order</button>
    </div>

    <div class="card">
      <h3>Turmeric + Vitamin D</h3>
      <p style="color:#777">Glow • Brightening • Pigmentation</p>
      <strong>₹50</strong>
      <br><br>
      <button class="btn btn-primary" onclick="orderNow('Turmeric + Vitamin D')">Order</button>
    </div>

    <div class="card">
      <h3>Sandalwood Luxury</h3>
      <p style="color:#777">Premium • Calming • Long-lasting</p>
      <strong>₹50</strong>
      <br><br>
      <button class="btn btn-primary" onclick="orderNow('Sandalwood Luxury')">Order</button>
    </div>

  </div>
</section>

<!-- ORDER -->
<section id="order">
  <h2>Order Now</h2>
  <p style="color:#777">Fill details — WhatsApp automatically open ho jayega.</p>

  <div class="card">
    <form id="orderForm" onsubmit="handleOrder(event)">
      <input id="name" placeholder="Aapka Naam" required />
      <input id="phone" placeholder="Phone Number" required />

      <select id="productSelect">
        <option value="Neem + Tulsi">Neem + Tulsi — ₹50</option>
        <option value="Aloe Vera + Goat Milk">Aloe Vera + Goat Milk — ₹50</option>
        <option value="Turmeric + Vitamin D">Turmeric + Vitamin D — ₹50</option>
        <option value="Sandalwood Luxury">Sandalwood Luxury — ₹50</option>
      </select>

      <input id="qty" type="number" min="1" value="1" />
      <textarea id="address" placeholder="Delivery Address"></textarea>
      <button class="btn btn-primary" type="submit">Order via WhatsApp</button>
    </form>
  </div>

</section>

<!-- CONTACT -->
<section id="contact">
  <h2>Contact</h2>
  <div class="card">
    <p style="color:#777">
      MG Manisha Glow Ayurvedic <br>
      Phone: +91 8888942084 <br>
      Instagram: @mg_manisha_glow_ayurvedic_
    </p>
  </div>
</section>

<footer>
  © <span id="year"></span> MG Manisha Glow Ayurvedic
</footer>

</div>

<script>
document.getElementById("year").textContent = new Date().getFullYear();
const businessNumber = "918888942084";

function orderNow(product){
  document.getElementById("productSelect").value = product;
  document.getElementById("qty").value = 1;
  location.hash = "#order";
}

function handleOrder(e){
  e.preventDefault();
  const name = document.getElementById("name").value;
  const phone = document.getElementById("phone").value;
  const product = document.getElementById("productSelect").value;
  const qty = document.getElementById("qty").value;
  const address = document.getElementById("address").value;

  const msg = `Hello, mera naam ${name}. Main order karna chahta/chahti hoon: ${product} (Qty: ${qty}). Address: ${address}. Phone: ${phone}`;
  const wa = `https://wa.me/${businessNumber}?text=${encodeURIComponent(msg)}`;
  window.open(wa, "_blank");
}
</script>

</body>
</html>
