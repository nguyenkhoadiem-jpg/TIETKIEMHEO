<html>
<head>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #93ff80;
        }

        h1 {
            color: #333;
        }
        .savings-image {
            width: 300px;
            height: 300px;
            margin-bottom: 20px;
        }

        .savings-form {
            margin: 20px auto;
            width: 400px;
        }

        .savings-input {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
        }

        .savings-button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
        }

        .savings-button:hover {
            background-color: #45a049;
        }

        .savings-result {
            margin: 20px auto;
            width: 400px;
            text-align: left;
            background-color: rgb(255, 183, 239);
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);

        }

        .savings-result {
            margin: 20px auto;
            width: 400px;
            text-align: left;
        }

        .savings-result span {
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>Ứng dụng tiết kiệm tiền CON HEO ĐẤT</h1>
        <label for="daily-allowance">Nhập số tiền trợ cấp hàng ngày (Ngàn VNĐ):</label>
        <input id="daily-allowance" class="savings-input" type="number">

        <button class="savings-button" onclick="calculateSavings()">Tính toán</button>
    </div>

    <div class="savings-result">
        <h2>Phân chia chi tiêu hàng ngày:</h2>
        <ul>
            <li>
                <span>Tiền sinh hoạt:</span>
                <span id="living-expense"></span>
            </li>
            <li>
                <span>Tiền ăn:</span>
                <span id="food-expense"></span>
            </li>
            <li>
                <span>Tiền đi lại:</span>
                <span id="transportation-expense"></span>
            </li>
            <li>
                <span>Tiền tiết kiệm:</span>
                <span id="savings-expense"></span>
            </li>
        </ul>

        <h2>Tổng tiền tiết kiệm:</h2>
        <ul>
            <li>
                <span>Sau 1 tháng:</span>
                <span id="savings-1-month"></span>
            </li>
            <li>
                <span>Sau 2 tháng:</span>
                <span id="savings-2-months"></span>
            </li>
        </ul>
    </div>

    <script>
        function calculateSavings() {
            var dailyAllowance = parseFloat(document.getElementById("daily-allowance").value);
            var livingExpense = dailyAllowance * 0.3;
            var foodExpense = dailyAllowance * 0.4;
            var transportationExpense = dailyAllowance * 0.2;
            var savingsExpense = dailyAllowance * 0.1;

            document.getElementById("living-expense").textContent = livingExpense + " VNĐ";
            document.getElementById("food-expense").textContent = foodExpense + " Ngàn VNĐ";
            document.getElementById("transportation-expense").textContent = transportationExpense + " VNĐ";
            document.getElementById("savings-expense").textContent = savingsExpense + " VNĐ";

            var totalSavings1Month = savingsExpense * 30;
            var totalSavings2Months = savingsExpense * 60;

            document.getElementById("savings-1-month").textContent = totalSavings1Month + " VNĐ";
            document.getElementById("savings-2-months").textContent = totalSavings2Months + " VNĐ";
        }
    </script>
</body>
</html>
