<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QFki Store | متجر ألعاب وحسابات</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal&display=swap" rel="stylesheet">
    <style>
        /* تنسيقات عامة */
        body {
            font-family: 'Tajawal', sans-serif;
            background: #F5F5F5;
            margin: 0;
        }

        /* الشريط العلوي */
        .navbar {
            background: #8A2BE2;
            padding: 1rem;
            position: sticky;
            top: 0;
            text-align: center;
        }

        .navbar a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
        }

        /* الهيدر */
        .header {
            background: linear-gradient(to right, #8A2BE2, #4B0082);
            color: white;
            text-align: center;
            padding: 4rem;
        }

        /* بطاقات المنتجات */
        .product-card {
            background: white;
            border-radius: 10px;
            padding: 1rem;
            margin: 1rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-card img {
            width: 100%;
            border-radius: 8px;
        }

        .price {
            color: #4B0082;
            font-weight: bold;
        }

        .btn {
            background: #FFD700;
            color: #4B0082;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        /* سلة التسوق */
        .cart-icon {
            position: fixed;
            left: 20px;
            top: 20px;
            background: #FFD700;
            padding: 10px 15px;
            border-radius: 25px;
            cursor: pointer;
            z-index: 1000;
        }

        /* جدول الحسابات */
        .accounts-section {
            margin: 2rem;
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th, td {
            padding: 12px;
            border: 1px solid #ddd;
            text-align: center;
        }

        /* الفوتر */
        footer {
            background: #4B0082;
            color: white;
            padding: 2rem;
            margin-top: 3rem;
            text-align: center;
        }

        /* تصميم الجوال */
        @media (max-width: 768px) {
            .navbar a { margin: 0 8px; font-size: 14px; }
            .header { padding: 2rem; }
            .product-card { margin: 1rem 0; }
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <a href="#home">الرئيسية</a>
        <a href="#products">المنتجات</a>
        <a href="#accounts">الحسابات</a>
    </nav>

    <div class="cart-icon">🛒 <span id="cart-count">0</span></div>

    <div class="header">
        <h1>مرحبًا في QFki Store! 🎮</h1>
        <p>أفضل الألعاب والحسابات بأرخص الأسعار</p>
    </div>

    <div class="product-card">
        <img src="https://via.placeholder.com/300x200" alt="لعبة">
        <h3>لعبة FIFA 24</h3>
        <p class="price">$49.99</p>
        <button class="btn">إضافة إلى السلة</button>
    </div>

    <div class="accounts-section">
        <h2>الحسابات المتاحة</h2>
        <table>
            <tr>
                <th>اللعبة</th>
                <th>المستوى</th>
                <th>السعر</th>
                <th>الشراء</th>
            </tr>
            <tr>
                <td>Fortnite</td>
                <td>100</td>
                <td>$20</td>
                <td><button class="btn">شراء الآن</button></td>
            </tr>
        </table>
    </div>

    <footer>
        <div class="contact-info">
            <h3>تواصل معنا</h3>
            <p>Email: contact@qfkistore.com</p>
            <p>Phone: +966 123 456 789</p>
        </div>
    </footer>

    <script>
        // سلة التسوق
        let cartItems = [];
        document.querySelectorAll('.btn').forEach(button => {
            button.addEventListener('click', () => {
                cartItems.push(button.parentElement.querySelector('h3').innerText);
                document.getElementById('cart-count').textContent = cartItems.length;
                alert("تمت الإضافة إلى السلة!");
            });
        });
    </script>
</body>
</html>
