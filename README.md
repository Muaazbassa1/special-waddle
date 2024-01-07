<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>We Get For You - Your Online Marketplace</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1 style="color: green; text-align: center;">We Get For You - Your Online Marketplace</h1>
    </header>

    <nav>
        <ul>
            <li><a href="#" onclick="showHome()">Home</a></li>
            <li><a href="#" onclick="showCommunication()">Communication</a></li>
        </ul>
    </nav>

    <!-- Home Section -->
    <section id="home" style="display: block;">
        <main>
            <h2 style="text-align: center;">Welcome to We Get For You!</h2>
            <p>Discover a wide range of products and services...</p>

            <!-- Featured Products Section -->
            <section id="featured-products">
                <h3 style="text-align: center;">Featured Products</h3>
                <div class="product">
                    <img src="product1.jpg" alt="Product 1">
                    <h4>Product 1</h4>
                    <p>Description of Product 1...</p>
                </div>

                <div class="product">
                    <img src="product2.jpg" alt="Product 2">
                    <h4>Product 2</h4>
                    <p>Description of Product 2...</p>
                </div>
                <!-- Add more products as needed -->
            </section>

            <!-- Latest News Section -->
            <section id="latest-news">
                <h3 style="text-align: center;">Latest News</h3>
                <article>
                    <h4>News Title 1</h4>
                    <img src="news1.jpg" alt="News Image 1">
                    <p>Summary of the latest news...</p>
                </article>

                <article>
                    <h4>News Title 2</h4>
                    <img src="news2.jpg" alt="News Image 2">
                    <p>Summary of another news article...</p>
                </article>
                <!-- Add more news articles as needed -->
            </section>

            <!-- Special Offers Section -->
            <section id="special-offers">
                <h3 style="text-align: center;">Special Offers</h3>
                <div class="offer">
                    <h4>Special Offer 1</h4>
                    <p>Details of the special offer...</p>
                </div>

                <div class="offer">
                    <h4>Special Offer 2</h4>
                    <p>Details of another special offer...</p>
                </div>
                <!-- Add more special offers as needed -->
            </section>

        </main>
    </section>

    <!-- Communication Section -->
    <section id="communication" style="display: none;">
        <main>
            <h2 style="text-align: center;">Communication</h2>
            <p style="text-align: center;">Talk to others using your email.</p>

            <!-- Chat Form -->
            <form action="#" method="post" onsubmit="sendMessage()">
                <label for="email">Your Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="message">Your Message:</label>
                <textarea id="message" name="message" rows="4" required></textarea>

                <input type="submit" value="Send Message">
            </form>

            <!-- Display Messages -->
            <div id="messageDisplay"></div>

            <!-- WhatsApp Link -->
            <p style="text-align: center;">
                Contact us on WhatsApp: <a href="https://wa.me/1234567890?text=Hello%20from%20We%20Get%20For%20You" target="_blank">Chat Now</a>
            </p>
        </main>
    </section>

    <footer>
        <p style="text-align: center;">&copy; 2024 Your Online Marketplace</p>
    </footer>

    <script src="main.js" defer></script>
    <script>
        function showHome() {
            document.getElementById('home').style.display = 'block';
            document.getElementById('communication').style.display = 'none';
        }

        function showCommunication() {
            document.getElementById('home').style.display = 'none';
            document.getElementById('communication').style.display = 'block';
        }

        function sendMessage() {
            // Add your logic to handle the message (e.g., display it on the page).
            var email = document.getElementById('email').value;
            var message = document.getElementById('message').value;
            var messageDisplay = document.getElementById('messageDisplay');
            messageDisplay.innerHTML += '<p><strong>' + email + ':</strong> ' + message + '</p>';

            // Clear the input fields
            document.getElementById('email').value = '';
            document.getElementById('message').value = '';

            // Prevent the form from submitting and refreshing the page
            return false;
        }
    </script>
</body>
</html>

