<!-- Save as index.html -->
<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>MG Manisha Glow Ayurvedic — Premium</title>

<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
/* ------------ RESET & ROOT ------------ */
:root{
  --accent:#4b7f39;
  --accent2:#2f5e28;
  --gold:#b58e43;
  --bg:#f6fbf6;
  --card:rgba(255,255,255,0.95);
  --muted:#6c7a63;
  --glass: rgba(255,255,255,0.8);
}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:"Poppins",sans-serif;background:var(--bg);color:#123217;line-height:1.45;}

/* ---- PRELOADER ---- */
#preloader {
  position:fixed;left:0;top:0;width:100%;height:100%;background:linear-gradient(180deg, rgba(245,250,245,1), rgba(230,245,230,1));
  display:flex;align-items:center;justify-content:center;z-index:9999;transition:opacity .45s ease;
}
.preloader-inner{display:flex;flex-direction:column;align-items:center;gap:18px}
.logo-circle{width:110px;height:110px;border-radius:18px;background:#fff;display:flex;align-items:center;justify-content:center;box-shadow:0 10px 30px rgba(20,30,10,0.08)}
.logo-circle img{max-width:82%;max-height:82%}
.loader-dots{display:flex;gap:8px}
.loader-dots span{width:12px;height:12px;border-radius:50%;background:var(--accent);opacity:.25;animation:dots .9s infinite}
.loader-dots span:nth-child(2){animation-delay:.12s}
.loader-dots span:nth-child(3){animation-delay:.24s}
@keyframes dots{0%{opacity:.25;transform:translateY(0)}50%{opacity:1;transform:translateY(-8px)}100%{opacity:.25;transform:translateY(0)}}

/* ---- MAIN LAYOUT ---- */
.container{max-width:1150px;margin:36px auto;padding:0 18px}
.header{display:flex;align-items:center;gap:18px;margin-bottom:12px}
.brand-logo{width:96px;height:96px;border-radius:12px;overflow:hidden;box-shadow:0 8px 28px rgba(20,30,10,0.06)}
.brand-logo img{width:100%;height:100%;object-fit:contain}
.brand-title h1{font-family:"Cormorant Garamond",serif;font-size:30px;color:var(--accent2);margin-bottom:4px}
.brand-title p{color:var(--muted);font-size:14px}

/* hero */
.hero{display:flex;gap:22px;align-items:center;background:linear-gradient(180deg, rgba(255,255,255,0.75), rgba(250,255,250,0.9));border-radius:16px;padding:22px;box-shadow:0 12px 30px rgba(20,30,10,0.06)}
.hero-left{flex:1}
.hero-right{width:360px;border-radius:12px;overflow:hidden}
.hero h2{font-family:"Playfair Display",serif;font-size:36px;color:var(--accent2);margin-bottom:8px}
.hero p{color:var(--muted);font-size:16px;margin-bottom:12px}

/* product grid — professional card style */
.products{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:18px;margin-top:20px}
.card{background:var(--card);border-radius:14px;padding:12px;box-shadow:0 10px 30px rgba(10,20,10,0.06);border:1px solid rgba(120,150,120,0.08);display:flex;flex-direction:column;gap:10px}
.thumb{height:170px;border-radius:12px;background-size:cover;background-position:center;position:relative;overflow:hidden}
.thumb::after{content:"";position:absolute;inset:0;background:linear-gradient(180deg,transparent,rgba(0,0,0,0.10))}
.prod-title{display:flex;align-items:center;justify-content:space-between;gap:8px}
.prod-title h3{font-size:18px;margin:0;color:var(--accent2);font-weight:600}
.badge{background:linear-gradient(90deg,var(--gold),#d6b06d);color:#fff;padding:6px 9px;border-radius:10px;font-weight:700;font-size:13px;box-shadow:0 6px 16px rgba(0,0,0,0.08)}

/* pro image overlay + view */
.thumb .view{position:absolute;right:12px;bottom:12px;background:rgba(255,255,255,0.92);padding:6px 8px;border-radius:8px;font-size:13px;color:var(--accent2);box-shadow:0 6px 18px rgba(20,30,10,0.06)}

.card p{color:var(--muted);font-size:13px}
.qty{display:flex;gap:8px;align-items:center;margin-top:auto}
.qty input{width:110px;padding:10px;border-radius:8px;border:1px solid #d6e1d0}

/* order box (smaller, centered) */
.order-box{max-width:600px;margin:28px auto;padding:16px;border-radius:12px;background:var(--glass);box-shadow:0 12px 30px rgba(20,30,10,0.06);border:1px solid rgba(120,150,120,0.08)}
.order-row{display:flex;gap:10px;margin-top:8px}
.order-row input{flex:1;padding:10px;border-radius:8px;border:1px solid #d6e6d6}
.total-line{display:flex;justify-content:space-between;align-items:center;margin-top:12px;font-weight:700;color:var(--accent2)}
.order-btn{margin-top:10px;padding:12px;border-radius:10px;background:var(--accent);color:#fff;border:none;cursor:pointer}

/* contact (smaller) */
.contact-small{max-width:720px;margin:18px auto;padding:14px;border-radius:12px;background:var(--card);box-shadow:0 8px 20px rgba(10,20,10,0.06);border-left:4px solid var(--gold);font-size:15px;color:var(--muted)}

/* footer */
.footer{margin-top:22px;text-align:center;color:var(--muted);font-size:14px;padding-bottom:30px}

/* responsive tweaks */
@media(max-width:880px){.hero{flex-direction:column}.hero-right{width:100%}}
</style>
</head>
<body>

<!-- PRELOADER -->
<div id="preloader">
  <div class="preloader-inner">
    <div class="logo-circle">
      <img src="main-logo.jpg" alt="logo" onerror="this.style.display='none'">
    </div>
    <div class="loader-dots"><span></span><span></span><span></span></div>
  </div>
</div>

<!-- MAIN -->
<div class="container" id="page" style="opacity:0;transform:translateY(8px)">

  <header class="header">
    <div class="brand-logo"><img src="main-logo.jpg" alt="logo" style="width:100%;height:100%;object-fit:contain" onerror="this.style.display='none'"></div>
    <div class="brand-title">
      <h1>MG Manisha Glow Ayurvedic</h1>
      <p>Handmade Ayurvedic Soaps · Face Packs · Natural Care</p>
    </div>
  </header>

  <section class="hero">
    <div class="hero-left">
      <h2>Natural, Pure & Premium Ayurvedic Skincare</h2>
      <p>Handcrafted soaps and creams made from Neem, Tulasi, Aloe Vera and traditional herbs. Gentle on skin — powerful on results.</p>
      <div style="display:flex;gap:12px;margin-top:12px">
        <button class="order-btn" onclick="scrollToOrder()">📩 Order Now</button>
        <a href="#contact" style="align-self:center;color:var(--accent2);font-weight:600;text-decoration:none">📞 Contact</a>
      </div>
    </div>
    <div class="hero-right">
      <img src="https://images.unsplash.com/photo-1542444459-db8a1b2d7b2a?auto=format&fit=crop&w=900&q=60" alt="" style="width:100%;height:100%;object-fit:cover">
    </div>
  </section>

  <h3 style="margin-top:26px;color:var(--accent2);font-family:'Cormorant Garamond',serif">Premium Products</h3>

  <div class="products">
    <!-- Example professional product cards -->
    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1582719478244-ff65d3f7b7a3?auto=format&fit=crop&w=1000&q=60')">
        <div class="view">View</div>
      </div>
      <div class="prod-title"><h3>🍃 Neem Soap</h3><div class="badge">₹50</div></div>
      <p>Natural anti-bacterial soap for clearer skin.</p>
      <div class="qty"><input type="number" min="0" value="0" data-price="50" data-name="Neem Soap"></div>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1501004318641-b39e6451bec6?auto=format&fit=crop&w=1000&q=60')">
        <div class="view">View</div>
      </div>
      <div class="prod-title"><h3>🌿 Tulasi Soap</h3><div class="badge">₹50</div></div>
      <p>Refreshing tulasi formulation for gentle cleansing.</p>
      <div class="qty"><input type="number" min="0" value="0" data-price="50" data-name="Tulasi Soap"></div>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1560264280-2ace7a2b4f0f?auto=format&fit=crop&w=1000&q=60')">
        <div class="view">View</div>
      </div>
      <div class="prod-title"><h3>🍀 Aloe Vera Soap</h3><div class="badge">₹50</div></div>
      <p>Hydrating soap with soothing aloe benefits.</p>
      <div class="qty"><input type="number" min="0" value="0" data-price="50" data-name="Aloe Vera Soap"></div>
    </div>

    <div class="card">
      <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1529921879218-1f6b61c95ef8?auto=format&fit=crop&w=1000&q=60')">
        <div class="view">View</div>
      </div>
      <div class="prod-title"><h3>💧 Moisturizer Cream</h3><div class="badge">₹30</div></div>
      <p>Lightweight herbal moisturizer for daily glow.</p>
      <div class="qty"><input type="number" min="0" value="0" data-price="30" data-name="Moisturizer Cream"></div>
    </div>

    <!-- add other cards similarly -->
  </div>

  <!-- order box -->
  <div class="order-box" id="orderBox">
    <h3 style="margin:0 0 8px 0">📝 Order Summary</h3>
    <div style="font-size:13px;color:var(--muted)">Enter quantity for each product, total calculates automatically.</div>

    <div class="order-row">
      <input id="custName" placeholder="Your name">
      <input id="custPhone" placeholder="Phone number">
    </div>
    <textarea id="custAddr" placeholder="Full delivery address"></textarea>

    <div class="total-line"><div>Total:</div><div id="grandTotal">₹0</div></div>
    <button class="order-btn" onclick="placeOrder()">Send WhatsApp Order</button>
  </div>

  <!-- contact smaller -->
  <div class="contact-small" id="contact">
    <strong>MG Manisha Glow Ayurvedic</strong><br>
    ✔ Mobile: 8888942084 — ✔ WhatsApp: 8888942084<br>
    ✔ Address: At Post Rawande, Tal Kopargaon, Dist Ahilyanagar 423601<br>
    ✔ Email: mgayurvedicc@gmail.com — Instagram: @mg_manisha_glow_Ayurvedic_<br>
    Website: https://mgayurvedicc-ui.github.io/MG-Manisha-Glow-Ayurvedic/
  </div>

  <div class="footer">© <span id="year1"></span> MG Manisha Glow Ayurvedic</div>
</div>

<script>
/* PRELOADER: hide after load */
window.addEventListener('load', ()=> {
  const pre = document.getElementById('preloader');
  pre.style.opacity = '0'; pre.style.pointerEvents = 'none';
  setTimeout(()=>pre.remove(),600);
  // reveal page
  const pg = document.getElementById('page');
  pg.style.opacity = 1; pg.style.transform = 'none';
});

/* AUTO TOTAL CALC */
function calcTotal(){
  let total = 0;
  document.querySelectorAll('.products input[type="number"]').forEach(i=>{
    const q = parseInt(i.value) || 0;
    const p = parseInt(i.dataset.price) || 0;
    total += q * p;
  });
  document.getElementById('grandTotal').innerText = '₹' + total;
  return total;
}
document.querySelectorAll('.products input[type="number"]').forEach(i=>i.addEventListener('input',calcTotal));

/* PLACE ORDER -> whatsapp */
function placeOrder(){
  const name = document.getElementById('custName').value.trim();
  const phone = document.getElementById('custPhone').value.trim();
  const addr = document.getElementById('custAddr').value.trim();
  const total = calcTotal();
  if(!name||!phone||!addr){ alert('कृपया Name, Phone और Address भरें!'); return; }
  const items = [];
  document.querySelectorAll('.products input[type="number"]').forEach(i=>{
    if((parseInt(i.value)||0) > 0) items.push(i.dataset.name + ' — ' + i.value + '×' + ' ₹' + i.dataset.price);
  });
  const msg = `🧾 New Order\n\n${items.join('\n')}\n\n💰 Total: ₹${total}\n\n👤 ${name}\n📞 ${phone}\n🏠 ${addr}`;
  window.open('https://wa.me/918888942084?text=' + encodeURIComponent(msg));
}

/* helper for order button from hero */
function scrollToOrder(){ document.getElementById('orderBox').scrollIntoView({behavior:'smooth'}); }

/* year */
document.getElementById('year1').textContent = new Date().getFullYear();
</script>
</body>
</html>
