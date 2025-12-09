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
    background-size: 520px;
    opacity: 0.13;
    z-index: -1;
}

.container { max-width: 1100px; margin: auto; padding: 20px; }
h1, h2 { text-align: center; color: #1f3812; }

.products, .facepack {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
    gap: 15px;
}

.card {
    background: rgba(255,255,255,0.92);
    padding: 18px;
    border-radius: 12px;
    box-shadow: 0 6px 18px rgba(0,0,0,0.10);
}

.card input, 
.card textarea {
    width: 100%;
    padding: 8px;
    margin-top: 6px;
    border-radius: 6px;
    border: 1px solid #ccc;
}

.btn {
    background: #6b8e23;
    color: white;
    padding: 10px;
    width: 100%;
    border: none;
    border-radius: 6px;
    margin-top: 10px;
    cursor: pointer;
}

.top-logo { width: 130px; display: block; margin: 20px auto; }
.bottom-logo { width: 110px; display: block; margin: 20px auto; }

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

<!-- TEMPLATE FOR EACH PRODUCT -->
<div class="card">
    <h3>Neem Soap</h3>

    <label>Quantity:</label>
    <input type="number" id="qty-Neem" min="1">

    <label>Your Name:</label>
    <input type="text" id="name-Neem">

    <label>Your Address:</label>
    <textarea id="addr-Neem"></textarea>

    <label>Your Phone No:</label>
    <input type="text" id="phone-Neem">

    <label>Total Amount:</label>
    <input type="text" id="total-Neem" readonly>

    <button class="btn" onclick="calcTotal('Neem',50)">Total निकालें</button>
    <button class="btn" onclick="sendOrder('Neem Soap','qty-Neem','name-Neem','addr-Neem','phone-Neem','total-Neem')">Order via WhatsApp</button>
</div>


<div class="card">
    <h3>Tulasi Soap</h3>

    <label>Quantity:</label>
    <input type="number" id="qty-Tulasi" min="1">

    <label>Your Name:</label>
    <input type="text" id="name-Tulasi">

    <label>Your Address:</label>
    <textarea id="addr-Tulasi"></textarea>

    <label>Your Phone No:</label>
    <input type="text" id="phone-Tulasi">

    <label>Total Amount:</label>
    <input type="text" id="total-Tulasi" readonly>

    <button class="btn" onclick="calcTotal('Tulasi',50)">Total निकालें</button>
    <button class="btn" onclick="sendOrder('Tulasi Soap','qty-Tulasi','name-Tulasi','addr-Tulasi','phone-Tulasi','total-Tulasi')">Order via WhatsApp</button>
</div>


<div class="card">
    <h3>Aloe Vera Soap</h3>

    <label>Quantity:</label>
    <input type="number" id="qty-Aloe" min="1">

    <label>Your Name:</label>
    <input type="text" id="name-Aloe">

    <label>Your Address:</label>
    <textarea id="addr-Aloe"></textarea>

    <label>Your Phone No:</label>
    <input type="text" id="phone-Aloe">

    <label>Total Amount:</label>
    <input type="text" id="total-Aloe" readonly>

    <button class="btn" onclick="calcTotal('Aloe',50)">Total निकालें</button>
    <button class="btn" onclick="sendOrder('Aloe Vera Soap','qty-Aloe','name-Aloe','addr-Aloe','phone-Aloe','total-Aloe')">Order via WhatsApp</button>
</div>

<!-- इसी तरह बाकी सभी soap products automatically same pattern में add कर दूँगा अगर चाहें तो -->


</div>




<!-- FACE PACK SECTION -->
<h2>🌿 Face Pack (₹30 Each)</h2>

<div class="facepack">

<div class="card">
    <h3>Neem Leaf Powder Face Pack</h3>

    <label>Quantity:</label>
    <input type="number" id="qty-NFP" min="1">

    <label>Your Name:</label>
    <input type="text" id="name-NFP">

    <label>Your Address:</label>
    <textarea id="addr-NFP"></textarea>

    <label>Your Phone No:</label>
    <input type="text" id="phone-NFP">

    <label>Total Amount:</label>
    <input type="text" id="total-NFP" readonly>

    <button class="btn" onclick="calcTotal('NFP',30)">Total निकालें</button>
    <button class="btn" onclick="sendOrder('Neem Leaf Powder Face Pack','qty-NFP','name-NFP','addr-NFP','phone-NFP','total-NFP')">Order via WhatsApp</button>
</div>


<div class="card">
    <h3>Moisturizer Face Pack</h3>

    <label>Quantity:</label>
    <input type="number" id="qty-MFP" min="1">

    <label>Your Name:</label>
    <input type="text" id="name-MFP">

    <label>Your Address:</label>
    <textarea id="addr-MFP"></textarea>

    <label>Your Phone No:</label>
    <input type="text" id="phone-MFP">

    <label>Total Amount:</label>
    <input type="text" id="total-MFP" readonly>

    <button class="btn" onclick="calcTotal('MFP',30)">Total निकालें</button>
    <button class="btn" onclick="sendOrder('Moisturizer Face Pack','qty-MFP','name-MFP','addr-MFP','phone-MFP','total-MFP')">Order via WhatsApp</button>
</div>

</div>


<img src="main-logo.jpg" class="bottom-logo">

<footer>
© <span id="year"></span> MG Manisha Glow Ayurvedic
</footer>

</div>


<script>
document.getElementById("year").textContent = new Date().getFullYear();

function calcTotal(id, price){
    let qty = document.getElementById("qty-" + id).value;
    document.getElementById("total-" + id).value = qty * price;
}

function sendOrder(product, q, n, a, p, t){
    let qty = document.getElementById(q).value;
    let name = document.getElementById(n).value;
    let addr = document.getElementById(a).value;
    let phone = document.getElementById(p).value;
    let total = document.getElementById(t).value;

    if(!qty || !name || !addr || !phone){
        alert("कृपया सभी details भरें!");
        return;
    }

    let msg = 
`🛒 *New Order*
----------------------
📦 Product: ${product}
🔢 Quantity: ${qty}
💵 Total Amount: ₹${total}

👤 Customer Name: ${name}
📞 Phone: ${phone}

🏠 Address:
${addr}

धन्यवाद!`;

    window.open(`https://wa.me/918888942084?text=${encodeURIComponent(msg)}`);
}
</script>

</body>
</html>
