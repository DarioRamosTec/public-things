<!DOCTYPE html>
<html>
<head>
    <title>Calculadora</title>
    <style>
        .calculator {
            width: 300px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
            background-color: #f4f4f4;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled>
        <br>
        <button onclick="clearDisplay()">C</button>
        <button onclick="appendToDisplay('7')">7</button>
        <button onclick="appendToDisplay('8')">8</button>
        <button onclick="appendToDisplay('9')">9</button>
        <button onclick="appendToDisplay('+')">+</button>
        <br>
        <button onclick="appendToDisplay('4')">4</button>
        <button onclick="appendToDisplay('5')">5</button>
        <button onclick="appendToDisplay('6')">6</button>
        <button onclick="appendToDisplay('-')">-</button>
        <br>
        <button onclick="appendToDisplay('1')">1</button>
        <button onclick="appendToDisplay('2')">2</button>
        <button onclick="appendToDisplay('3')">3</button>
        <button onclick="appendToDisplay('*')">*</button>
        <br>
        <button onclick="appendToDisplay('0')">0</button>
        <button onclick="appendToDisplay('.')">.</button>
        <button onclick="calculateResult()">=</button>
        <button onclick="appendToDisplay('/')">/</button>
    </div>

    <script>
        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function appendToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function calculateResult() {
            try {
                const result = eval(document.getElementById('display').value);
                document.getElementById('display').value = result;
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }
    </script>
</body>
</html>
