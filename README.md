# Ecommerce-website
my first E commerce website 
<br>
Author Shivam Meena
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>E-Commerce Website</title>

  <style>

    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:Arial, sans-serif;
    }

    body{
      background:#f4f4f4;
    }

    /* HEADER */

    header{
      background:#222;
      color:white;
      padding:15px 30px;
      display:flex;
      justify-content:space-between;
      align-items:center;
    }

    header h1{
      font-size:28px;
    }

    nav a{
      color:white;
      text-decoration:none;
      margin:0 10px;
      font-size:18px;
    }

    .cart{
      background:orange;
      padding:10px 15px;
      border-radius:5px;
      font-weight:bold;
    }

    /* HERO */

    .hero{
      background:linear-gradient(to right,#007bff,#00c6ff);
      color:white;
      text-align:center;
      padding:70px 20px;
    }

    .hero h2{
      font-size:45px;
      margin-bottom:10px;
    }

    /* PRODUCTS */

    .products{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
      gap:20px;
      padding:40px;
    }

    .product{
      background:white;
      border-radius:10px;
      padding:20px;
      text-align:center;
      box-shadow:0 2px 10px rgba(0,0,0,0.1);
    }

    .product img{
      width:100%;
      border-radius:10px;
    }

    .product h3{
      margin:15px 0;
    }

    .price{
      color:green;
      font-size:22px;
      margin-bottom:10px;
    }

    button{
      padding:10px 15px;
      border:none;
      border-radius:5px;
      cursor:pointer;
      margin:5px;
      color:white;
      background:#007bff;
    }

    button:hover{
      background:#0056b3;
    }

    /* MODAL */

    .modal{
      display:none;
      position:fixed;
      left:0;
      top:0;
      width:100%;
      height:100%;
      background:rgba(0,0,0,0.6);
    }

    .modal-content{
      background:white;
      width:400px;
      margin:100px auto;
      padding:30px;
      border-radius:10px;
      text-align:center;
    }

    .close{
      float:right;
      font-size:25px;
      cursor:pointer;
    }

    footer{
      background:#222;
      color:white;
      text-align:center;
      padding:15px;
      margin-top:20px;
    }

  </style>
</head>

<body>

  <!-- HEADER -->

  <header>

    <h1>🛒 E-Commerce Store</h1>

    <nav>
      <a href="#">Home</a>
      <a href="#">Products</a>
      <a href="#">Contact</a>
    </nav>

    <div class="cart">
      Cart: <span id="cart-count">0</span>
    </div>

  </header>

  <!-- HERO SECTION -->

  <section class="hero">

    <h2>Welcome to Our Store</h2>

    <p>Buy Amazing Products at Best Prices</p>

  </section>

  <!-- PRODUCTS -->

  <section class="products">

    <!-- PRODUCT 1 -->

    <div class="product">

      <img src="https://via.placeholder.com/250" alt="Product">

      <h3>Wireless Headphones</h3>

      <div class="price">₹1999</div>

      <button onclick="showDetails(
        'Wireless Headphones',
        'High quality sound with deep bass.',
        1999
      )">
        View Details
      </button>

      <button onclick="addToCart()">
        Add to Cart
      </button>

    </div>

    <!-- PRODUCT 2 -->

    <div class="product">

      <img src="https://via.placeholder.com/250" alt="Product">

      <h3>Smart Watch</h3>

      <div class="price">₹2999</div>

      <button onclick="showDetails(
        'Smart Watch',
        'Fitness tracking and smart notifications.',
        2999
      )">
        View Details
      </button>

      <button onclick="addToCart()">
        Add to Cart
      </button>

    </div>

    <!-- PRODUCT 3 -->

    <div class="product">

      <img src="https://via.placeholder.com/250" alt="Product">

      <h3>Gaming Mouse</h3>

      <div class="price">₹1499</div>

      <button onclick="showDetails(
        'Gaming Mouse',
        'RGB gaming mouse with fast response.',
        1499
      )">
        View Details
      </button>

      <button onclick="addToCart()">
        Add to Cart
      </button>

    </div>

  </section>

  <!-- PRODUCT DETAILS MODAL -->

  <div class="modal" id="modal">

    <div class="modal-content">

      <span class="close" onclick="closeModal()">
        &times;
      </span>

      <h2 id="title"></h2>

      <p id="description"></p>

      <h3 id="price"></h3>

      <br>

      <button onclick="buyNow()">
        Buy Now
      </button>

    </div>

  </div>

  <!-- FOOTER -->

  <footer>

    <p>© 2026 E-Commerce Website</p>

  </footer>

  <script>

    let cart = 0;

    /* ADD TO CART */

    function addToCart(){

      cart++;

      document.getElementById("cart-count").innerText = cart;

      alert("✅ Product Added to Cart");

    }

    /* SHOW PRODUCT DETAILS */

    function showDetails(name, description, price){

      document.getElementById("title").innerText = name;

      document.getElementById("description").innerText = description;

      document.getElementById("price").innerText =
        "Price: ₹" + price;

      document.getElementById("modal").style.display = "block";

    }

    /* CLOSE MODAL */

    function closeModal(){

      document.getElementById("modal").style.display = "none";

    }

    /* BUY NOW */

    function buyNow(){

      alert("🎉 Order Placed Successfully!");

      closeModal();

    }

  </script>

</body>
</html>
