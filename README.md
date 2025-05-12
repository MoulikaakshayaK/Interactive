# Ex.08 Design of Interactive Image Gallery
## Date:

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
home.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Golden Cuisine</title>
    <style>
      
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            box-sizing: border-box;
        }

        *, *::before, *::after {
            box-sizing: inherit;
        }

        header {
            background: #054c04;
            color: #333;
            padding: 10px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        header img {
            height: 40px;
        }

        header nav a {
            text-decoration: none;
            color: #f9f9f9;
            font-weight: bold;
            margin: 0 10px;
            transition: color 0.3s ease;
        }

        header nav a:hover {
            color: #ff5722;
        }

        .banner {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 30px 20px;
            background: url('bg.jpg') no-repeat center center/cover;
            color: white;
            height: 300px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.8);
        }

        .banner-content {
            max-width: 50%;
        }

        .banner-content h1 {
            font-family: Georgia, 'Times New Roman', Times, serif;
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: rgb(4, 82, 38);
        }

        .banner-content p {
            font-size: 1rem;
            margin-bottom: 15px;
            color: white;
        }

        .banner-content a {
            background: #ff5722;
            color: white;
            padding: 8px 15px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 5px;
            transition: background 0.3s ease;
        }

        .banner-content a:hover {
            background: #e64a19;
        }

        .features {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            padding: 20px;
            gap: 15px;
            background: #f9f9f9;
        }

        .feature {
            background: white;
            border-radius: 10px;
            padding: 15px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            flex: 1;
            text-align: center;
        }

        .feature img {
            width: 100%;
            border-radius: 10px;
            margin-bottom: 10px;
        }

        .feature h3 {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: #1f1714;
        }

        .feature p {
            font-size: 0.9rem;
            color: white;
        }

        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            margin-top: 10px;
        }

        footer a {
            color: #ff5722;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: #ffdd57;
        }

        @media (max-width: 768px) {
            .banner {
                flex-direction: column;
                height: auto;
                text-align: center;
            }

            .banner-content {
                max-width: 100%;
            }

            .features {
                flex-direction: column;
                gap: 20px;
            }

            .feature {
                flex: none;
            }

            header nav a {
                margin: 0 5px;
            }
        }
    </style>
</head>
<body>
      <header>
        <img src="logo.jpg">
        <nav>
            <a href="home.html">Home</a>
            <a href="menu.html">Menu</a>
            <a href="contact.html">Contact</a>
            <a href="admin.html">Administration</a>
        </nav>
    </header>

    <div class="banner">
        <div class="banner-content">
            <h1>Welcome to Golden Cuisine</h1>
            <p>A genuine fine-dining experience awaits.. We serve happiness on a plate!</p>
            <a href="#features">Explore Now</a>
        </div>
    </div>

    <section id="features" class="features">
        <div class="feature">
            <img src="fresh.jpg" alt="Fresh Ingredients">
            <h3>Fresh Ingredients</h3>
            <p>Freshness Focused: "Taste the freshness, enjoy the flavor".</p>
        </div>
        <div class="feature">
            <img src="ambient.jpg" alt="Cozy Ambiance">
            <h3>Cozy Ambiance</h3>
            <p>The Perfect Place to Relax and Reconnect.</p>
        </div>
        <div class="feature">
            <img src="reserve.jpg" alt="Easy Reservations">
            <h3>Easy Reservations</h3>
            <p>Book your table in seconds and guarantee yourself an unforgettable experience.</p>
        </div>
    </section>

    <footer>
        <p>&copy; Designed and developed by N.Hareni | <a href="#">Privacy Policy</a></p>
    </footer>

</body>
</html>

menu.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Golden Cuisine- Menu</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            box-sizing: border-box;
        }

        *, *::before, *::after {
            box-sizing: inherit;
        }

        header {
            background: #054c04;
            color: #fff;
            padding: 10px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        header nav a {
            text-decoration: none;
            color: #f9f9f9;
            font-weight: bold;
            margin: 0 10px;
            transition: color 0.3s ease;
        }

        header nav a:hover {
            color: #ffdd57;
        }

        header h1 {
            font-size: 1.5rem;
        }

        .menu-container {
            padding: 10px;
            background: #f9f9f9;
            text-align: center;
        }

        .menu-container h1 {
            font-size: 2rem;
            color: #054c04;
            margin-bottom: 15px;
        }

        .menu-items {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
        }

        .menu-item {
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 280px;
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .menu-item img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }

        .menu-item:hover {
            transform: scale(1.05);
        }

        .menu-details {
            padding: 10px;
        }

        .menu-details h3 {
            font-size: 1.2rem;
            color: #054c04;
            margin-bottom: 8px;
        }

        .menu-details p {
            font-size: 0.9rem;
            color: #555;
            margin-bottom: 10px;
        }

        .menu-details .price {
            font-weight: bold;
            font-size: 1rem;
            color: #ff5722;
        }

        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            margin-top: 10px;
        }

        footer a {
            color: #ff5722;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: #ffdd57;
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 1.2rem;
            }

            .menu-items {
                flex-direction: column;
                gap: 20px;
            }

            .menu-item {
                width: 100%;
            }

            header nav a {
                margin: 0 5px;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>Golden Cuisine</h1>
        <nav>
            <a href="home.html">Home</a>
            <a href="menu.html">Menu</a>
            <a href="contact.html">contact</a>
            <a href="admin.html">Administration</a>
        </nav>
    </header>

    <div class="menu-container">
        <h1>Our Menu</h1>
        <div class="menu-items">
            <div class="menu-item">
                <img src="pani puri.jpeg" alt="Biryani">
                <div class="menu-details">
                    <h3> Pani Puri</h3>
                    <p>Crispy puris filled with spicy, tangy water, mashed potatoes, chickpeas, and chutneys – an explosion of flavors in every bite! Served fresh for that authentic street food experience.</p>
                    <p class="price">₹170/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="pav bhaji.jpeg" alt="Curd rice">
                <div class="menu-details">
                    <h3> Pav Bhaji</h3>
                    <p>Spicy buttered vegetable mash served with toasted pav, onions, lemon, and extra butter.</p>
                    <p class="price">₹150/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="brownie.jpeg" alt="Brownie">
                <div class="menu-details">
                    <h3>Brownie</h3>
                    <p>Brownie topped with coffee chip ice cream, chocolate sauce, and your favorite sundae toppings.</p>
                    <p class="price">₹100/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="dosa.jpeg" alt="Dosa">
                <div class="menu-details">
                    <h3>Crispy dosa</h3>
                    <p>Crispy dosa with yummy taste.</p>
                    <p class="price">₹150/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="falooda.jpeg" alt="falooda">
                <div class="menu-details">
                    <h3>Falooda</h3>
                    <p> Chilled dessert drink with rose milk, vermicelli, basil seeds, jelly, and ice cream.</p>
                    <p class="price">₹150/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="gulab.jpeg" alt="gulab">
                <div class="menu-details">
                    <h3>Custard Gulab Jamun</h3>
                    <p>Soft gulab jamuns served chilled with creamy custard for a rich, delightful treat.</p>
                    <p class="price">₹180/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="pasta.jpeg" alt="">
                <div class="menu-details">
                    <h3>White Sauce Pasta</h3>
                    <p>Creamy, cheesy pasta tossed in rich white sauce with veggies and Italian herbs.</p>
                    <p class="price">₹180/-</p>
                </div>
            </div>


            <div class="menu-item">
                <img src="idly.jpeg" alt="Idly">
                <div class="menu-details">
                    <h3>Idly</h3>
                    <p>Idly is a soft & fluffy steamed cake made with fermented rice & lentil batter. </p>
                    <p class="price">₹70/-</p>
                </div>
            </div>


            <div class="menu-item">
                <img src="momos.jpeg" alt="momos">
                <div class="menu-details">
                    <h3>Momos</h3>
                    <p>Steamed or fried dumplings filled with veggies or meat, served with spicy dipping sauce.</p>
                    <p class="price">₹180/-</p>
                </div>
            </div>


            <div class="menu-item">
                <img src="fruit icecream.jpeg" alt="fruit icecream">
                <div class="menu-details">
                    <h3>Fruit Ice Cream</h3>
                    <p>Refreshing, creamy ice cream made with real fruit, offering a sweet and fruity indulgence. </p>
                    <p class="price">₹200/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="cutlet.jpeg" alt="cutlet">
                <div class="menu-details">
                    <h3>Cutlet</h3>
                    <p>Crispy, golden-fried patties filled with spiced vegetables or meat, served with tangy chutney.</p>
                    <p class="price">₹180/-</p>
                </div>
            </div>


            <div class="menu-item">
                <img src="hot chocolate.jpeg" alt="hot chocolate">
                <div class="menu-details">
                    <h3>Hot Chocolate</h3>
                    <p>Rich, creamy, and indulgent chocolate drink, perfect for cozy moments and cold weather.</p>
                    <p class="price">₹180/-</p>
                </div>
            </div>
         </div>
    </div>

    <footer>
        <p>&copy; designed and developed by N.Hareni| <a href="home.html">Back to Home</a></p>
    </footer>

</body>
</html>

contact.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Golden Cuisine- Contact Us</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            box-sizing: border-box;
        }

        *, *::before, *::after {
            box-sizing: inherit;
        }

        header {
            background: #054c04;
            color: #333;
            padding: 15px 30px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        header img {
            height: 50px;
        }

        header nav a {
            text-decoration: none;
            color: #f9f9f9;
            font-weight: bold;
            margin: 0 10px;
            transition: color 0.3s ease;
        }

        header nav a:hover {
            color: #ff5722;
        }

        .contact-banner {
            display: flex;
            align-items: center;
            justify-content: center;
            background: url('contacts.jpg') no-repeat center center/cover;
            height: 300px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.8);
        }

        .contact-banner h1 {
            font-family: Georgia, 'Times New Roman', Times, serif;
            font-size: 2.5rem;
            color: #f9f9f9;
        }

        .contact-section {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 30px 15px;
            background: #f9f9f9;
            gap: 20px;
        }

        .contact-details, .contact-form {
            flex: 1;
            max-width: 500px;
            margin: 10px;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .contact-details h2, .contact-form h2 {
            font-size: 1.8rem;
            margin-bottom: 15px;
            color: #1f1714;
            text-align: center;
        }

        .contact-details p {
            margin: 10px 0;
            font-size: 1rem;
            color: #555;
        }

        .contact-details img {
            max-width: 100%;
            border-radius: 10px;
            margin-bottom: 20px;
        }

        .contact-form input, .contact-form textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 1rem;
        }

        .contact-form textarea {
            height: 100px;
        }

        .contact-form button {
            width: 100%;
            padding: 10px;
            background: #ff5722;
            color: white;
            font-size: 1.1rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s ease;
        }

        .contact-form button:hover {
            background: #e64a19;
        }

        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 15px 0;
        }

        footer a {
            color: #ff5722;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: #ffdd57;
        }

        @media (max-width: 768px) {
            .contact-details, .contact-form {
                max-width: 100%;
            }

            .contact-banner h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <img src="logo.jpg">
        <nav>
            <a href="home.html">Home</a>
            <a href="menu.html">Menu</a>
            <a href="contact.html">Contact</a>
            <a href="admin.html">Administration</a>
        </nav>
    </header>

    <div class="contact-banner">
     
    </div>

    <section class="contact-section">
        <div class="contact-details">
            <h2>Get in Touch</h2>
            <img src="contact.jpeg" alt="Contact Us">
            <p><strong>Address:</strong> Golden Cuisine, Chennai, Tamilnadu, India</p>
            <p><strong>Phone:</strong> +91 1234567890</p>
            <p><strong>Email:</strong> contact@golden.com</p>
            <p><strong>Hours:</strong> Mon-Sun: 12:00 am -12:00 pm</p>
        </div>

        <div class="contact-form">
            <h2>Send Us a Message</h2>
            <form action="/submit-contact" method="POST">
                <label for="name">Full Name</label>
                <input type="text" id="name" name="name" placeholder="Enter your full name" required>

                <label for="email">Email Address</label>
                <input type="email" id="email" name="email" placeholder="Enter your email address" required>
         
                <label for="phone no">Phone Number</label>
                <input type="phone no" id="phone no" name="phone no" placeholder="Enter your phone number" required>

                <label for="message">Message</label>
                <textarea id="message" name="message" placeholder="Your message" required></textarea>

                <button type="submit">Send Message</button>
            </form>
        </div>
    </section>

    <footer>
        <p>&copy; designed and by developed by N.Hareni | <a href="#">Privacy Policy</a></p>
    </footer>

</body>
</html>

admin.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Golden Cuisine- Administration</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            box-sizing: border-box;
        }

        *, *::before, *::after {
            box-sizing: inherit;
        }

        header {
            background: #054c04;
            color: #fff;
            padding: 10px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        header nav a {
            text-decoration: none;
            color: #f9f9f9;
            font-weight: bold;
            margin: 0 10px;
            transition: color 0.3s ease;
        }

        header nav a:hover {
            color: #ffdd57;
        }

        header h1 {
            font-size: 1.5rem;
        }

        .admin-container {
            padding: 20px;
            background: #f9f9f9;
            text-align: center;
        }

        .admin-container h1 {
            font-size: 2rem;
            color: #054c04;
            margin-bottom: 20px;
        }

        .admin-items {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }

        .admin-item {
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 300px;
            overflow: hidden;
            transition: transform 0.3s ease;
            text-align: left;
        }

        .admin-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .admin-item:hover {
            transform: scale(1.05);
        }

        .admin-details {
            padding: 15px;
        }

        .admin-details h3 {
            font-size: 1.2rem;
            color: #054c04;
            margin-bottom: 8px;
        }

        .admin-details p {
            font-size: 0.9rem;
            color: #555;
            margin-bottom: 10px;
        }

        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            margin-top: 10px;
        }

        footer a {
            color: #ff5722;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: #ffdd57;
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 1.2rem;
            }

            .admin-items {
                flex-direction: column;
                gap: 20px;
            }

            .admin-item {
                width: 100%;
            }

            header nav a {
                margin: 0 5px;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>Golden Cuisine - admin</h1>
        <nav>
            <a href="home.html">Home</a>
            <a href="menu.html">Menu</a>
            <a href="contact.html">Contact</a>
            <a href="admin.html">Administration</a>
        </nav>
    </header>

   <div class="admin-container">
      <h1>Our Leadership Team</h1>
      <div class="admin-items">
          <div class="admin-item">
              <img src="Mary.jpeg" alt="Mary - Chief Executive Officer">
              <div class="admin-details">
                  <h3>Mary</h3>
                  <p>Chief Executive Officer - With over 15 years of experience in the hospitality industry, Mary leads Golden Cuisine with a strategic vision focused on guest satisfaction, business growth, and culinary innovation.</p>
              </div>
          </div>

          <div class="admin-item">
              <img src="John.jpeg" alt="John - Operations Manager">
              <div class="admin-details">
                  <h3>John</h3>
                  <p>Operations Manager - John brings a strong background in hotel management and front-of-house operations. He ensures daily activities run smoothly, from staff coordination to customer service quality. </p>
              </div>
          </div>

          <div class="admin-item">
              <img src="Williams.jpeg" alt="Williams - Executive Chef">
              <div class="admin-details">
                  <h3>Williams</h3>
                  <p>Executive Chef - A culinary artist with international training, Williams specializes in fusing classic techniques with modern flavors. He curates the restaurant’s signature menu, supervises kitchen operations.</p>
              </div>
          </div>

          <div class="admin-item">
              <img src="Sofia.jpeg" alt="Sofia - Deputy Director">
              <div class="admin-details">
                  <h3>Sofia</h3>
                  <p>Deputy Director - With expertise in business administration and hospitality services, Sofia supports strategic planning, staff training, and customer engagement programs.</p>
             </div>
          </div>
      </div>
  </div>
     <footer>
        <p>&copy; designed and developed by N.Hareni | <a href="home.html">Back to Home</a></p>
    </footer>

</body>
</html>

```

## OUTPUT:
![Screenshot 2025-05-12 215235](https://github.com/user-attachments/assets/d4e66c4d-8664-4cee-9c16-efa1e30cc2e7)
![Screenshot 2025-05-12 215316](https://github.com/user-attachments/assets/dbc5ba9a-37be-4aa6-993c-a731ab5eb6a4)
![Screenshot 2025-05-12 215339](https://github.com/user-attachments/assets/ad5cd9e2-f4fa-466f-8ca2-e86d00d4a56e)
![Screenshot 2025-05-12 215355](https://github.com/user-attachments/assets/a07974de-1e5d-4f9f-a63d-a1beffe8c920)
![Screenshot 2025-05-12 215429](https://github.com/user-attachments/assets/34a8a11e-4119-4b49-8e13-f088cfab0bf3)
![Screenshot 2025-05-12 215448](https://github.com/user-attachments/assets/38dd65a6-01fc-4223-b8bb-fea619f0ef65)






## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
