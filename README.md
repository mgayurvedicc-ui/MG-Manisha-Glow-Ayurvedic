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
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 15px;
}
.card {
    background: rgba(255,255,255,0.90);
    padding: 18px;
    border-radius: 12px;
    box-shadow: 0 6px 18px rgba(0,0,0,0.1);
}
.card input {
    width: 100%;
    padding: 8px;
    margin-top: 6px;
    border-radius: 6px;
    border: 1px solid #ccc;
}

.order-box {
    background: rgba(255,255,255,0.92);
    padding: 20px;
    border-radius: 12px;
    margin-top: 30px;
    box-shadow: 0 6px 18px rgba(0,0,0,0.1);
}

.order-box input, .order-box textarea {
    width: 100%;
    padding: 10px;
    margin-top: 8px;
    border-radius: 6px;
    border: 1px solid #bbb;
}

.btn {
    background: #6b8e23;
    color: white;
    padding: 12px;
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

<div class="card">
    <h3>Neem Soap</h3>
    <label>Quantity:</label>
    <input type="number" id="Neem" min="0" placeholder="0">
</div>

<div class="card">
    <h3>Tulasi Soap</h3>
    <label>Quantity:</label>
    <input type="number" id="Tulasi" min="0" placeholder="0">
</div>

<div class="card">
    <h3>Aloe Vera Soap</h3>
    <label>Quantity:</label>
    <input type="number" id="Aloe" min="0" placeholder="0">
</div>

<div class="card">
    <h3>Goat Milk Soap</h3>
    <label>Quantity:</label>
    <input type="number" id="Goat" min="0" placeholder="0">
</div>

<div class="card">
    <h3>Charcoal Soap</h3>
    <label>Quantity:</label>
    <input type="number" id="Charcoal" min="0" placeholder="0">
</div>

<div class="card">
    <h3>Turmeric Soap</h3>
    <label>Quantity:</label>
    <input type="number" id="Turmeric" min="0" placeholder="0">
</div>

<div class="card">
    <h3>Rice Potato Soap</h3>
    <label>Quantity:</label>
    <input type="number" id="Rice" min="0" placeholder="0">
</div>

<div class="card">
    <h3>Bheem Sen Kapur Alum Soap</h3>
    <label>Quantity:</label>
    <input type="number" id="Bheem" min="0" placeholder="0">
</div>

</div>


<!-- FACE PACK SECTION -->
<h2>🌿 Face Pack (₹30 Each)</h2>
<div class="facepack">

<div class="card">
    <h3>Neem Leaf Powder Face Pack</h3>
    <label>Quantity:</label>
    <input type="number" id="NFP" min="0" placeholder="0">
</div>

<div class="card">
    <h3>Moisturizer Face Pack</h3>
    <label>Quantity:</label>
    <input type="number" id="MFP" min="0" placeholder="0">
</div>

</div>


<!-- ORDER FORM -->
<div class="order-box">
<h2>📝 Customer Details</h2>

<label>Your Name:</label>
<input type="text" id="custName">

<label>Phone Number:</label>
<input type="text" id="custPhone">

<label>Address:</label>
<textarea id="custAddr"></textarea>

<label>Total Amount:</label>
<input type="text" id="grandTotal" readonly>

<button class="btn" onclick="calculateGrandTotal()">Total Calculate करें</button>
<button class="btn" onclick="placeOrder()">WhatsApp Order भेजें</button>
</div>


<img src="main-logo.jpg" class="bottom-logo">

<footer>© <span id="year"></span> MG Manisha Glow Ayurvedic</footer>

</div>


<script>
document.getElementById("year").textContent = new Date().getFullYear();

/* CALCULATE TOTAL */
function calculateGrandTotal(){
    let soapPrice = 50;
    let facePrice = 30;

    let total = 
      (document.getElementById("Neem").value * soapPrice) +
      (document.getElementById("Tulasi").value * soapPrice) +
      (document.getElementById("Aloe").value * soapPrice) +
      (document.getElementById("Goat").value * soapPrice) +
      (document.getElementById("Charcoal").value * soapPrice) +
      (document.getElementById("Turmeric").value * soapPrice) +
      (document.getElementById("Rice").value * soapPrice) +
      (document.getElementById("Bheem").value * soapPrice) +

      (document.getElementById("NFP").value * facePrice) +
      (document.getElementById("MFP").value * facePrice);

    document.getElementById("grandTotal").value = total;
}

/* SEND ORDER */
function placeOrder(){
    let name = document.getElementById("custName").value;
    let phone = document.getElementById("custPhone").value;
    let addr = document.getElementById("custAddr").value;
    let total = document.getElementById("grandTotal").value;

    if(!name || !phone || !addr){
        alert("कृपया Name, Phone, Address भरें!");
        return;
    }

    let msg = 
`🛒 *New Order*
----------------------

*Quantities:*
Neem Soap: ${Neem.value}
Tulasi Soap: ${Tulasi.value}
Aloe Vera Soap: ${Aloe.value}
Goat Milk Soap: ${Goat.value}
Charcoal Soap: ${Charcoal.value}
Turmeric Soap: ${Turmeric.value}
Rice Potato Soap: ${Rice.value}
Bheem Alum Soap: ${Bheem.value}

Neem Leaf Face Pack: ${NFP.value}
Moisturizer Face Pack: ${MFP.value}

----------------------
💵 *Total Amount:* ₹${total}

👤 *Customer:* ${name}
📞 *Phone:* ${phone}
🏠 *Address:* 
${addr}

धन्यवाद 🙏`;

    window.open(`https://wa.me/918888942084?text=${encodeURIComponent(msg)}`);
}
</script>

</body>
</html>
