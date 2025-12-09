<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MG Manisha Glow Ayurvedic</title>

<style>
    body {
        margin: 0;
        padding: 0;
        font-family: Arial, sans-serif;
        background: #fffdf9;
        position: relative;
        overflow-x: hidden;
    }

    /* 🔥 Background Logo Watermark using your attached logo */
    body::before {
        content: "";
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: url('main logo.jpg'); /* your logo */
        background-repeat: no-repeat;
        background-position: center;
        background-size: 520px;
        opacity: 0.13; 
        z-index: -1;
    }

    .container {
        max-width: 1100px;
        margin: auto;
        padding: 20px;
    }

    h1, h2 {
        text-align: center;
        color: #1f3812;
    }

    .products, .facepack {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 15px;
        margin-top: 20px;
    }

    .card {
        background: rgba(255,255,255,0.90);
        border-radius: 12px;
        padding: 18px;
        box-shadow: 0 6px 18px rgba(0,0,0,0.10);
        backdrop-filter: blur(3px);
    }

    .btn {
        background: #6b8e23;
        color: white;
        padding: 10px 14px;
        border-radius: 6px;
        border: none;
        cursor: pointer;
        margin-top: 10px;
        width: 100%;
    }

    footer {
        text-align: center;
        color: #666;
        margin-top: 40px;
        padding-bottom: 20px;
    }
</style>

</head>
<body>

<div class="container">

<h1>MG Manisha Glow Ayurvedic</h1>
<h2>Premium Home-Made Ayurvedic Products</h2>

<!-- SOAP LIST -->
<h2>🧼 Soap Collection (₹50 Each)</h2>

<div class="products">

    <div class="card">
        <h3>Neem Soap</h3>
        <p>Anti-bacterial • Clear Skin</p>
        <button class="btn" onclick="orderSoap('Neem Soap')">Order ₹50</button>
    </div>

    <div class="card">
        <h3>Tulasi Soap</h3>
        <p>Detox • Fresh Skin</p>
        <button class="btn" onclick="orderSoap('Tulasi Soap')">Order ₹50</button>
    </div>

    <div class="card">
        <h3>Aloe Vera Soap</h3>
        <p>Moisturizing • Soft Skin</p>
        <button class="btn" onclick="orderSoap('Aloe Vera Soap')">Order ₹50</button>
    </div>

    <div class="card">
        <h3>Goat Milk Soap</h3>
        <p>Nourishing • Gentle</p>
        <button class="btn" onclick="orderSoap('Goat Milk Soap')">Order ₹50</button>
    </div>

    <div class="card">
        <h3>Charcoal Soap</h3>
        <p>Deep Clean • Oil Control</p>
        <button class="btn" onclick="orderSoap('Charcoal Soap')">Order ₹50</button>
    </div>

    <div class="card">
        <h3>Turmeric Soap</h3>
        <p>Glow • Brightening</p>
        <button class="btn" onclick="orderSoap('Turmeric Soap')">Order ₹50</button>
    </div>

    <div class="card">
        <h3>Rice Potato Soap</h3>
        <p>Tan Remove • Soft Skin</p>
        <button class="btn" onclick="orderSoap('Rice Potato Soap')">Order ₹50</button>
    </div>

    <div class="card">
        <h3>Bheem Sen Kapur Alum (तुरटी) Soap</h3>
        <p>Skin Tightening • Smooth Texture</p>
        <button class="btn" onclick="orderSoap('Bheem Sen Kapur Alum Soap')">Order ₹50</button>
    </div>

</div>

<!-- FACE PACK SECTION -->
<h2>🌿 Face Pack Collection (₹30 Each)</h2>

<div class="facepack">

    <div class="card">
        <h3>Neem Leaf Powder (Face Pack)</h3>
        <p>Detox • Pimple Control</p>
        <button class="btn" onclick="orderFace('Neem Leaf Powder Face Pack')">Order ₹30</button>
    </div>

    <div class="card">
        <h3>Moisturizer Face Pack</h3>
        <p>Soft • Hydrating • Glow</p>
        <button class="btn" onclick="orderFace('Moisturizer Face Pack')">Order ₹30</button>
    </div>

</div>

<footer>
    © <span id="year"></span> MG Manisha Glow Ayurvedic
</footer>

</div>

<script>
document.getElementById("year").textContent = new Date().getFullYear();

const wa = "918888942084";

/* SOAP ORDER ₹50 */
function orderSoap(product){
    const msg = `Hello, mujhe ${product} (₹50) order karna hai.`;
    window.open(`https://wa.me/${wa}?text=${encodeURIComponent(msg)}`, "_blank");
}

/* FACE PACK ORDER ₹30 */
function orderFace(product){
    const msg = `Hello, mujhe ${product} (₹30) order karna hai.`;
    window.open(`https://wa.me/${wa}?text=${encodeURIComponent(msg)`, "_blank");
}
</script>

</body>
</html>
