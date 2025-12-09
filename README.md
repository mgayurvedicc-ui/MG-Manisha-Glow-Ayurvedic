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

.card {
    background: #ffffffdd;
    padding: 18px;
    border-radius: 12px;
    box-shadow: 0 6px 18px #0001;
    margin: 10px 0;
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

.order-box {
    background: #ffffffee;
    padding: 18px;
    border-radius: 12px;
    box-shadow: 0 5px 15px #0002;
    margin-top: 25px;
}

input, textarea, select {
    width: 100%;
    padding: 10px;
    margin-top: 6px;
    border-radius: 6px;
    border: 1px solid #ccc;
}

.bottom-logo { width: 110px; display: block; margin: 20px auto; }
.top-logo { width: 130px; display: block; margin: 20px auto; }

footer { text-align: center; padding: 20px; color: #777; }

</style>
</head>

<body>

<div class="container">

<!-- TOP LOGO -->
<img src="main-logo.jpg" class="top-logo">

<h1>MG Manisha Glow Ayurvedic</h1>
<h2>Premium Home-Made Ayurvedic Products</h2>

<!-- ORDER FORM -->
<div class="order-box">
<h2>🛒 Place Your Order</h2>

<label>Product चुनें:</label>
<select id="product">
    <option value="Neem Soap" data-price="50">Neem Soap (₹50)</option>
    <option value="Tulasi Soap" data-price="50">Tulasi Soap (₹50)</option>
    <option value="Aloe Vera Soap" data-price="50">Aloe Vera Soap (₹50)</option>
    <option value="Goat Milk Soap" data-price="50">Goat Milk Soap (₹50)</option>
    <option value="Charcoal Soap" data-price="50">Charcoal Soap (₹50)</option>
    <option value="Turmeric Soap" data-price="50">Turmeric Soap (₹50)</option>
    <option value="Rice Potato Soap" data-price="50">Rice Potato Soap (₹50)</option>
    <option value="Bheem Sen Kapur Alum Soap" data-price="50">Bheem Sen Kapur Alum (₹50)</option>

    <option value="Neem Leaf Powder Face Pack" data-price="30">Neem Leaf Powder Face Pack (₹30)</option>
    <option value="Moisturizer Face Pack" data-price="30">Moisturizer Face Pack (₹30)</option>
</select>

<label>Quantity:</label>
<input type="number" id="qty" placeholder="0" min="1">

<label>Customer Name:</label>
<input type="text" id="custname" placeholder="अपना नाम लिखें">

<label>Customer Address:</label>
<textarea id="address" placeholder="पूरा address लिखें"></textarea>

<label>Total Amount:</label>
<input type="text" id="total" readonly>

<button class="btn" onclick="placeOrder()">📩 Send Order on WhatsApp</button>
</div>

<!-- CONTACT DETAILS -->
<h2>📞 Contact Details</h2>
<div class="card">
    <p><b>Name:</b> MG Manisha Glow Ayurvedic</p>
    <p><b>Mobile:</b> 8888942084</p>
    <p><b>WhatsApp:</b> 8888942084</p>
    <p><b>Address:</b> At Post Rawande, Tal Kopargaon, Dist Ahilyanagar 423601</p>
    <p><b>Email:</b> mgayurvedicc@gmail.com</p>
    <p><b>Instagram:</b> @mg_manisha_glow_Ayurvedic_</p>
    <p><b>Website:</b> https://mgayurvedicc-ui.github.io/MG-Manisha-Glow-Ayurvedic/</p>
</div>

<!-- BOTTOM LOGO -->
<img src="main-logo.jpg" class="bottom-logo">

<footer>© <span id="year"></span> MG Manisha Glow Ayurvedic</footer>

</div>


<script>
document.getElementById("year").textContent = new Date().getFullYear();

// Auto calculate total when qty changes
document.getElementById("qty").addEventListener("input", function(){
    let product = document.getElementById("product");
    let price = product.options[product.selectedIndex].dataset.price;
    let qty = document.getElementById("qty").value;
    document.getElementById("total").value = qty * price;
});

// WhatsApp order system
function placeOrder(){
    let product = document.getElementById("product").value;
    let price = document.getElementById("product").options[product.selectedIndex].dataset.price;
    let qty = document.getElementById("qty").value;
    let name = document.getElementById("custname").value;
    let address = document.getElementById("address").value;
    let total = qty * price;

    if(!qty || !name || !address){
        alert("कृपया सभी details भरें!");
        return;
    }

    let msg = 
`🛒 *New Order*
------------------------
📦 Product: ${product}
🔢 Quantity: ${qty}
💰 Price: ₹${price}
💵 Total Amount: ₹${total}

👤 Customer Name: ${name}

🏠 Address:
${address}

धन्यवाद!`;

    window.open(`https://wa.me/918888942084?text=${encodeURIComponent(msg)}`);
}
</script>

</body>
</html>
