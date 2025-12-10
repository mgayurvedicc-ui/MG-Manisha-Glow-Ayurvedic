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

/* Soft Herbal Pattern Background */
body::before {
    content: "";
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('https://i.imgur.com/2O8l6MT.png');
    opacity: 0.09;
    z-index: -1;
}

/* -------------------- HEADER --------------------- */
.header {
    background: linear-gradient(to bottom right, #c9e7c3, #f5f0da);
    padding: 30px;
    text-align: center;
    border-bottom: 5px solid #8fbf7a;
    background-image: url('https://images.unsplash.com/photo-1590393804594-2b51d7c5ee54?auto=format&fit=crop&w=1400&q=60');
    background-size: cover;
    background-position: center;
    color: white;
}

.header h1 {
    font-size: 35px;
    font-weight: 700;
    text-shadow: 2px 2px 10px #000;
}

.header h2 {
    font-size: 20px;
    margin-top: 5px;
    text-shadow: 2px 2px 8px #000;
}

/* -------------------- PRODUCT GRID --------------------- */
.section-title {
    text-align: center;
    font-size: 28px;
    margin-top: 30px;
    color: #3e5d2c;
}

.products, .facepack {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 20px;
    padding: 20px;
}

/* Aesthetic Card */
.card {
    background: rgba(255, 255, 255, 0.95);
    padding: 18px;
    border-radius: 16px;
    box-shadow: 0 12px 30px rgba(0,0,0,0.12);
    transition: 0.3s;
    border: 1px solid #dfe8d3;
    backdrop-filter: blur(4px);
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 18px 40px rgba(0,0,0,0.18);
}

.card h3 {
    margin: 5px 0;
    font-size: 20px;
    color: #2e4821;
}

.card input {
    width: 100%;
    padding: 10px;
    border-radius: 8px;
    border: 1px solid #a5b99a;
    margin-top: 10px;
    font-size: 15px;
}

/* -------------------- ORDER FORM --------------------- */
.order-box {
    width: 90%;
    max-width: 600px;
    margin: 35px auto;
    padding: 25px;
    background: rgba(255,255,255,0.97);
    border-radius: 18px;
    border: 1px solid #d3dfc6;
    box-shadow: 0 12px 30px rgba(0,0,0,0.10);
}

.order-box input, .order-box textarea {
    width: 100%;
    padding: 12px;
    margin-top: 8px;
    border-radius: 10px;
    border: 1px solid #a3b899;
    font-size: 15px;
}

textarea {
    height: 70px;
}

/* Button */
.btn {
    width: 100%;
    padding: 12px;
    background: #6f9e58;
    color: white;
    border: none;
    border-radius: 10px;
    margin-top: 15px;
    font-size: 17px;
    cursor: pointer;
    transition: 0.3s;
}

.btn:hover {
    background: #568843;
}

/* -------------------- COMPANY DETAILS --------------------- */
.company-details {
    background: rgba(255,255,255,0.95);
    width: 90%;
    margin: 20px auto;
    padding: 20px;
    border-radius: 14px;
    text-align: center;
    border: 1px solid #d9e7cd;
    box-shadow: 0 8px 20px rgba(0,0,0,0.08);
}

.company-details p {
    margin: 5px 0;
}

/* -------------------- FOOTER --------------------- */
footer {
    text-align: center;
    padding: 15px;
    font-size: 14px;
    margin-top: 20px;
    background: #e6f0e0;
    border-top: 2px solid #9fbd94;
}
</style>
</head>

<body>

<!-- HERO HEADER -->
<div class="header">
    <h1>🌿 MG Manisha Glow Ayurvedic</h1>
    <h2>Premium Home-Made Ayurvedic Products</h2>
</div>

<!-- SOAP SECTION -->
<h2 class="section-title">🧼 Soap Collection (₹50)</h2>

<div class="products">

    <div class="card"><h3>🍃 Neem Soap</h3><input type="number" id="Neem" min="0"></div>
    <div class="card"><h3>🌿 Tulasi Soap</h3><input type="number" id="Tulasi" min="0"></div>
    <div class="card"><h3>🍀 Aloe Vera Soap</h3><input type="number" id="Aloe" min="0"></div>
    <div class="card"><h3>🥛 Goat Milk Soap</h3><input type="number" id="Goat" min="0"></div>
    <div class="card"><h3>🖤 Charcoal Soap</h3><input type="number" id="Charcoal" min="0"></div>
    <div class="card"><h3>✨ Turmeric Soap</h3><input type="number" id="Turmeric" min="0"></div>
    <div class="card"><h3>🍚 Rice Potato Soap</h3><input type="number" id="Rice" min="0"></div>
    <div class="card"><h3>Bheem Sen Kapur Soap</h3><input type="number" id="Bheem" min="0"></div>

</div>

<!-- FACE PACK SECTION -->
<h2 class="section-title">🌸 Face Pack Collection (₹30)</h2>

<div class="facepack">
    <div class="card"><h3>🍃 Neem Leaf Powder Pack</h3><input type="number" id="NFP" min="0"></div>
    <div class="card"><h3>💧 Moisturizer Pack</h3><input type="number" id="MFP" min="0"></div>
</div>

<!-- ORDER FORM -->
<div class="order-box">
<h2 style="text-align:center;">📝 Customer Details</h2>

<input type="text" id="custName" placeholder="👤 Your Name">
<input type="text" id="custPhone" placeholder="📞 Phone Number">
<textarea id="custAddr" placeholder="🏠 Full Address"></textarea>

<input type="text" id="totalAmount" placeholder="💵 Total Amount (Auto)" readonly>

<button class="btn" onclick="placeOrder()">📩 WhatsApp Order भेजें</button>
</div>

<!-- COMPANY DETAILS -->
<div class="company-details">
    <p><b>Contact Name:</b> MG Manisha Glow Ayurvedic</p>
    <p><b>Mobile:</b> 8888942084</p>
    <p><b>WhatsApp:</b> 8888942084</p>
    <p><b>Address:</b> Rawande, Kopargaon, Ahilyanagar 423601</p>
    <p><b>Email:</b> mgayurvedicc@gmail.com</p>
    <p><b>Instagram:</b> @mg_manisha_glow_Ayurvedic_</p>
    <p><b>Website:</b> https://mgayurvedicc-ui.github.io/MG-Manisha-Glow-Ayurvedic/</p>
</div>

<footer>
© <span id="year"></span> MG Manisha Glow Ayurvedic 🌿
</footer>

<script>
document.getElementById("year").textContent = new Date().getFullYear();

/* AUTO TOTAL PRICE */
function calcTotal() {
    let total =
        (Neem.value * 50) +
        (Tulasi.value * 50) +
        (Aloe.value * 50) +
        (Goat.value * 50) +
        (Charcoal.value * 50) +
        (Turmeric.value * 50) +
        (Rice.value * 50) +
        (Bheem.value * 50) +
        (NFP.value * 30) +
        (MFP.value * 30);

    document.getElementById("totalAmount").value = total;
}

/* AUTO CALCULATE EVERY TIME USER TYPES */
document.querySelectorAll("input[type='number']").forEach(input=>{
    input.addEventListener("input", calcTotal);
});

/* SEND ORDER */
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
`🧾 *New Order Received*  
----------------------------------  
🧼 *Soap Quantities:*  
🍃 Neem: ${Neem.value}  
🌿 Tulasi: ${Tulasi.value}  
🍀 Aloe Vera: ${Aloe.value}  
🥛 Goat Milk: ${Goat.value}  
🖤 Charcoal: ${Charcoal.value}  
✨ Turmeric: ${Turmeric.value}  
🍚 Rice Potato: ${Rice.value}  
Bheem Sen Kapur: ${Bheem.value}  

🌸 *Face Pack:*  
🍃 Neem Leaf Pack: ${NFP.value}  
💧 Moisturizer Pack: ${MFP.value}  

----------------------------------  
💵 *Total Amount:* ₹${total}  

👤 *Customer Name:* ${name}  
📞 *Phone:* ${phone}  
🏠 *Address:*  
${addr}`;

    window.open(`https://wa.me/918888942084?text=${encodeURIComponent(msg)}`);
}
</script>

</body>
</html>
