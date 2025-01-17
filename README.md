<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Welcome to my dynamic website">
    <title>Interactive Website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
        <nav>
            <ul>
                <li><a href="#about" onclick="toggleSection('about-desc')">About</a></li>
                <li><a href="#services" onclick="toggleSection('services-desc')">Services</a></li>
                <li><a href="#contact" onclick="toggleSection('contact-desc')">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="about">
            <h2>About Us</h2>
            <p id="about-desc" class="hidden">We are a company dedicated to providing exceptional services to our clients.</p>
        </section>

        <section id="services">
            <h2>Services</h2>
            <p id="services-desc" class="hidden">Our services include web development, app development, and digital marketing.</p>
        </section>

        <section id="contact">
            <h2>Contact Us</h2>
            <p id="contact-desc" class="hidden">You can reach us at contact@example.com or call us at 123-456-7890.</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 My Interactive Website. All rights reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

