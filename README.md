<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>MG Manisha Glow Ayurvedic</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
*{box-sizing:border-box}
body{
    margin:0;
    font-family:Arial, sans-serif;
    background:#fff8e6;
    color:#333;
}

/* HEADER */
header{
    background:#0f5c4d;
    color:white;
    padding:15px;
    text-align:center;
    font-size:26px;
    font-weight:bold;
}

/* CONTAINER */
.container{
    max-width:1200px;
    margin:auto;
    padding:20px;
    background:white;
}

/* PRODUCT */
.product{
    display:flex;
    flex-wrap:wrap;
    gap:30px;
}

/* IMAGES */
.product-images{
    flex:1;
    min-width:300px;
}
.product-images img{
    width:100%;
    border-radius:10px;
    border:1px solid #ddd;
}

/* DETAILS */
.product-details{
    flex:1;
    min-width:300px;
}
.product-details h1{
    color:#0f5c4d;
    font-size:30px;
}
.price{
    font-size:26px;
    color:#7b1e1e;
    font-weight:bold;
    margin:10px 0;
}
.badges span{
    display:inline-block;
    background:#e6f4ea;
    color:#0f5c4d;
    padding:6px 12px;
    border-radius:20px;
    margin:5px 5px 5px 0;
    font-size:14px;
}

/* BUTTONS */
.buttons{
    margin:20px 0;
}
.btn{
    padding:14px 22px;
    font-size:16px;
    border:none;
    border-radius:6px;
    cursor:pointer;
}
.cart{
    background:#0f5c4d;
    color:white;
}
.buy{
    background:#7b1e1e;
    color:white;
    margin-left:10px;
}

/* DESCRIPTION */
.section{
    margin-top:30px;
}
.section h2{
    color:#7b1e1e;
    border-bottom:2px solid #eee;
    padding-bottom:5px;
}
.section ul{
    padding-left:18px;
}

/* FOOTER */
footer{
    background:#0f5c4d;
    color:white;
    text-align:center;
    padding:20px;
    margin-top:40px;
}

/* MOBILE */
@media(max-width:768px){
    .product{
        flex-direction:column;
    }
}
</style>
</head>

<body>

<header>
🌿 MG Manisha Glow Ayurvedic
</header>

<div class="container">

    <div class="product">

        <!-- IMAGE -->
        <div class="product-images">
            <img src="soap.jpg" alt="Ayurvedic Soap">
        </div>

        <!-- DETAILS -->
        <div class="product-details">
            <h1>Ayurvedic Handmade Black Detox Soap</h1>

            <div class="price">₹249</div>

            <div class="badges">
                <span>✔ Handmade</span>
                <span>✔ Chemical Free</span>
                <span>✔ Ayurvedic</span>
                <span>✔ For All Skin Types</span>
            </div>

            <div class="buttons">
                <button class="btn cart">Add to Cart</button>
                <button class="btn buy">Buy Now</button>
            </div>

            <p>
                Our Ayurvedic Handmade Black Detox Soap is enriched with
                activated charcoal and natural herbs that deeply cleanse
                the skin, remove toxins and control acne.
            </p>
        </div>

    </div>

    <!-- DESCRIPTION -->
    <div class="section">
        <h2>Product Benefits</h2>
        <ul>
            <li>Removes dirt & toxins</li>
            <li>Controls acne & pimples</li>
            <li>Improves skin glow</li>
            <li>No chemicals, no parabens</li>
        </ul>
    </div>

    <div class="section">
        <h2>Ingredients</h2>
        <p>Activated Charcoal, Coconut Oil, Herbal Extracts, Essential Oils</p>
    </div>

</div>

<footer>
MG Manisha Glow Ayurvedic <br>
📞 8888942084 | 6351470697 <br>
🌿 Handmade Ayurvedic Products
</footer>

</body>
</html>
