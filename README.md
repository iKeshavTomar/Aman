# Aman
<html lang="en"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Keshav Tomar - Personal Webpage</title>
    <style>
        body {
            font-family: Times New Roman, sans-serif;
            margin: 0;
            padding: 0;
            background-image: url("D:\StockCake-Sunlit Blossom Brilliance_1719892634.jpg");
            background-size: cover;
            color: #333;
        }
        header {
            background-color: rgba(46, 139, 87,0.3);
            color: white;
            padding: 1rem 0;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: rgba(51, 51, 51, 0.9);
        }
        nav a {
            color: white;
            padding: 1rem;
            text-decoration: none;
            text-align: center;
            transition: background-color 0.3s;
        }
        nav a:hover {
            background-color: rgba(46, 139, 87,0.5);
        }
        section {
            padding: 2rem;
            background-color: rgba(255, 255, 255, 0.9);
            margin: 1rem;
            border-radius: 8px;
            transition: opacity 0.5s;
        }
        footer {
            background-color: rgba(51, 51, 51, 0.9);
            color: white;
            text-align: center;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        #portfolio img {
            width: 100%;
            height: auto;
            max-width: 300px;
        }
        .hidden {
            display: none;
        }
        .visible {
            display: block;
            opacity: 1;
        }
    </style>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            const sections = document.querySelectorAll("section");
            const navLinks = document.querySelectorAll("nav a");

            function showSection(id) {
                sections.forEach(section => {
                    section.classList.add("hidden");
                    section.classList.remove("visible");
                });
                const targetSection = document.querySelector(id);
                targetSection.classList.remove("hidden");
                targetSection.classList.add("visible");
            }

            navLinks.forEach(link => {
                link.addEventListener("click", function(event) {
                    event.preventDefault();
                    const targetId = this.getAttribute("href");
                    showSection(targetId);
                });
            });

            // Show About section by default
            showSection("#about");
        });

        function submitContactForm(event) {
            event.preventDefault();
            alert("Thank you for your message!");
        }
    </script>
</head>
<body>

<header>
    <h1>Keshav Tomar</h1>
    <p>Welcome to my personal webpage!</p>
</header>

<nav>
    <a href="#about">About</a>
    <a href="#portfolio">Portfolio</a>
    <a href="#contact">Contact</a>
    <a href="#blog">Blog</a>
</nav>

<section id="about" class="visible">
    <h2>About Me</h2>
    <p>My name is Keshav Tomar. I am 17 years old and have recently passed 12th grade with 87.4% in PCM with Computer Science. I scored 88% in 10th grade. Currently, I am pursuing NDA coaching to further my career goals.</p>
</section>

<section id="portfolio" class="hidden">
    <h2>Portfolio</h2>
    <p>Here you can showcase your projects and achievements. This section will be updated with your work over time.</p>
    <img src="https://via.placeholder.com/300" alt="Sample Project">
</section>

<section id="contact" class="hidden">
    <h2>Contact</h2>
    <p>If you wish to get in touch with me, please fill out the form below:</p>
    <form onsubmit="submitContactForm(event)">
        <label for="name">Name:</label><br>
        <input type="text" id="name" name="name" required=""><br><br>
        <label for="email">Email:</label><br>
        <input type="email" id="email" name="email" required=""><br><br>
        <label for="message">Message:</label><br>
        <textarea id="message" name="message" required=""></textarea><br><br>
        <input type="submit" value="Submit">
    </form>
</section>

<section id="blog" class="hidden">
    <h2>Blog</h2>
    <p>Welcome to my blog! Here, I will share my thoughts, experiences, and updates on my journey. Stay tuned for more posts!</p>
</section>

<footer>
    <q>© 2024 Keshav Tomar. All rights reserved.</q>
</footer></body></html>
