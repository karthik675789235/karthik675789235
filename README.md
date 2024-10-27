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

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f8f9fa;
}

header {
    background-color: #343a40;
    color: white;
    padding: 10px 20px;
    text-align: center;
}

main {
    display: flex;
    justify-content: space-around;
    padding: 20px;
}

#menu, #cart {
    width: 45%;
    background: white;
    border-radius: 8px;
    padding: 20px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

.menu-item {
    margin-bottom: 15px;
}

button {
    padding: 10px 15px;
    border: none;
    border-radius: 5px;
    background-color: #007bff;
    color: white;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

let cart = [];

function addToCart(item) {
    cart.push(item);
    updateCartDisplay();
}

function updateCartDisplay() {
    const cartItemsElement = document.getElementById('cart-items');
    cartItemsElement.innerHTML = '';

    cart.forEach(item => {
        const li = document.createElement('li');
        li.textContent = item;
        cartItemsElement.appendChild(li);
    });
}

function checkout() {
    if (cart.length === 0) {
        alert('Your cart is empty!');
    } else {
        alert('Thank you for your order!');
        cart = [];
        updateCartDisplay();
    }
}
