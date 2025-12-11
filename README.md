<script>

/* ---------- AUTO TOTAL ---------- */
function calcTotal() {
    const pricing = {
        Neem:50, Tulasi:50, Aloe:50, Goat:50,
        Charcoal:50, Turmeric:50, Rice:50, Bheem:50,
        NFP:30, MFP:30
    };

    let total = 0;
    for (let id in pricing) {
        const el = document.getElementById(id);
        let qty = parseInt(el.value) || 0;
        total += qty * pricing[id];
    }
    document.getElementById("totalAmount").value = total ? "₹ " + total : "";
}

document.querySelectorAll("input[type='number']").forEach(i =>
    i.addEventListener("input", calcTotal)
);


/* ---------- REPORTS DATA ---------- */
const REPORTS = {
neem:{
title:"🍃 Neem Soap - Lab Report",
data:`PH at 25°C: 6.13
Lather: 212 ml
Mush: 18.5 g
Free Caustic Alkali: Absent
Free Carbonated Alkali: Absent
Grittiness: Passed
Cracking: Passed
Cleaning Efficiency: Passed
Total Fatty Matter: 56.52%
Synthetic Surface Active Agent: 52.14
Fatty Matter From Dissolved Actives: 10.13`
},

tulasi:{
title:"🌿 Tulasi Soap - Lab Report",
data:`PH at 25°C: 5.89
Lather: 204.3 ml
Mush: 18.5 g
Free Caustic Alkali: Absent
Free Carbonated Alkali: Absent
Grittiness: Passed
Cracking: Passed
Cleaning Efficiency: Passed
Total Fatty Matter: 54.6%
Synthetic Surface Active Agent: 46.2
Fatty Matter From Dissolved Actives: 8.72`
},

charcoal:{
title:"🖤 Charcoal Soap - Lab Report",
data:`PH at 25°C: 6.64
Lather: 202 ml
Mush: 16.1 g
Free Caustic Alkali: Absent
Free Carbonated Alkali: Absent
Grittiness: Passed
Cracking: Passed
Cleaning Efficiency: Passed
Total Fatty Matter: 43%
Synthetic Surface Active Agent: 44.8
Fatty Matter From Dissolved Actives: 11.02`
},

turmeric:{
title:"✨ Turmeric Soap - Lab Report",
data:`PH at 25°C: 6.28
Lather: 216.5 ml
Mush: 22.3 g
Free Caustic Alkali: Absent
Free Carbonated Alkali: Absent
Grittiness: Passed
Cracking: Passed
Cleaning Efficiency: Passed
Total Fatty Matter: 64%
Synthetic Surface Active Agent: 45.1
Fatty Matter From Dissolved Actives: 18.0`
}
};


/* ---------- OPEN SHEET ---------- */
function openSheet(key){
    const r = REPORTS[key];
    document.getElementById("sheetTitle").innerText = r.title;

    let html = "<table>";
    r.data.split("\n").forEach(line=>{
        const [k,v] = line.split(":");
        html += `<tr><td>${k}</td><td>${v}</td></tr>`;
    });
    html += "</table>";

    document.getElementById("sheetContent").innerHTML = html;

    document.getElementById("sheetOverlay").style.display="flex";
    setTimeout(()=>document.getElementById("sheet").classList.add("open"),20);

    /* share report */
    document.getElementById("shareBtn").onclick = ()=>{
        const msg = r.title + "\n\n" + r.data;
        window.open("https://wa.me/?text="+encodeURIComponent(msg));
    };

    /* download as TXT */
    document.getElementById("pdfBtn").onclick = ()=>{
        const blob = new Blob([r.title+"\n\n"+r.data], {type:"text/plain"});
        const url = URL.createObjectURL(blob);
        const a=document.createElement("a");
        a.href=url;
        a.download=r.title+".txt";
        a.click();
    };
}

/* ---------- CLOSE SHEET ---------- */
function closeSheet(){
    document.getElementById("sheet").classList.remove("open");
    setTimeout(()=>document.getElementById("sheetOverlay").style.display="none",250);
}

document.getElementById("sheetOverlay").addEventListener("click",(e)=>{
    if(e.target.id==="sheetOverlay") closeSheet();
});


/* ---------- SEND ORDER ---------- */
function placeOrder(){
    let name=custName.value.trim();
    let phone=custPhone.value.trim();
    let addr=custAddr.value.trim();
    let total=totalAmount.value || "₹0";

    if(!name||!phone||!addr){
        alert("❗ कृपया Name, Phone और Address भरें!");
        return;
    }

    let msg=`🧾 New Order\n\nName: ${name}\nPhone: ${phone}\nAddress:\n${addr}\n\nTotal: ${total}`;
    window.open("https://wa.me/918888942084?text="+encodeURIComponent(msg));
}

</script>
