<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>MG Manisha Glow Ayurvedic</title>

<!-- jsPDF + html2canvas -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>

<style>
body{
    margin:0;
    font-family:Arial;
    background:#fffdf7;
}
.container{
    max-width:1100px;
    margin:auto;
    padding:20px;
}
h2{text-align:center;color:#184d47;}
.card{
    background:#ffffffee;
    padding:15px;
    border-radius:10px;
    box-shadow:0 4px 12px rgba(0,0,0,0.1);
}
.products, .facepack{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:15px;
}
.btn{
    background:#2e6b3f;
    color:white;
    padding:8px;
    border:none;
    width:100%;
    border-radius:6px;
    margin-top:8px;
}
.order-box{
    background:white;
    padding:20px;
    border-radius:12px;
    margin-top:25px;
    box-shadow:0 4px 15px rgba(0,0,0,0.1);
}
.order-box input, .order-box textarea{
    width:100%;
    padding:8px;
    margin-top:8px;
    border-radius:6px;
    border:1px solid #aaa;
}
.invoice-btn{
    background:#c9a032;
    padding:10px;
    width:100%;
    color:white;
    font-size:16px;
    border:none;
    border-radius:8px;
    margin-top:10px;
}

/* INVOICE PREVIEW BOX (Hidden) */
#invoicePreview{
    width:650px;
    padding:20px;
    background:#fdf7e3;
    border-radius:12px;
    border:2px solid #d4af37;
    display:none;
}
</style>
</head>
<body>

<div class="container">

<img src="main-logo.jpg" style="width:140px; display:block; margin:auto;">

<h2>🌿 MG Manisha Glow Ayurvedic</h2>

<h2>🧼 Soap Collection (₹50 Each)</h2>
<div class="products">

<div class="card"><h3>Neem Soap</h3><input id="Neem" type="number" min="0"></div>
<div class="card"><h3>Tulasi Soap</h3><input id="Tulasi" type="number" min="0"></div>
<div class="card"><h3>Aloe Vera Soap</h3><input id="Aloe" type="number" min="0"></div>
<div class="card"><h3>Goat Milk Soap</h3><input id="Goat" type="number" min="0"></div>
<div class="card"><h3>Charcoal Soap</h3><input id="Charcoal" type="number" min="0"></div>
<div class="card"><h3>Turmeric Soap</h3><input id="Turmeric" type="number" min="0"></div>
<div class="card"><h3>Rice Potato Soap</h3><input id="Rice" type="number" min="0"></div>
<div class="card"><h3>Bheem Sen Kapur Soap</h3><input id="Bheem" type="number" min="0"></div>

</div>

<h2>🌸 Face Pack Collection (₹30 Each)</h2>
<div class="facepack">

<div class="card"><h3>Neem Leaf Powder</h3><input id="NFP" type="number" min="0"></div>
<div class="card"><h3>Moisturizer Cream</h3><input id="MFP" type="number" min="0"></div>

</div>

<!-- ORDER FORM -->
<div class="order-box">
<h2>📝 Customer Details</h2>

<input id="custName" type="text" placeholder="Name">
<input id="custPhone" type="text" placeholder="Phone">
<textarea id="custAddr" placeholder="Full Address"></textarea>

<input id="totalAmount" type="text" readonly placeholder="Total Amount">

<button class="btn" onclick="placeOrder()">📩 Send WhatsApp Order</button>
<button class="invoice-btn" onclick="generatePDF()">📄 Download Invoice</button>
</div>

</div>

<!-- INVOICE HIDDEN PREVIEW -->
<div id="invoicePreview">

<div style="text-align:center;">
    <img src="main-logo.jpg" style="width:120px;">
    <h2>MG MANISHA GLOW AYURVEDIC</h2>
    <p>Premium Ayurvedic Products Invoice</p>
    <hr>
</div>

<div id="invoiceItems"></div>

<h3 id="invoiceTotal" style="text-align:right;"></h3>

</div>

<script>
/* AUTO TOTAL */
function calcTotal(){
    const pricing={Neem:50,Tulasi:50,Aloe:50,Goat:50,Charcoal:50,Turmeric:50,Rice:50,Bheem:50,NFP:30,MFP:30};
    let total=0;
    for(let p in pricing){
        let qty=parseInt(document.getElementById(p).value)||0;
        total+=qty*pricing[p];
    }
    totalAmount.value = total ? "₹ " + total : "";
}
document.querySelectorAll("input[type='number']").forEach(i=>i.addEventListener("input",calcTotal));


/* WHATSAPP ORDER */
function placeOrder(){
    let name=custName.value.trim();
    let phone=custPhone.value.trim();
    let addr=custAddr.value.trim();
    let total=totalAmount.value||"₹0";

    if(!name||!phone||!addr){
        alert("Please fill all fields!");
        return;
    }

    const pricing={Neem:50,Tulasi:50,Aloe:50,Goat:50,Charcoal:50,Turmeric:50,Rice:50,Bheem:50,NFP:30,MFP:30};

    let list="";
    for(let p in pricing){
        let qty=parseInt(document.getElementById(p).value)||0;
        if(qty>0){
            list += `• ${p} — ${qty} qty = ₹${qty*pricing[p]}\n`;
        }
    }
    if(list==="") list="No items selected";

    let msg=`🧾 *New Order*\n\n👤 *Name:* ${name}\n📞 *Phone:* ${phone}\n🏠 *Address:* ${addr}\n\n📦 *Items:*\n${list}\n💵 *Total:* ${total}`;
    window.open("https://wa.me/918888942084?text="+encodeURIComponent(msg));
}


/* PDF GENERATOR */
function generatePDF(){
    const pricing={Neem:50,Tulasi:50,Aloe:50,Goat:50,Charcoal:50,Turmeric:50,Rice:50,Bheem:50,NFP:30,MFP:30};
    
    let html="<h3>Order Summary</h3><table style='width:100%;font-size:14px'>";
    html+="<tr><th align='left'>Item</th><th>Qty</th><th>Amount</th></tr>";

    let total=0;

    for(let p in pricing){
        let qty=parseInt(document.getElementById(p).value)||0;
        if(qty>0){
            let amt=qty*pricing[p];
            total+=amt;
            html+=`<tr><td>${p}</td><td align="center">${qty}</td><td align="right">₹${amt}</td></tr>`;
        }
    }

    html+="</table>";
    invoiceItems.innerHTML=html;
    invoiceTotal.innerHTML="Total: ₹"+total;

    const box=document.getElementById("invoicePreview");
    box.style.display="block";

    html2canvas(box).then(canvas=>{
        const img=canvas.toDataURL("image/png");
        const pdf=new jspdf.jsPDF("p","mm","a4");
        let w=pdf.internal.pageSize.getWidth();
        let h=canvas.height * w / canvas.width;
        pdf.addImage(img,"PNG",0,0,w,h);
        pdf.save("MG-Invoice.pdf");
    });
}
</script>

</body>
</html>
