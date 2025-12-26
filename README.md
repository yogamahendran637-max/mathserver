# Ex.05 Design a Website for Server Side Processing
# Date:
# AIM:
To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side.

# FORMULA:
P = I2R
P --> Power (in watts)
 I --> Intensity
 R --> Resistance

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Create python programs for views and urls to perform server side processing.

## Step 5:
Create a HTML file to implement form based input and output.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>GOAT Bites Restaurant</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #fdfdfd;
    }
    header {
      background-color: #ff6f61 ;
      color: white;
      padding: 20px;
      text-align: center;
    }
    nav {
      display: flex;
      justify-content: center;
      background-color: #333;
    }
    nav a {
      color: white;
      padding: 14px 20px;
      text-decoration: none;
      text-align: center;
    }
    nav a:hover {
      background-color: #575757;
    }
    section {
      padding: 40px;
    }
    .dishes, .chefs {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .card {
      background-color: white;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      padding: 20px;
      text-align: center;
    }
    .card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 8px;
    }
    h2 {
      text-align: center;
      color: #000000;
      margin-bottom: 20px;
    }
    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 30px;
    }
    form {
      max-width: 500px;
      margin: auto;
    }
    input, textarea {
      width: 100%;
      padding: 10px;
      margin: 8px 0;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    button {
      background-color: #17ebdd;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #16b698;
    }
  </style>
</head>
<body>

<header>
  <h1>GOAT Bites</h1>
  <p>Fresh. Delicious. Made with Love.</p>
</header>

<nav>
  <a href="#home">Home</a>
  <a href="#food">Foods</a>
  <a href="#administration">Administration</a>
  <a href="#contact">Contact</a>
</nav>

<section id="home">
  <h2>Home</h2>
  <p style="text-align:center;">Welcome to Delish Bites, where passion meets flavor! Indulge in a culinary adventure with our exquisitely crafted dishes, made with fresh, high-quality ingredients and a whole lot of love. Come, savor the moment and explore a world of delicious possibilities! </p>
</section>

<section id="food">
  <h2>Our Food Menu</h2>
  <div class="dishes">
    <div class="card">
      <img src="Pizza Margherita Recipe.jpeg" alt="Margherita Pizza">
      <h3>Margherita Pizza</h3>
      <p>Tomatoes, mozzarella, and basil on crispy crust.</p>
    </div>
    <div class="card">
      <img src="Spaghetti Carbonara.jpg" alt="Spaghetti Carbonara">
      <h3>Spaghetti Carbonara</h3>
      <p>Rich and creamy with pancetta and parmesan.</p>
    </div>
    <div class="card">
      <img src="Cheeseburge.jpg" alt="Cheeseburger">
      <h3>Cheeseburger Deluxe</h3>
      <p>Juicy beef patty, cheese, and lettuce.</p>
    </div>
    <div class="card">
      <img src="Sushi Platter.jpg" alt="Sushi Platter">
      <h3>Sushi Platter</h3>
      <p>Fresh selection of sushi rolls and sashimi.</p>
    </div>
    <div class="card">
      <img src="Caesar Salad.jpg" alt="Caesar Salad">
      <h3>Caesar Salad</h3>
      <p>Classic salad with creamy dressing.</p>
    </div>
    <div class="card">
      <img src="Grilled Steak.jpg" alt="Grilled Steak">
      <h3>Grilled Steak</h3>
      <p>Perfectly grilled tender steak.</p>
    </div>
    <div class="card">
      <img src="Chocolate Lava Cake.jpg" alt="Chocolate Lava Cake">
      <h3>Chocolate Lava Cake</h3>
      <p>Melting chocolate goodness inside.</p>
    </div>
    <div class="card">
      <img src="Fluffy Pancakes.jpg" alt="Fluffy Pancakes">
      <h3>Fluffy Pancakes</h3>
      <p>Soft pancakes with maple syrup.</p>
    </div>
    <div class="card">
      <img src="Mexican Tacos.jpg" alt="Mexican Tacos">
      <h3>Mexican Tacos</h3>
      <p>Spiced meat and fresh toppings.</p>
    </div>
  </div>
</section>

<section id="administration">
  <h2>Our Chefs</h2>
  <div class="chefs">
    <div class="card">
      <img src="Chef Mario Rossi.jpg" alt="Chef Mario">
      <h3>Chef Mario Rossi</h3>
      <p>Master of Italian cuisine.</p>
    </div>
    <div class="card">
      <img src="sydney sweeney.jpg" alt="Sydney Sweeney">
      <h3>Chef Sydney Sweeney</h3>
      <p>Japanese sushi and traditional food expert.</p>
    </div>
    <div class="card">
      <img src="Amninder Sandhu.jpg" alt="Amninder Sandhu">
      <h3>Chef Amninder Sandhu</h3>
      <p>American grill and dessert innovator.</p>
    </div>
  </div>
</section>

<section id="contact">
  <h2>Contact Us</h2>
  <div class="contact-grid">
    <div class="card contact-box">
      <div class="contact-icon"><i class="fab fa-instagram"></i></div>
      <p><strong>Instagram</strong></p>
      <a href="https://www.instagram.com/_rabii.___" target="_blank">@goatbites</a>
    </div>
    <div class="card contact-box">
      <div class="contact-icon"><i class="fas fa-phone-alt"></i></div>
      <p><strong>Mobile</strong></p>
      <a href="tel:6969">+123 696</a>
    </div>
    <div class="card contact-box">
      <div class="contact-icon"><i class="fas fa-envelope"></i></div>
      <p><strong>Email</strong></p>
      <a href="mailto:your.email@goatbites.com">@goatbites.com</a>
    </div>
  </div>
</section>

<footer>
  <p>&copy; 2025 Delish Bites. All rights reserved.</p>
</footer>

<!-- JavaScript -->
<script>
  const form = document.getElementById('contactForm');
  form.addEventListener('submit', function(event) {
    event.preventDefault();
    const name = document.getElementById('name').value.trim();
    const email = document.getElementById('email').value.trim();
    const message = document.getElementById('message').value.trim();
    
    if(name && email && message) {
      alert(`Thank you, ${name}! We have received your message.`);
      form.reset();
    } else {
      alert('Please fill in all fields before submitting.');
    }
  });
</script>

</body>
</html>
```

# SERVER SIDE PROCESSING:
# HOMEPAGE:
![Uploading 440644775-cdddc5bf-8f42-404e-86dd-b25b7fbcf860.png…]()
![Uploading 440644830-4f194906-ed1c-4d3a-9536-b9079673c252.png…]()
![Uploading 440644894-1864e31f-4edf-4f62-90b6-838a345f14c9.png…]()
![Uploading 440644945-0458490d-13f3-42e6-accc-c8131511b64c.png…]()




# RESULT:
The program for performing server side processing is completed successfully.
