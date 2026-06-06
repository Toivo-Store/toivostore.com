<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>TOIVO | Fashion & Accessories</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #000;
      color: #fff;
    }

    header {
      width: 100%;
      padding: 20px 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: #000;
      border-bottom: 1px solid #333;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    .logo {
      font-size: 28px;
      font-weight: bold;
      letter-spacing: 4px;
    }

    nav a {
      color: #fff;
      text-decoration: none;
      margin-left: 25px;
      font-size: 15px;
      transition: 0.3s;
    }

    nav a:hover {
      color: #aaa;
    }

    .hero {
      min-height: 90vh;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 60px 8%;
      background: linear-gradient(to right, #000 50%, #111);
    }

    .hero-text {
      max-width: 550px;
    }

    .hero-text h1 {
      font-size: 64px;
      line-height: 1.1;
      margin-bottom: 20px;
      text-transform: uppercase;
    }

    .hero-text p {
      font-size: 18px;
      color: #ccc;
      margin-bottom: 30px;
      line-height: 1.6;
    }

    .btn {
      display: inline-block;
      padding: 14px 32px;
      background: #fff;
      color: #000;
      text-decoration: none;
      font-weight: bold;
      border: 2px solid #fff;
      transition: 0.3s;
    }

    .btn:hover {
      background: transparent;
      color: #fff;
    }

    .hero-box {
      width: 380px;
      height: 480px;
      border: 2px solid #fff;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      font-size: 28px;
      font-weight: bold;
      letter-spacing: 3px;
      background: #111;
      box-shadow: 20px 20px 0 #fff;
      color: #fff;
    }

    section {
      padding: 70px 8%;
    }

    .section-title {
      text-align: center;
      font-size: 40px;
      margin-bottom: 45px;
      text-transform: uppercase;
      letter-spacing: 3px;
    }

    .categories {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 25px;
    }

    .category-card {
      border: 1px solid #444;
      padding: 45px 25px;
      text-align: center;
      background: #080808;
      transition: 0.3s;
    }

    .category-card:hover {
      background: #fff;
      color: #000;
      transform: translateY(-8px);
    }

    .category-card h3 {
      font-size: 24px;
      margin-bottom: 10px;
    }

    .category-card p {
      color: #aaa;
    }

    .category-card:hover p {
      color: #222;
    }

    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 30px;
    }

    .product-card {
      background: #080808;
      border: 1px solid #333;
      padding: 20px;
      transition: 0.3s;
    }

    .product-card:hover {
      transform: scale(1.03);
      border-color: #fff;
    }

    .product-img {
      height: 260px;
      background: linear-gradient(135deg, #222, #000);
      border: 1px solid #555;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #aaa;
      font-size: 20px;
      margin-bottom: 18px;
    }

    .product-card h3 {
      font-size: 21px;
      margin-bottom: 8px;
    }

    .price {
      color: #ccc;
      margin-bottom: 15px;
    }

    .product-card button {
      width: 100%;
      padding: 12px;
      background: #fff;
      color: #000;
      border: none;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }

    .product-card button:hover {
      background: #000;
      color: #fff;
      border: 1px solid #fff;
    }

    .about {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
      align-items: center;
    }

    .about-img {
      height: 360px;
      border: 2px solid #fff;
      background: #111;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 26px;
      font-weight: bold;
      letter-spacing: 2px;
    }

    .about-text h2 {
      font-size: 38px;
      margin-bottom: 20px;
    }

    .about-text p {
      color: #ccc;
      line-height: 1.8;
      font-size: 17px;
    }

    .newsletter {
      text-align: center;
      background: #fff;
      color: #000;
      padding: 60px 8%;
    }

    .newsletter h2 {
      font-size: 36px;
      margin-bottom: 15px;
    }

    .newsletter p {
      margin-bottom: 25px;
      color: #333;
    }

    .newsletter input {
      padding: 14px;
      width: 280px;
      border: 2px solid #000;
      outline: none;
      margin-right: 10px;
    }

    .newsletter button {
      padding: 14px 25px;
      background: #000;
      color: #fff;
      border: 2px solid #000;
      cursor: pointer;
      font-weight: bold;
    }

    .newsletter button:hover {
      background: #fff;
      color: #000;
    }

    footer {
      background: #000;
      color: #aaa;
      text-align: center;
      padding: 25px;
      border-top: 1px solid #333;
    }

    @media (max-width: 768px) {
      header {
        flex-direction: column;
        gap: 15px;
      }

      nav a {
        margin: 0 8px;
      }

      .hero {
        flex-direction: column;
        text-align: center;
        gap: 40px;
      }

      .hero-text h1 {
        font-size: 42px;
      }

      .hero-box {
        width: 280px;
        height: 360px;
        box-shadow: 10px 10px 0 #fff;
      }

      .about {
        grid-template-columns: 1fr;
        text-align: center;
      }

      .newsletter input {
        width: 100%;
        margin-bottom: 12px;
      }

      .newsletter button {
        width: 100%;
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="logo">TOIVO</div>
    <nav>
      <a href="#home">Home</a>
      <a href="#categories">Categories</a>
      <a href="#products">Shop</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero" id="home">
    <div class="hero-text">
      <h1>Streetwear Made Bold</h1>
      <p>
        Discover premium customized tees, fashion accessories, caps, chains,
        bags and more. Designed for Gen Z street style lovers.
      </p>
      <a href="#products" class="btn">Shop Now</a>
    </div>

    <div class="hero-box">
      BLACK<br>&<br>WHITE<br>STYLE
    </div>
  </section>

  <section id="categories">
    <h2 class="section-title">Categories</h2>

    <div class="categories">
      <div class="category-card">
        <h3>T-Shirts</h3>
        <p>Oversized and custom printed tees</p>
      </div>

      <div class="category-card">
        <h3>Accessories</h3>
        <p>Chains, rings, bracelets and more</p>
      </div>

      <div class="category-card">
        <h3>Caps</h3>
        <p>Minimal and streetwear headwear</p>
      </div>

      <div class="category-card">
        <h3>Bags</h3>
        <p>Tote bags and everyday fashion bags</p>
      </div>
    </div>
  </section>

  <section id="products">
    <h2 class="section-title">Featured Products</h2>

    <div class="products">
      <div class="product-card">
        <div class="product-img">Oversized Tee</div>
        <h3>Black Custom Tee</h3>
        <p class="price">₹799</p>
        <button onclick="addToCart('Black Custom Tee')">Add to Cart</button>
      </div>

      <div class="product-card">
        <div class="product-img">Silver Chain</div>
        <h3>Streetwear Chain</h3>
        <p class="price">₹499</p>
        <button onclick="addToCart('Streetwear Chain')">Add to Cart</button>
      </div>

      <div class="product-card">
        <div class="product-img">Cap</div>
        <h3>Minimal Black Cap</h3>
        <p class="price">₹599</p>
        <button onclick="addToCart('Minimal Black Cap')">Add to Cart</button>
      </div>

      <div class="product-card">
        <div class="product-img">Tote Bag</div>
        <h3>White Graphic Tote</h3>
        <p class="price">₹699</p>
        <button onclick="addToCart('White Graphic Tote')">Add to Cart</button>
      </div>
    </div>
  </section>

  <section class="about" id="about">
    <div class="about-img">
      TOIVO FASHION
    </div>

    <div class="about-text">
      <h2>About Our Brand</h2>
      <p>
        TOIVO is a modern fashion and accessories brand focused on bold,
        minimal, and custom streetwear. Our black and white style gives every
        product a clean, premium, and timeless look.
      </p>
    </div>
  </section>

  <section class="newsletter" id="contact">
    <h2>Join Our Fashion Club</h2>
    <p>Get updates on new drops, offers and exclusive designs.</p>

    <input type="email" placeholder="Enter your email" />
    <button onclick="subscribeUser()">Subscribe</button>
  </section>

  <footer>
    <p>© 2026 TOIVO Fashion & Accessories. All Rights Reserved.</p>
  </footer>

  <script>
    function addToCart(productName) {
      alert(productName + " added to cart!");
    }

    function subscribeUser() {
      alert("Thank you for subscribing to TOIVO!");
    }
  </script>

</body>
</html>
