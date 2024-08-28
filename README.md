<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Landing Page</title>
    <style>
        /* Basic reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Header styles */
        header {
            background-color: #333;
            color: #fff;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
            transition: background-color 0.3s ease;
        }

        header.scrolled {
            background-color: #222;
        }

        header .logo {
            float: left;
        }

        header nav {
            float: right;
        }

        header nav ul {
            list-style: none;
        }

        header nav ul li {
            display: inline;
            margin-left: 20px;
        }

        header nav ul li a {
            color: #fff;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        header nav ul li a:hover {
            color: #008CBA;
        }

        /* Hero section */
        .hero {
            background-color: #555; /* Placeholder background color */
            color: #fff;
            padding: 100px 0;
            text-align: center;
            margin-top: 60px; /* Adjust margin to account for fixed header */
        }

        .hero .btn {
            background-color: #008CBA;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
        }

        /* Footer styles */
        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 1rem 0;
        }

        /* Responsive styles */
        @media (max-width: 768px) {
            header nav {
                float: none;
                text-align: center;
            }

            header nav ul {
                padding: 0;
            }

            header nav ul li {
                display: block;
                margin: 10px 0;
            }
        }
    </style>
</head>
<body>
    <header id="header">
        <div class="container">
            <h1 class="logo">My Website</h1>
            <nav>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="home" class="hero">
        <div class="container">
            <h2>Welcome to My Website</h2>
            <p>This is a simple, clean, and responsive landing page.</p>
            <a href="#" class="btn">Learn More</a>
        </div>
    </section>

    <!-- Additional sections can be added here -->

    <footer>
        <div class="container">
            <p>&copy; 2024 My Website. All rights reserved.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
    </script>
</body>
</html>
