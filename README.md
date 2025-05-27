# ayomikun-web-development-portfolio
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Onifade Praise Coffee Shop</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>
  <header>
    <h1>Praise's Coffee House</h1>
    <nav>
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#gallery">Gallery</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section id="hero">
    <h2>Welcome to Praise's Coffee House</h2>
    <p>Where every cup is a hug in a mug</p>
    <button onclick="scrollToContact()">Get in Touch</button>
  </section>

  <section id="about">
    <h2>About Us</h2>
    <p>Founded by Onifade Praise, our shop is a cozy haven for coffee lovers. We serve freshly brewed coffee and homemade pastries daily.</p>
  </section>

  <section id="menu">
    <h2>Our Menu</h2>
    <ul>
      <li>Espresso - #1500</li>
      <li>Cappuccino - #2000</li>
      <li>Latte - #2500</li>
      <li>Mocha - #1000</li>
      <li>Chocolate Muffin - #3000</li>
    </ul>
  </section>

  <section id="gallery">
    <h2>Gallery</h2>
    <div class="gallery-images">
      <img src="https://via.placeholder.com/200" alt="Coffee 1"/>
      <img src="https://via.placeholder.com/200" alt="Coffee 2"/>
      <img src="https://via.placeholder.com/200" alt="Interior"/>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Us</h2>
    <form id="contact-form">
      <input type="text" placeholder="Your Name" required/>
      <input type="email" placeholder="Your Email" required/>
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
    <p id="response"></p>
  </section>

  <footer>
    <p>© 2025 Onifade Praise Coffee House. All rights reserved.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
body {
  font-family: 'Segoe UI', sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.6;
  background: #fefcfb;
  color: #333;
}

header {
  background: #6f4e37;
  color: #fff;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

nav ul {
  list-style: none;
  display: flex;
  gap: 1rem;
}

nav a {
  color: #fff;
  text-decoration: none;
}

#hero {
  background: url('https://via.placeholder.com/800x300') no-repeat center center/cover;
  color: white;
  text-align: center;
  padding: 5rem 1rem;
}

section {
  padding: 2rem;
  text-align: center;
}

.gallery-images img {
  width: 200px;
  height: auto;
  margin: 1rem;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

form {
  max-width: 400px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

input, textarea {
  padding: 0.75rem;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  background: #6f4e37;
  color: white;
  border: none;
  padding: 0.75rem;
  cursor: pointer;
  border-radius: 5px;
  transition: background 0.3s ease;
}

button:hover {
  background: #4e342e;
}

footer {
  background: #ddd;
  text-align: center;
  padding: 1rem;
}
function scrollToContact() {
  document.getElementById("contact").scrollIntoView({ behavior: "smooth" });
}

document.getElementById("contact-form").addEventListener("submit", function (e) {
  e.preventDefault();
  document.getElementById("response").textContent = "Thank you for reaching out! We'll get back to you soon.";
  this.reset();
});
