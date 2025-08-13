# Ex02 Commercial Website
## Date: 13/08/2025

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
### main.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WhizzRecipe</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <div class="logo">WhizzRecipe</div>
        <nav>
            <ul>
                <li><a href="#hero">Home</a></li>
                <li><a href="#recipes">Recipes</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="hero">
        <div class="hero-content">
            <h1>Cook Smarter, Eat Better</h1>
            <p>Discover quick, delicious, and healthy recipes tailored just for you.</p>
            <a href="#recipes" class="btn">Get Started</a>
        </div>
    </section>

    <!-- Recipes Section -->
    <section id="recipes">
  <h2>Our Popular Recipes</h2>
  <div class="recipe-grid">
    <div class="recipe-card">
      <img src="pasta.jpg" alt="Creamy Alfredo Pasta">
      <h3>Creamy Alfredo Pasta</h3>
    </div>
    <div class="recipe-card">
      <img src="cake.jpg" alt="Creamy Alfredo Pasta">
      <h3>Chocolate Lava Cake</h3>
    </div>
    <div class="recipe-card">
      <img src="salad.jpg" alt="Creamy Alfredo Pasta">
      <h3>Fresh Garden Salad</h3>
    </div>
  </div>
</section>


    <!-- About Section -->
    <section id="about">
        <h2>About WhizzRecipe</h2>
        <p>WhizzRecipe is your go-to destination for quick, healthy, and mouthwatering dishes. 
           Our mission is to make cooking simple and enjoyable for everyone, whether you're a 
           beginner in the kitchen or a seasoned chef. With our handpicked recipes and easy-to-follow steps, 
           you'll create meals that bring joy to the table.</p>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact Us</h2>
        <a href="mailto:contact@whizzrecipe.com" class="btn">Email Us</a>
        <a href="https://linkedin.com" target="_blank" class="btn">Call Us</a>
    </section>

    <footer>
        <p>© 2025 WhizzRecipe. All rights reserved.</p>
    </footer>

</body>
</html>
```
### style.css
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    line-height: 1.6;
}

/* Header */
header {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    padding: 20px 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 10;
}

.logo {
    color: #fff;
    font-size: 24px;
    font-weight: bold;
    position: absolute;
    left: 50px;
}

nav ul {
    display: flex;
    list-style: none;
}

nav ul li {
    margin-left: 20px;
}

nav ul li a {
    text-decoration: none;
    color: #fff;
    font-weight: 500;
    transition: 0.3s;
}

nav ul li a:hover {
    color: #ffae42;
}

/* Hero Section */
#hero {
    height: 100vh;
    position: relative;
    background: url('https://images.unsplash.com/photo-1504674900247-0877df9cc836?auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: #fff;
    padding: 0 20px;
}

#hero::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.4);
    z-index: 1;
}

.hero-content {
    position: relative;
    z-index: 2;
}

.hero-content h1 {
    font-size: 48px;
    margin-bottom: 15px;
}

.hero-content p {
    font-size: 18px;
    margin-bottom: 20px;
}

.btn {
    display: inline-block;
    padding: 10px 20px;
    background: #ffae42;
    color: #fff;
    text-decoration: none;
    border-radius: 5px;
    transition: 0.3s;
}

.btn:hover {
    background: #e69533;
}

/* Recipes Section */
#recipes {
    padding: 50px 20px;
    text-align: center;
}

.recipe-grid {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;
    margin-top: 20px;
}

.recipe-card {
    background: #fff;
    border-radius: 8px;
    overflow: hidden;
    width: 300px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.recipe-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.recipe-card h3 {
    padding: 15px;
}

/* About Section */
#about {
    padding: 50px 20px;
    background: #f8f8f8;
    text-align: center;
}

#about p {
    max-width: 800px;
    margin: auto;
    font-size: 18px;
}

/* Contact Section */
#contact {
    padding: 50px 20px;
    text-align: center;
}

#contact .btn {
    margin: 10px;
}

/* Footer */
footer {
    text-align: center;
    padding: 20px;
    background: #333;
    color: #fff;
}
```

## OUTPUT
<img width="1903" height="907" alt="image" src="https://github.com/user-attachments/assets/1bdb5604-a512-44a5-9dcc-f690a3dfa2b6" />
<img width="1897" height="527" alt="image" src="https://github.com/user-attachments/assets/35ed40a8-fe7e-470e-b72a-abd76d66234f" />
<img width="1890" height="315" alt="image" src="https://github.com/user-attachments/assets/863b77f0-77e3-4958-825d-757d13184a04" />
<img width="1895" height="255" alt="image" src="https://github.com/user-attachments/assets/d6dcf225-1653-4587-a7e5-08576a597d12" />





## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
