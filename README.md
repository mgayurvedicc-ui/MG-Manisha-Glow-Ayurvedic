<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MG Manisha Glow Ayurvedic</title>
  <style>
    body{
      margin:0;
      font-family:Arial, sans-serif;
      background:#f6f6f6;
    }
    header{
      background:#0f3d2e;
      color:#fff;
      padding:20px;
      text-align:center;
    }
    header img{
      width:90px;
      margin-bottom:10px;
    }
    .container{
      max-width:1100px;
      margin:auto;
      padding:30px 15px;
    }
    .products{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
      gap:25px;
    }
    .product{
      background:#fff;
      border-radius:12px;
      box-shadow:0 4px 12px rgba(0,0,0,0.1);
      padding:20px;
      text-align:center;
    }
    .product img{
      width:100%;
      max-height:260px;
      object-fit:contain;
    }
    .product h3{
      margin:15px 0 5px;
      color:#0f3d2e;
    }
    .price{
      font-size:22px;
      color:#b12704;
      margin:10px 0;
    }
    .btn{
      background:#0f3d2e;
      color:#fff;
      padding:10px 18px;
      border:none;
      border-radius:6px;
      cursor:pointer;
      font-size:15px;
    }
    .btn:hover{
      background:#145c44;
    }
    footer{
      background:#0f3d2e;
      color:#fff;
      text-align:center;
      padding:15px;
      margin-top:40px;
    }
  </style>
</head>
<body>

<header>
  <!-- LOGO -->
  <img src="images/logo.png" alt="MG Manisha Glow Ayurvedic" />
  <h1>MG Manisha Glow Ayurvedic</h1>
  <p>100% Homemade Ayurvedic Soaps</p>
</header>

<div class="container">
  <h2 style="text-align:center;margin-bottom:30px;">Our Products</h2>

  <div class="products">

    <!-- Charcoal Soap -->
    <div class="product">
      <img src="images/Charcoal.jpeg" alt="Charcoal Ayurvedic Soap" />
      <h3>Charcoal Ayurvedic Soap</h3>
      <p class="price">₹89</p>
      <button class="btn">Buy Now</button>
    </div>

    <!-- Kapoor Soap -->
    <div class="product">
      <img src="images/Kapoor.jpeg" alt="Kapoor Ayurvedic Soap" />
      <h3>Kapoor Ayurvedic Soap</h3>
      <p class="price">₹89</p>
      <button class="btn">Buy Now</button>
    </div>

    <!-- Neem Tulsi Soap -->
    <div class="product">
      <img src="images/Neem Tulsi.jpeg" alt="Neem Tulsi Ayurvedic Soap" />
      <h3>Neem Tulsi Ayurvedic Soap</h3>
      <p class="price">₹89</p>
      <button class="btn">Buy Now</button>
    </div>

  </div>
</div>

<footer>
  <p>© 2025 MG Manisha Glow Ayurvedic. All Rights Reserved.</p>
</footer>

</body>
</html>
