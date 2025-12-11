<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MG Manisha Glow Ayurvedic – Premium Invoice</title>
<style>
    body {
        margin: 0;
        font-family: 'Poppins', sans-serif;
        background: linear-gradient(135deg, #002d18, #0b5e36, #d4af37);
        color: #fff;
        padding: 20px;
    }

    .container {
        max-width: 900px;
        margin: auto;
        background: rgba(255,255,255,0.08);
        padding: 25px;
        border-radius: 15px;
        backdrop-filter: blur(10px);
        border: 1px solid rgba(255,255,255,0.2);
    }

    .header {
        text-align: center;
        margin-bottom: 20px;
    }

    .header img {
        width: 120px;
    }

    h2 {
        color: #ffd700;
        margin-bottom: 5px;
    }

    label {
        font-weight: 600;
    }

    input, select {
        width: 100%;
        padding: 10px;
        border: none;
        border-radius: 8px;
        margin: 6px 0 15px;
        font-size: 16px;
    }

    button {
        width: 100%;
        padding: 12px;
        background: #ffd700;
        border: none;
        border-radius: 10px;
        color: #000;
        font-size: 18px;
        font-weight: 700;
        cursor: pointer;
        transition: 0.2s;
    }

    button:hover {
        background: #ffcc00;
    }

    table {
        width: 100%;
        margin-top: 20px;
        border-collapse: collapse;
        background: rgba(0,0,0,0.3);
        border-radius: 10px;
        overflow: hidden;
    }

    table th, table td {
        padding: 12px;
        text-align: left;
        border-bottom: 1px solid rgba(255,255,255,0.2);
    }

    table th {
        background: rgba(255,215,0,0.2);
        color: #ffd700;
        font-size: 17px;
    }

    .total-box {
        text-align: right;
        margin-top: 15px;
        font-size: 22px;
        font-weight: 600;
        color: #ffd700;
    }

    .invoice-box {
        background: rgba(255,255,255,0.1);
        padding: 20px;
        border-radius: 12px;
        margin-top: 25px;
    }
</style>
</head>
<body>

<div class="container">

    <div class="header">
        <img src="main logo.jpg" alt="Logo">
        <h2>MG Manisha Glow Ayurvedic - Premium Invoice</h2>
    </div>

    <!-- Customer Details -->
    <label>Customer Name</label>
    <input type="text" id="custName" placeholder="Enter customer name">

    <label>Phone Number</label>
    <input type="text" id="custPhone" placeholder="Enter phone number">

    <label>Address</label>
    <input type="text" id="custAddress" placeholder="Enter address">


    <!-- Product Dropdown -->
    <label>Select Product</label>
    <select id="productList">
        <option value="Neem Tulsi Soap|70">Neem Tulsi Soap — ₹70</option>
        <option value="Aloe Vera Soap|80">Aloe Vera Soap — ₹80</option>
        <option value="Red Sandal Soap|90">Red Sandal Soap — ₹90</option>
        <option value="MG Glow Premium Soap|120">MG Glow Premium Soap — ₹120</option>
    </select>

    <label>Quantity</label>
    <input type="number" id="qty" min="1" value="1">

    <button onclick="addItem()">Add Item</button>


    <!-- Invoice Table -->
    <table id="invoiceTable" style="display:none;">
        <thead>
            <tr>
                <th>Product</th>
                <th>Qty</th>
                <th>Price</th>
                <th>Total</th>
            </tr>
        </thead>
        <tbody id="tableBody"></tbody>
    </table>

    <div class="total-box" id="grandTotalBox" style="display:none;">Grand Total: ₹0</div>

    <button onclick="generatePDF()" id="pdfBtn" style="display:none;margin-top:20px;">Download PDF Invoice</button>
    <button onclick="sendWhatsApp()" id="waBtn" style="display:none;margin-top:15px;background:#25D366;color:#fff;">Send on WhatsApp</button>

</div>


<!-- JS SECTION -->
<script>
let totalAmount = 0;
let rows = [];

function addItem() {
    const selected = document.getElementById("productList").value.split("|");
    const name = selected[0];
    const price = parseInt(selected[1]);
    const qty = parseInt(document.getElementById("qty").value);
    const lineTotal = price * qty;

    rows.push({name, qty, price, lineTotal});
    totalAmount += lineTotal;

    updateTable();
}

function updateTable() {
    const table = document.getElementById("invoiceTable");
    const body = document.getElementById("tableBody");
    const grandTotal = document.getElementById("grandTotalBox");
    const pdfBtn = document.getElementById("pdfBtn");
    const waBtn = document.getElementById("waBtn");

    table.style.display = "table";
    grandTotal.style.display = "block";
    pdfBtn.style.display = "block";
    waBtn.style.display = "block";

    body.innerHTML = "";

    rows.forEach(r => {
        body.innerHTML += `
            <tr>
                <td>${r.name}</td>
                <td>${r.qty}</td>
                <td>₹${r.price}</td>
                <td>₹${r.lineTotal}</td>
            </tr>
        `;
    });

    grandTotal.innerHTML = `Grand Total: ₹${totalAmount}`;
}

function sendWhatsApp() {
    const name = document.getElementById("custName").value;
    const phone = document.getElementById("custPhone").value;
    const address = document.getElementById("custAddress").value;

    let msg = `*MG MANISHA GLOW AYURVEDIC*%0A%0A`;
    msg += `*Customer:* ${name}%0A`;
    msg += `*Phone:* ${phone}%0A`;
    msg += `*Address:* ${address}%0A%0A`;

    msg += `*Order Details:*%0A`;
    rows.forEach(r => {
        msg += `${r.name} (${r.qty} × ₹${r.price}) = ₹${r.lineTotal}%0A`;
    });

    msg += `%0A*Grand Total:* ₹${totalAmount}`;

    window.open(`https://wa.me/${phone}?text=${msg}`, "_blank");
}

function generatePDF() {
    alert("PDF Feature Next Update 🔥 (Fully Auto PDF)");
}
</script>

</body>
</html>
