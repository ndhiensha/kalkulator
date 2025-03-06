<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Kalkulator Sederhana</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            margin: 0;
        }
        .calculator {
            background-color: #333;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 300px;
        }
        .display {
            width: 100%;
            height: 60px;
            margin-bottom: 10px;
            text-align: right;
            font-size: 24px;
            padding: 10px;
            background-color: #fff;
            border: none;
            border-radius: 5px;
            box-sizing: border-box;
            overflow: auto;
        }
        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
        }
        .btn {
            padding: 15px;
            font-size: 18px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            transition: background-color 0.3s;
        }
        .btn:hover {
            background-color: #45a049;
        }
        .operator {
            background-color: #ff9800;
        }
        .operator:hover {
            background-color: #f57c00;
        }
        .clear {
            background-color: #f44336;
        }
        .clear:hover {
            background-color: #d32f2f;
        }
        .equal {
            background-color: #2196F3;
        }
        .equal:hover {
            background-color: #1976D2;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <div id="display" class="display"></div>
        <div class="buttons">
            <button class="button" onclick="addToDisplay('7')">7</button>
            <button class="button" onclick="addToDisplay('8')">8</button>
            <button class="button" onclick="addToDisplay('9')">9</button>
            <button class="button operator" onclick="addToDisplay('/')">÷</button>
            
            <button class="button" onclick="addToDisplay('4')">4</button>
            <button class="button" onclick="addToDisplay('5')">5</button>
            <button class="button" onclick="addToDisplay('6')">6</button>
            <button class="button operator" onclick="addToDisplay('*')">×</button>
            
            <button class="button" onclick="addToDisplay('1')">1</button>
            <button class="button" onclick="addToDisplay('2')">2</button>
            <button class="button" onclick="addToDisplay('3')">3</button>
            <button class="button operator" onclick="addToDisplay('-')">-</button>
            
            <button class="button" onclick="addToDisplay('0')">0</button>
            <button class="button" onclick="addToDisplay('.')">.</button>
            <button class="button equal" onclick="addToDisplay('=')">=</button>
            <button class="button operator" onclick="addToDisplay('+')">+</button>
            
            <button class="button clear" onclick="clearDisplay()">C</button>
        </div>
    </div>

    <script>
        function addToDisplay(value) {
            const display = document.getElementById('display');
            display.textContent += value;
        }

        function clearDisplay() {
            const display = document.getElementById('display');
            display.textContent = '';
        }

    </script>
</body>
</html>
