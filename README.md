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
        alert("कृपया Name, Phone आणि Address भरा!");
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
धन्यवाद आम्हाला Order दिल्या बद्दल 🙏  
नक्कीच तुम्हाला आमचा Product आवडेल व तुम्हाला फायदा होईल 🙏  
लवकरात लवकर तुमची Order तुमच्या पर्यंत पोहचवू  
धन्यवाद 🙏🙏`;

    window.open(`https://wa.me/918888942084?text=${encodeURIComponent(msg)}`);
}
</script>
