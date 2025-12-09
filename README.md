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
        opacity: 0.13;
        z-index: -1;
    }

    .top-logo, .bottom-logo {
        display: block;
        margin: 20px auto;
    }

    .top-logo { width: 130px; }
    .bottom-logo { width: 110px; }

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
    }

    .card input {
        width: 100%;
        padding: 8px;
        margin-top: 8px;
        border-radius: 6px;
        border: 1px solid #aaa;
    }

    .order-box {
        background: rgba(255,255,255,0.95);
        padding: 15px;
        border-radius: 12px;
        margin-top: 25px;
        width: 100%;
        max-width: 600px;
        margin-left: auto;
        margin-right: auto;
        box-shadow: 0 6px 18px rgba(0,0,0,0.10);
    }

    .order-box input, .order-box textarea {
        width: 100%;
        padding: 8px;
        margin-top: 8px;
        border-radius: 6px;
        border: 1px solid #aaa;
        font-size: 14px;
    }

    .order-box textarea {
        height: 60px;
    }

    .btn {
        background: #6b8e23;
        color: white;
        padding: 10px;
        border: none;
        width: 100%;
        margin-top: 12px;
        border-radius: 6px;
        cursor: pointer;
        font-size: 15px;
    }

    .company-details {
        text-align: center;
        margin-top: 35px;
        background: rgba(255,255,255,0.90);
        padding: 18px;
        border-radius: 12px;
        box-shadow: 0 6px 18px rgba(0,0,0,0.08);
    }

    .company-details p {
        margin: 6px 0;
        font-size: 15px;
    }

    footer {
        text-align: center;
        margin-top: 40px;
        padding-bottom: 20px;
        color: #666;
    }
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
    <div class="card"><h3>Neem Soap</h3><input type="number" id="Neem" min="0" oninput="calcTotal()"></div>
    <div class="card"><h3>Tulasi Soap</h3><input type="number" id="Tulasi" min="0" oninput="calcTotal()"></div>
    <div class="card"><h3>Aloe Vera Soap</h3><input type="number" id="Aloe" min="0" oninput="calcTotal()"></div>
    <div class="card"><h3>Goat Milk Soap</h3><input type="number" id="Goat" min="0" oninput="calcTotal()"></div>
    <div class="card"><h3>Charcoal Soap</h3><input type="number" id="Charcoal" min="0" oninput="calcTotal()"></div>
    <div class="card"><h3>Turmeric Soap</h3><input type="number" id="Turmeric" min="0" oninput="calcTotal()"></div>
    <div class="card"><h3>Rice Potato Soap</h3><input type="number" id="Rice" min="0" oninput="calcTotal()"></div>
    <div class="card"><h3>Bheem Sen Kapur Alum Soap</h3><input type="number" id="Bheem" min="0" oninput="calcTotal()"></div>
</div>

<!-- FACE PACK SECTION -->
<h2>🌿 Face Pack Collection (₹30 Each)</h2>

<div class="facepack">
    <div class="card"><h3>Neem Leaf Powder Face Pack</h3><input type="number" id="NFP" min="0" oninput="calcTotal()"></div>
    <div class="card"><h3>Moisturizer Face Pack</h3><input type="number" id="MFP" min="0" oninput="calcTotal()"></div>
</div>

<!-- ORDER FORM -->
<div class="order-box">
<h2 style="text-align:center;">📝 Customer Details</h2>

<input type="text" id="custName" placeholder="Your Name">
<input type="text" id="custPhone" placeholder="Phone Number">
<textarea id="custAddr" placeholder="Full Address"></textarea>

<input type="text" id="totalAmount" placeholder="Total Amount" readonly>

<button class="btn" onclick="placeOrder()">WhatsApp Order भेजें</button>
</div>

<!-- COMPANY DETAILS -->
<div class="company-details">
    <p><b>Contact Name:</b> MG Manisha Glow Ayurvedic</p>
    <p><b>Mobile:</b> 8888942084</p>
    <p><b>WhatsApp:</b> 8888942084</p>
    <p><b>Address:</b> At Post Rawande, Tal Kopargaon, Dist Ahilyanagar - 423601</p>
    <p><b>Email:</b> mgayurvedicc@gmail.com</p>
    <p><b>Instagram:</b> @mg_manisha_glow_Ayurvedic_</p>
    <p><b>Website:</b> https://mgayurvedicc-ui.github.io/MG-Manisha-Glow-Ayurvedic/</p>
</div>

<img src="main-logo.jpg" class="bottom-logo">

<footer>
© <span id="year"></span> MG Manisha Glow Ayurvedic
</footer>

</div>

<script>
document.getElementById("year").textContent = new Date().getFullYear();

/* AUTO TOTAL CALCULATION */
function calcTotal() {
    let total =
        (Neem.value * 50) + (Tulasi.value * 50) + (Aloe.value * 50) +
        (Goat.value * 50) + (Charcoal.value * 50) + (Turmeric.value * 50) +
        (Rice.value * 50) + (Bheem.value * 50) +
        (NFP.value * 30) + (MFP.value * 30);

    document.getElementById("totalAmount").value = total;
}

/* SEND WHATSAPP ORDER */
function placeOrder() {

    let name = custName.value;
    let phone = custPhone.value;
    let addr = custAddr.value;
    let total = totalAmount.value;

    if (!name || !phone || !addr) {
        alert("कृपया Name, Phone और Address भरें!");
        return;
    }

    let msg =
`🛒 *New Order*
--------------------
*Quantities:*
Neem: ${Neem.value}
Tulasi: ${Tulasi.value}
Aloe: ${Aloe.value}
Goat Milk: ${Goat.value}
Charcoal: ${Charcoal.value}
Turmeric: ${Turmeric.value}
Rice Potato: ${Rice.value}
Bheem Sen: ${Bheem.value}

Neem Face Pack: ${NFP.value}
Moisturizer Pack: ${MFP.value}

--------------------
💵 *Total:* ₹${total}

👤 *Name:* ${name}
📞 *Phone:* ${phone}
🏠 *Address:* ${addr}

--------------------
    window.open(`https://wa.me/918888942084?text=${encodeURIComponent(msg)}`);
}
</script>

</body>
</html>
<script>
document.getElementById("year").textContent = new Date().getFullYear();

/* AUTO TOTAL CALCULATION */
function calcTotal() {
    let total =
        (Neem.value * 50) + (Tulasi.value * 50) + (Aloe.value * 50) +
        (Goat.value * 50) + (Charcoal.value * 50) + (Turmeric.value * 50) +
        (Rice.value * 50) + (Bheem.value * 50) +
        (NFP.value * 30) + (MFP.value * 30);

    document.getElementById("totalAmount").value = total;
}

/* SEND WHATSAPP ORDER + AUTO THANK YOU MESSAGE */
function placeOrder() {

    let name = custName.value;
    let phone = custPhone.value;
    let addr = custAddr.value;
    let total = totalAmount.value;

    if (!name || !phone || !addr) {
        alert("कृपया Name, Phone आणि Address भरा!");
        return;
    }

    let orderMsg =
``🛒🛒 *New Order*
--------------------
*Quantities:*
Neem: ${Neem.value}
Tulasi: ${Tulasi.value}
Aloe: ${Aloe.value}
Goat Milk: ${Goat.value}
Charcoal: ${Charcoal.value}
Turmeric: ${Turmeric.value}
Rice Potato: ${Rice.value}
Bheem Sen: ${Bheem.value}

Neem Face Pack: ${NFP.value}
Moisturizer Pack: ${MFP.value}

--------------------
💵 *Total:* ₹${total}

👤 *Name:* ${name}
📞 *Phone:* ${phone}
🏠 *Address:* ${addr}`;

    let thankMsg =
`धन्यवाद आम्हाला Order दिल्या बद्दल 🙏  
नक्कीच तुम्हाला आमचा Product आवडेल व तुम्हाला फायदा होईल 🙏  
लवकरात लवकर तुमची Order तुमच्या पर्यंत पोहचवू  
धन्यवाद 🙏🙏`;

    // First message = Order
    window.open(`https://wa.me/918888942084?text=${encodeURIComponent(orderMsg)}`);

    // Second message = Thank You
    setTimeout(() => {
        window.open(`https://wa.me/${custPhone.value}?text=${encodeURIComponent(thankMsg)}`);
    }, 1500);
}
</script>
