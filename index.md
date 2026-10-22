Assignment 7.3 — Responsive Product Listing
Complete HTML + CSS code

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.3 - Responsive Product Listing</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f1f5f9;
            color: #1e293b;
        }

        /* Header */
        header {
            background-color: #1e293b;
            color: white;
            text-align: center;
            padding: 25px 15px;
        }

        header h1 {
            margin-bottom: 10px;
        }

        /* Main Section */
        .product-section {
            max-width: 1200px;
            margin: auto;
            padding: 40px 20px;
        }

        .product-section h2 {
            text-align: center;
            margin-bottom: 30px;
            font-size: 30px;
        }

        /* Flexbox Product Container */
        .product-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: stretch;
            gap: 25px;
        }

        /* Product Card */
        .product-card {
            background-color: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);

            /* Flexbox sizing properties */
            flex-grow: 1;
            flex-shrink: 1;
            flex-basis: 250px;

            max-width: 350px;
            display: flex;
            flex-direction: column;
            transition: transform 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        /* Product Image */
        .product-card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            display: block;
        }

        /* Product Details */
        .product-info {
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            gap: 12px;
            flex-grow: 1;
        }

        .product-info h3 {
            font-size: 20px;
        }

        .price {
            color: #2563eb;
            font-size: 22px;
            font-weight: bold;
        }

        .description {
            color: #64748b;
            font-size: 14px;
            line-height: 1.5;
        }

        /* Product Button */
        .product-info button {
            width: 100%;
            margin-top: auto;
            padding: 12px;
            border: none;
            border-radius: 6px;
            background-color: #2563eb;
            color: white;
            font-size: 16px;
            cursor: pointer;
        }

        .product-info button:hover {
            background-color: #1d4ed8;
        }

        /* Footer */
        footer {
            background-color: #1e293b;
            color: white;
            text-align: center;
            padding: 18px;
            margin-top: 20px;
        }

        /* Mobile Responsive Design */
        @media (max-width: 600px) {
            .product-section {
                padding: 25px 15px;
            }

            .product-section h2 {
                font-size: 24px;
            }

            .product-container {
                flex-direction: column;
                align-items: center;
                gap: 20px;
            }

            .product-card {
                flex: 1 1 auto;
                width: 100%;
                max-width: 400px;
            }

            .product-card img {
                height: 200px;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>My Online Store</h1>
        <p>Discover our latest products at great prices</p>
    </header>

    <main class="product-section">
        <h2>Our Products</h2>

        <div class="product-container">

            <!-- Product 1 -->
            <div class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=600&q=80"
                    alt="Wireless headphones"
                >
                <div class="product-info">
                    <h3>Wireless Headphones</h3>
                    <p class="description">Enjoy high-quality sound and comfortable listening.</p>
                    <p class="price">₹1,499</p>
                    <button onclick="addToCart('Wireless Headphones')">
                        Add to Cart
                    </button>
                </div>
            </div>

            <!-- Product 2 -->
            <div class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=600&q=80"
                    alt="Classic wristwatch"
                >
                <div class="product-info">
                    <h3>Classic Watch</h3>
                    <p class="description">A stylish watch for everyday use and special occasions.</p>
                    <p class="price">₹2,299</p>
                    <button onclick="addToCart('Classic Watch')">
                        Add to Cart
                    </button>
                </div>
            </div>

            <!-- Product 3 -->
            <div class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=600&q=80"
                    alt="Red sports shoes"
                >
                <div class="product-info">
                    <h3>Sports Shoes</h3>
                    <p class="description">Lightweight shoes designed for comfort and movement.</p>
                    <p class="price">₹1,899</p>
                    <button onclick="addToCart('Sports Shoes')">
                        Add to Cart
                    </button>
                </div>
            </div>

            <!-- Product 4 -->
            <div class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1503602642458-232111445657?auto=format&fit=crop&w=600&q=80"
                    alt="Modern chair"
                >
                <div class="product-info">
                    <h3>Modern Chair</h3>
                    <p class="description">A contemporary chair for your home or office.</p>
                    <p class="price">₹3,499</p>
                    <button onclick="addToCart('Modern Chair')">
                        Add to Cart
                    </button>
                </div>
            </div>

            <!-- Product 5 -->
            <div class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?auto=format&fit=crop&w=600&q=80"
                    alt="Vintage camera"
                >
                <div class="product-info">
                    <h3>Digital Camera</h3>
                    <p class="description">Capture your favorite memories in beautiful detail.</p>
                    <p class="price">₹5,999</p>
                    <button onclick="addToCart('Digital Camera')">
                        Add to Cart
                    </button>
                </div>
            </div>

            <!-- Product 6 -->
            <div class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1546868871-7041f2a55e12?auto=format&fit=crop&w=600&q=80"
                    alt="Smartwatch"
                >
                <div class="product-info">
                    <h3>Smart Watch</h3>
                    <p class="description">Track your activity and stay connected on the go.</p>
                    <p class="price">₹2,799</p>
                    <button onclick="addToCart('Smart Watch')">
                        Add to Cart
                    </button>
                </div>
            </div>

        </div>
    </main>

    <footer>
        <p>&copy; 2026 My Online Store | All Rights Reserved</p>
    </footer>

    <script>
        function addToCart(productName) {
            alert(productName + " added to cart!");
        }
    </script>

</body>
</html>
How the assignment requirements are fulfilled
Requirement

Code used

At least 6 product cards

Six .product-card elements

Product images

img with src and alt

Product name and price

h3 and .price

Button on each card

Add to Cart button

Flexbox container

display: flex;

Cards wrap to next line

flex-wrap: wrap;

Spacing between cards

gap: 25px;

Flex growth

flex-grow: 1;

Flex shrinking

flex-shrink: 1;

Base card width

flex-basis: 250px;

Mobile responsiveness

@media (max-width: 600px)

How Flexbox works in this project
flex-grow: 1 — allows cards to use available extra space.

flex-shrink: 1 — allows cards to shrink when the container becomes narrower.

flex-basis: 250px — sets the initial preferred width of each card.

flex-wrap: wrap — moves cards onto additional rows when they no longer fit.

gap: 25px — adds consistent spacing between cards.

justify-content: center — centers the cards in each row.

Expected output
Desktop view
Building a Modern E-commerce App with Next.js 15, Zustand, and TypeScript - DEV Community
On a desktop, the cards should appear in multiple columns, typically three per row at a suitable screen width.

Mobile view
Build a flutter ecommerce or cart app ui by Arbaazaj | Fiverr
On a mobile screen, the cards stack vertically and fill most of the available width.

How to take the required screenshots
Save the code as Assignment-7.3.html.

Open the file in Chrome or another browser.

For the desktop screenshot, maximize the browser window and capture the product listing.

For the mobile screenshot, press F12 in Chrome, select the device toolbar using Ctrl + Shift + M, and choose a device such as iPhone SE or a viewport around 375 pixels wide.

Capture the mobile view and save both screenshots for submission.

Submission checklist:


HTML file saved as Assignment-7.3.html

Six product cards with images, names, prices, and buttons

Flexbox properties demonstrated

Desktop screenshot saved

Mobile screenshot saved