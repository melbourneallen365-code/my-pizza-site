<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pizza Brand</title>
<style>
:root {
  --red: #C0392B;
  --yellow: #F4D03F;
  --green: #27AE60;
  --cream: #FFF8F0;
  --black: #2C2C2C;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  background: var(--cream);
  color: var(--black);
}

/* NAVBAR */
nav {
  position: sticky;
  top: 0;
  background: white;
  display: flex;
  justify-content: space-between;
  padding: 15px 30px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  z-index: 1000;
}

nav ul {
  display: flex;
  list-style: none;
  gap: 20px;
}

nav a {
  text-decoration: none;
  color: var(--black);
  font-weight: bold;
}

/* HERO */
.hero {
  height: 100vh;
  background: url('https://images.unsplash.com/photo-1601924582975-7e33d6f2b8c6') center/cover no-repeat;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: white;
  position: relative;
}

.hero::after {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.5);
  top: 0;
  left: 0;
}

.hero-content {
  position: relative;
  z-index: 1;
  animation: fadeIn 1.5s ease-in-out;
}

.hero h1 {
  font-size: 3rem;
  margin-bottom: 10px;
}

.hero p {
  margin-bottom: 20px;
}

.btn {
  padding: 12px 25px;
  border: none;
  cursor: pointer;
  margin: 5px;
  font-weight: bold;
  transition: 0.3s;
}

.btn-primary {
  background: var(--red);
  color: white;
}

.btn-secondary {
  background: white;
  color: var(--black);
}

.btn:hover {
  transform: scale(1.05);
}

/* MENU */
.menu {
  padding: 50px 20px;
  text-align: center;
}

.menu-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin-top: 30px;
}

.card {
  background: white;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  transition: 0.3s;
}

.card:hover {
  transform: translateY(-5px);
}

.card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
}

.card-content {
  padding: 15px;
}

.price {
  color: var(--green);
  font-weight: bold;
}

/* DEALS */
.deals {
  background: var(--yellow);
  padding: 40px;
  text-align: center;
}

.badge {
  background: var(--red);
  color: white;
  padding: 5px 10px;
  margin-left: 10px;
}

/* STORY */
.story {
  padding: 50px 20px;
  text-align: center;
}

/* REVIEWS */
.reviews {
  background: #fff;
  padding: 50px 20px;
}

.review {
  margin: 20px 0;
}

/* LOCATION */
.location {
  padding: 50px 20px;
  text-align: center;
}

iframe {
  width: 100%;
  height: 300px;
  border: none;
}

/* FOOTER */
footer {
  background: var(--black);
  color: white;
  text-align: center;
  padding: 20px;
}

/* ANIMATIONS */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* MOBILE */
@media(max-width: 600px) {
  .hero h1 { font-size: 2rem; }
}

</style>
</head>
<body>

<!-- NAVBAR -->
<nav>
  <h2>Pizza🔥</h2>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#menu">Menu</a></li>
    <li><a href="#deals">Deals</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#contact">Contact</a></li>
    <li>🛒</li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-content">
    <h1>Hot. Fresh. Unforgettable Pizza.</h1>
    <p>Made with real ingredients. Delivered fast.</p>
    <button class="btn btn-primary">Order Now</button>
    <button class="btn btn-secondary">View Menu</button>
  </div>
</section>

<!-- MENU -->
<section class="menu" id="menu">
  <h2>Our Menu</h2>
  <div class="menu-grid">
    <div class="card">
      <img src="https://images.unsplash.com/photo-1594007654729-407eedc4be65">
      <div class="card-content">
        <h3>Jerk Chicken Pizza</h3>
        <p>Spicy Jamaican flavor</p>
        <p class="price">$10</p>
        <button class="btn btn-primary">Add to Cart</button>
      </div>
    </div>

    <div class="card">
      <img src="https://images.unsplash.com/photo-1548365328-9f547fb0953a">
      <div class="card-content">
        <h3>Veggie Pizza</h3>
        <p>Fresh garden toppings</p>
        <p class="price">$8</p>
        <button class="btn btn-primary">Add to Cart</button>
      </div>
    </div>
  </div>
</section>

<!-- DEALS -->
<section class="deals" id="deals">
  <h2>Special Deals</h2>
  <p>2 Large Pizzas for $15 <span class="badge">LIMITED</span></p>
</section>

<!-- STORY -->
<section class="story" id="about">
  <h2>Our Story</h2>
  <p>We started with one goal—real pizza made with real ingredients.</p>
</section>

<!-- REVIEWS -->
<section class="reviews">
  <h2>What Customers Say</h2>
  <div class="review">⭐⭐⭐⭐⭐ Best pizza in Montego Bay!</div>
</section>

<!-- LOCATION -->
<section class="location" id="contact">
  <h2>Find Us</h2>
  <p>Mon–Sun: 10AM–11PM</p>
  <iframe src="https://maps.google.com/maps?q=Montego%20Bay&t=&z=13&ie=UTF8&iwloc=&output=embed"></iframe>
</section>

<!-- FOOTER -->
<footer>
  <p>© 2026 Pizza Brand | Follow us on social media</p>
</footer>

</body>
</html>

