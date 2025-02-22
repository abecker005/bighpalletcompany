<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Big H Pallet Company</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 20px 0;
            text-align: center;
        }
        .container {
            width: 80%;
            margin: auto;
            overflow: hidden;
        }
        form {
            background: #fff;
            padding: 20px;
            margin-top: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        label {
            display: block;
            margin: 10px 0 5px;
        }
        select, input[type="text"], input[type="submit"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        input[type="submit"] {
            background: #333;
            color: #fff;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background: #555;
        }
    </style>
    <script>
        function validateForm() {
            const quantity = document.getElementById('quantity').value;
            if (isNaN(quantity) || quantity <= 0) {
                alert('Please enter a valid number for quantity.');
                return false;
            }
            return true;
        }
    </script>
</head>
<body>
    <header>
        <h1>Big H Pallet Company</h1>
    </header>
    <div class="container">
        <form onsubmit="return validateForm()">
            <label for="transactionType">Are you looking to buy or sell pallets?</label>
            <select id="transactionType" name="transactionType" required>
                <option value="buy">Buy</option>
                <option value="sell">Sell</option>
            </select>

            <label for="quantity">How many pallets do you need per week?</label>
            <input type="text" id="quantity" name="quantity" required>

            <label for="size">What size of pallets do you need?</label>
            <select id="size" name="size" required>
                <option value="small">Small</option>
                <option value="medium">Medium</option>
                <option value="large">Large</option>
            </select>

            <input type="submit" value="Submit">
        </form>
    </div>
</body>
</html>
