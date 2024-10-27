<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Food Delivery</title>
</head>
<body>
    <header>
        <h1>Food Delivery Service</h1>
    </header>
    <main>
        <section id="menu">
            <h2>Menu</h2>
            <div class="menu-item">
                <h3>Pizza</h3>
                <p>Delicious cheese and tomato pizza</p>
                <button onclick="addToCart('Pizza')">Add to Cart</button>
            </div>
            <div class="menu-item">
                <h3>Burger</h3>
                <p>Juicy beef burger with lettuce and tomato</p>
                <button onclick="addToCart('Burger')">Add to Cart</button>
            </div>
            <div class="menu-item">
                <h3>Pasta</h3>
                <p>Classic spaghetti with marinara sauce</p>
                <button onclick="addToCart('Pasta')">Add to Cart</button>
            </div>
        </section>
        <section id="cart">
            <h2>Your Cart</h2>
            <ul id="cart-items"></ul>
            <button onclick="checkout()">Checkout</button>
        </section>
    </main>
    <script src="script.js"></script>
</body>
</html>
