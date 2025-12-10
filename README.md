<!-- Save as index-minimal.html -->
<!doctype html>
<html lang="hi">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>MG Manisha Glow Ayurvedic — Minimal Luxury</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">

<style>
:root{
  --bg:#0f1a12; /* very dark green */
  --card:#11261a;
  --accent:#b99a46; /* gold */
  --muted:#cbd8c0;
}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:"Montserrat",sans-serif;background:var(--bg);color:var(--muted);min-height:100vh}
.watermark{position:fixed;inset:0;opacity:.06;background:url('main-logo.jpg') center/600px no-repeat;pointer-events:none;z-index:0}

/* container */
.wrap{max-width:1100px;margin:40px auto;padding:20px;position:relative;z-index:2}

/* top */
.top{display:flex;align-items:center;gap:18px;margin-bottom:16px}
.top .logo{width:80px;height:80px;border-radius:8px;background:#071009;display:flex;align-items:center;justify-content:center;border:1px solid rgba(255,255,255,0.03)}
.top h1{font-family:"Playfair Display",serif;color:var(--accent);font-size:28px;margin:0}
.top p{color:var(--muted);margin:2px 0 0 0;font-size:13px}

/* hero */
.hero{padding:28px;border-radius:12px;background:linear-gradient(180deg,rgba(255,255,255,0.01),rgba(255,255,255,0.00));border:1px solid rgba(255,255,255,0.03);display:flex;align-items:center;justify-content:space-between;gap:20px}
.hero-left h2{color:var(--muted);font-size:22px;font-family:"Playfair Display";margin:0}
.hero-left p{color:#a7b8a3;margin-top:6px}

/* product list minimal */
.products{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px;margin-top:22px}
.card{background:var(--card);padding:14px;border-radius:10px;border:1px solid rgba(255,255,255,0.03)}
.card .thumb{height:140px;border-radius:8px;background-size:cover;background-position:center;margin-bottom:10px}
.card h3{color:var(--muted);font-size:16px;margin:0}
.card small{color:#9eb39c}

/* order bar fixed bottom */
.order-bar{position:fixed;left:0;right:0;bottom:16px;margin:auto;max-width:1100px;padding:12px 14px;background:linear-gradient(90deg, rgba(17,34,18,0.9), rgba(20,40,22,0.95));border-radius:12px;border:1px solid rgba(185,154,70,0.12);display:flex;gap:12px;align-items:center;z-index:5}
.order-bar input{flex:1;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:var(--muted)}
.order-bar button{background:var(--accent);color:#06120a;padding:10px 14px;border-radius:8px;border:none;font-weight:700}

/* footer */
.footer{margin-top:90px;text-align:center;color:#9fb59c;padding-bottom:40px}
@media(max-width:720px){.hero{flex-direction:column}.order-bar{left:12px;right:12px}}
</style>
</head>
<body>

<div class="watermark"></div>

<div class="wrap">
  <div class="top">
    <div class="logo"><img src="main-logo.jpg" alt="" style="max-width:86%;max-height:86%" onerror="this.style.display='none'"></div>
    <div>
      <h1>MG Manisha Glow</h1>
      <p>Ayurvedic · Handmade · Premium</p>
    </div>
  </div>

  <section class="hero">
    <div class="hero-left">
      <h2>हमारे प्रीमियम हर्बल उत्पाद</h2>
      <p>कुशलता से बनाए गए साबुन और मॉइस्चराइज़र — रोज़मर्रा की त्वचा देखभाल के लिए।</p>
    </div>
    <div><img src="https://images.unsplash.com/photo-1542444459-db8a1b2d7b2a?auto=format&fit=crop&w=600&q=60" style="width:220px;border-radius:8px;display:block"></div>
  </section>

  <div class="products" style="margin-top:24px;">
    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1582719478244-ff65d3f7b7a3?auto=format&fit=crop&w=900&q=60')"></div>
      <h3>Neem Soap</h3>
      <small>₹50 • anti-bacterial</small>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1501004318641-b39e6451bec6?auto=format&fit=crop&w=900&q=60')"></div>
      <h3>Tulasi Soap</h3>
      <small>₹50 • refreshing</small>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1560264280-2ace7a2b4f0f?auto=format&fit=crop&w=900&q=60')"></div>
      <h3>Aloe Vera Soap</h3>
      <small>₹50 • soothing</small>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1542444459-db8a1b2d7b2a?auto=format&fit=crop&w=900&q=60')"></div>
      <h3>Moisturizer Cream</h3>
      <small>₹30 • daily glow</small>
    </div>
  </div>

</div>

<!-- ORDER BAR -->
<div class="order-bar">
  <input id="orderSummary" placeholder="Enter name, phone & address after adding quantities in product cards (simple version)">
  <button onclick="openWhatsAppMinimal()">Order via WhatsApp</button>
</div>

<div class="footer">
  © <span id="yr2"></span> MG Manisha Glow Ayurvedic — Contact: 8888942084
</div>

<script>
document.getElementById('yr2').innerText = new Date().getFullYear();

function openWhatsAppMinimal(){
  const q = encodeURIComponent(document.getElementById('orderSummary').value || 'Hello, I want to order');
  window.open('https://wa.me/918888942084?text=' + q);
}
</script>

</body>
</html>
