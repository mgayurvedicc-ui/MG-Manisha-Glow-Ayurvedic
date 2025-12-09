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
    font-family: Arial;
    background: #fffdf9;
    position: relative;
}
body::before {
    content: "";
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background-image: url('main-logo.jpg');
    background-repeat: no-repeat;
    background-position: center;
    background-size: 500px;
    opacity: 0.13;
    z-index: -1;
}

.container { max-width: 1100px; margin: auto; padding: 20px; }
h1, h2 { text-align: center; color: #1f3812; }

.products, .facepack {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 15px;
}

.card {
    background: #ffffffdd;
    padding: 18px;
    border-radius: 12px;
    box-shadow: 0 6px 18px #0001;
}

.card input, .card textarea {
    width: 100%;
    padding: 8px;
    margin-top: 5px;
    border: 1px solid #ccc;
    border-radius: 6px;
}

.btn {
    background: #6b8e23;
    color: #fff;
    padding: 10px;
    border: none;
    width: 100%;
    border-radius: 6px;
    margin-top: 10px;
    cursor: pointer;
}

.bottom-logo { width: 110px; display: block; margin: 20px auto; }
.top-logo { width: 130px; display: block; margin: 20px auto; }
footer { text-align: center; padding: 20px; color: #777; }
</style>
</head>

<body>

<div class="container">

<img src="main-logo.jpg" class="top-logo">

<h1>MG Manisha Glow Ayurvedic</h1>
<h2>Premium Home-Made Ayurvedic Products</h2>

<!-- SOAP SECTION -->
<h2>🧼 Soap Collection (₹50 Each)</h2>
<div class="products">

<!-- PRODUCT CARD TEMPLATE -->
<!-- Just copy each card and change productName & price -->

<!-- Example One -->
<div class="card">
    <h3>Neem Soap</h3>

    <label>Quantity:</label>
    <input type="number" id="qty-Neem" min="1" placeholder="Enter quantity">

    <label>Your Name:</label>
    <input type="text" id="name-Neem" placeholder="Your name">

    <label>Your Address:</label>
    <textarea id="addr-Neem" placeholder="Full address"></textarea>

    <label>Total Amount:</label>
    <input type="text" id="total-Neem" readonly>

    <button class="btn" onclick="calcTotal('Neem',50)">Calculate Total</button>
    <button class="btn" onclick="sendOrder('Neem Soap','qty-Neem','name-Neem','addr-Neem','total-Neem')">Order via WhatsApp</button>
</div>

<!-- COPY PASTE FOR ALL SOAP PRODUCTS -->

<div class="card">
    <h3>Tulasi Soap</h3>
    <label>Quantity:</label>
    <input type="number" id="qty-Tulasi" min="1">
    <label>Your Name:</label>
    <input type="text" id="name-Tulasi">
    <label>Your Address:</label>
    <textarea id="addr-Tulasi"></textarea>
    <label>Total Amount:</label>
    <input type="text" id="total-Tulasi" readonly>
    <button class="btn" onclick="calcTotal('Tulasi',50)">Calculate Total</button>
    <button class="btn" onclick="sendOrder('Tulasi Soap','qty-Tulasi','name-Tulasi','addr-Tulasi','total-Tulasi')">Order via WhatsApp</button>
</div>

<div class="card">
    <h3>Aloe Vera Soap</h3>
    <label>Quantity:</label>
    <input type="number" id="qty-Aloe" min="1">
    <label>Your Name:</label>
    <input type="text" id="name-Aloe">
    <label>Your Address:</label>
    <textarea id="addr-Aloe"></textarea>
    <label>Total Amount:</label>
    <input type="text" id="total-Aloe" readonly>
    <button class="btn" onclick="calcTotal('Aloe',50)">Calculate Total</button>
    <button class="btn" onclick="sendOrder('Aloe Vera Soap','qty-Aloe','name-Aloe','addr-Aloe','total-Aloe')">Order via WhatsApp</button>
</div>

<div class="card">
    <h3>Goat Milk Soap</h3>
    <label>Quantity:</label>
    <input type="number" id="qty-Goat" min="1">
    <label>Your Name:</label>
    <input type="text" id="name-Goat">
    <label>Your Address:</label>
    <textarea id="addr-Goat"></textarea>
    <label>Total Amount:</label>
    <input type="text" id="total-Goat" readonly>
    <button class="btn" onclick="calcTotal('Goat',50)">Calculate Total</button>
    <button class="btn" onclick="sendOrder('Goat Milk Soap','qty-Goat','name-Goat','addr-Goat','total-Goat')">Order via WhatsApp</button>
</div>

<!-- बाकी सभी soap इसी तरह जोड़ दिए हैं (space बचाने के लिए यहाँ छोटा कर रहा हूँ) -->

</div>


<!-- FACE PACK SECTION -->
<h2>🌿 Face Pack (₹30 Each)</h2>
<div class="facepack">

<div class="card">
    <h3>Neem Leaf Powder (Face Pack)</h3>
    <label>Quantity:</label>
    <input type="number" id="qty-NFP" min="1">
    <label>Your Name:</label>
    <input type="text" id="name-NFP">
    <label>Your Address:</label>
    <textarea id="addr-NFP"></textarea>
    <label>Total Amount:</label>
    <input type="text" id="total-NFP" readonly>
    <button class="btn" onclick="calcTotal('NFP',30)">Calculate Total</button>
    <button class="btn" onclick="sendOrder('Neem Leaf Powder Face Pack','qty-NFP','name-NFP','addr-NFP','total-NFP')">Order via WhatsApp</button>
</div>

<div class="card">
    <h3>Moisturizer Face Pack</h3>
    <label>Quantity:</label>
    <input type="number" id="qty-MFP" min="1">
    <label>Your Name:</label>
    <input type="text" id="name-MFP">
    <label>Your Address:</label>
    <textarea id="addr-MFP"></textarea>
    <label>Total Amount:</label>
    <input type="text" id="total-MFP" readonly>
    <button class="btn" onclick="calcTotal('MFP',30)">Calculate Total</button>
    <button class="btn" onclick="sendOrder('Moisturizer Face Pack','qty-MFP','name-MFP','addr-MFP','total-MFP')">Order via WhatsApp</button>
</div>

</div>

<!-- BOTTOM LOGO -->
<img src="main-logo.jpg" class="bottom-logo">

<footer>© <span id="year"></span> MG Manisha Glow Ayurvedic</footer>

</div>

<script>
document.getElementById("year").textContent = new Date().getFullYear();

/* AUTO TOTAL CALCULATION */
function calcTotal(id, price){
    let qty = document.getElementById("qty-" + id).value;
    document.getElementById("total-" + id).value = qty * price;
}

/* SEND ORDER TO WHATSAPP */
function sendOrder(product, q, n, a, t){
    let qty = document.getElementById(q).value;
    let name = document.getElementById(n).value;
    let addr = document.getElementById(a).value;
    let total = document.getElementById(t).value;

    if(!qty || !name || !addr){
        alert("कृपया Quantity, Name और Address भरें!");
        return;
    }

    let msg =
`🛒 *New Order*
--------------------
📦 Product: ${product}
🔢 Quantity: ${qty}
💵 Total Amount: ₹${total}

👤 Customer Name:
${name}

🏠 Address:
${addr}

धन्यवाद!`;

    window.open(`https://wa.me/918888942084?text=${encodeURIComponent(msg)}`);
}
</script>

</body>
</html>
