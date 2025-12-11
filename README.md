<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8" />
<title>MG Manisha Glow Ayurvedic - Premium Invoice</title>

<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Marcellus&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>
body {
    font-family: 'Poppins', sans-serif;
    background: #f9f5e9;
    margin: 0;
    padding: 0;
}

.invoice-box {
    max-width: 850px;
    background: white;
    margin: 30px auto;
    padding: 25px 40px;
    border-radius: 18px;
    box-shadow: 0 8px 35px rgba(0,0,0,0.15);
    border: 4px solid #d4b36a;
}

.header {
    text-align: center;
    border-bottom: 3px solid #d4b36a;
    padding-bottom: 15px;
}

.header img {
    width: 130px;
    margin-bottom: -10px;
}

.brand-title {
    font-family: 'Marcellus', serif;
    font-size: 32px;
    color: #2e4a27;
    margin-top: 5px;
}

.tagline {
    color: #775f2b;
    margin-top: -5px;
    font-size: 15px;
}

/* Invoice Info */
.inv-details {
    margin-top: 20px;
    font-size: 15px;
    color: #333;
}

.section-title {
    font-weight: 600;
    margin-bottom: 6px;
    font-size: 18px;
    color: #2e4a27;
    border-left: 5px solid #d4b36a;
    padding-left: 8px;
}

/* Table */
table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 12px;
}

table th {
    background: #2e4a27;
    color: white;
    padding: 10px;
    font-weight: 500;
}

table td {
    padding: 10px;
    border-bottom: 1px solid #ddd;
}

/* Total box */
.total-box {
    text-align: right;
    font-size: 18px;
    margin-top: 15px;
    font-weight: 600;
    color: #2e4a27;
}

.btn {
    display: block;
    width: 100%;
    margin-top: 18px;
    padding: 12px;
    background: #2e4a27;
    border: none;
    color: white;
    border-radius: 8px;
    font-size: 16px;
    cursor: pointer;
}

.btn:hover {
    background: #3e6536;
}

.whatsapp {
    background: #128c7e;
}

.whatsapp:hover {
    background: #0d6f64;
}

</style>
</head>
<body>

<div class="invoice-box">

    <!-- HEADER -->
    <div class="header">
        <img src="main-logo.jpg" alt="Logo">
        <div class="brand-title">MG Manisha Glow Ayurvedic</div>
        <div class="tagline">Premium Ayurvedic Skin Care Products</div>
    </div>

    <!-- Invoice Top Info -->
    <div class="inv-details">
        <b>Invoice No:</b> <span id="invNo"></span><br>
        <b>Date:</b> <span id="invDate"></span>
    </div>

    <!-- Customer Section -->
    <div class="section-title">Customer Details</div>
    <p>
        <b>Name:</b> <span id="custName"></span><br>
        <b>Phone:</b> <span id="custPhone"></span><br>
        <b>Address:</b> <span id="custAddr"></span>
    </p>

    <!-- Product Table -->
    <div class="section-title">Order Summary</div>
    <table>
        <thead>
            <tr>
                <th>Product</th>
                <th>Qty</th>
                <th>Rate (₹)</th>
                <th>Total (₹)</th>
            </tr>
        </thead>
        <tbody id="itemTable"></tbody>
    </table>

    <!-- Total Amount -->
    <div class="total-box">
        Grand Total: ₹ <span id="grandTotal">0</span>
    </div>

    <!-- Buttons -->
    <button class="btn" onclick="downloadPDF()">📄 Download Invoice PDF</button>
    <button class="btn whatsapp" onclick="sendWhatsApp()">📩 Share on WhatsApp</button>

</div>

<!-- PDF LIBRARY -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>

<script>
/* AUTOFILL INVOICE DATA */
document.getElementById("invNo").innerText = "INV" + Math.floor(Math.random()*90000+10000);
document.getElementById("invDate").innerText = new Date().toLocaleDateString("en-IN");

/* SAMPLE ORDER DATA (आपकी वेबसाइट से आ सकता है) */
const order = {
    name: "Demo Customer",
    phone: "9876543210",
    addr: "Kopargaon, Ahilyanagar",
    items: [
        {name:"Neem Soap", qty:2, rate:50},
        {name:"Tulasi Soap", qty:1, rate:50},
        {name:"Charcoal Soap", qty:3, rate:50}
    ]
};

/* Fill Customer Data */
document.getElementById("custName").innerText = order.name;
document.getElementById("custPhone").innerText = order.phone;
document.getElementById("custAddr").innerText = order.addr;

/* Fill Items */
let total = 0;
let html = "";
order.items.forEach(item=>{
    let t = item.qty * item.rate;
    total += t;
    html += `<tr>
                <td>${item.name}</td>
                <td>${item.qty}</td>
                <td>${item.rate}</td>
                <td>${t}</td>
            </tr>`;
});
document.getElementById("itemTable").innerHTML = html;
document.getElementById("grandTotal").innerText = total;

/* DOWNLOAD PDF */
function downloadPDF(){
    const element = document.querySelector(".invoice-box");
    html2pdf().from(element).save("MG-Invoice.pdf");
}

/* WHATSAPP SHARE */
function sendWhatsApp(){
    let msg = `🧾 *MG Manisha Glow Invoice*\n\n` +
              `Customer: ${order.name}\nPhone: ${order.phone}\n` +
              `Total Amount: ₹${total}\n\n` +
              `Thank you for shopping 🌿`;
    window.open(`https://wa.me/?text=${encodeURIComponent(msg)}`);
}

</script>

</body>
</html>
