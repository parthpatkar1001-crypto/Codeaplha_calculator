<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced Calculator</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
        }

        .calculator {
            background: #000;
            padding: 25px;
            border-radius: 25px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
            width: 370px;
        }

        .history {
            color: #8a8a8a;
            text-align: right;
            height: 25px;
            font-size: 16px;
            margin-bottom: 8px;
            overflow: hidden;
            white-space: nowrap;
        }

        #display {
            width: 100%;
            height: 85px;
            font-size: 48px;
            font-weight: 300;
            text-align: right;
            margin-bottom: 20px;
            border: none;
            background: #000;
            color: white;
            padding: 0 10px;
        }

        .buttons {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 12px;
        }

        button {
            height: 65px;
            font-size: 22px;
            font-weight: 400;
            border: none;
            border-radius: 50%;
            cursor: pointer;
            background: #333333;
            color: white;
            transition: all 0.2s;
        }

        button:active {
            transform: scale(0.95);
            opacity: 0.7;
        }

        button:hover {
            filter: brightness(1.2);
        }

        .operator {
            background: #ff9500;
            font-size: 28px;
        }

        .func {
            background: #a5a5a5;
            color: black;
            font-size: 20px;
        }

        .zero {
            grid-column: span 2;
            border-radius: 32px;
            text-align: left;
            padding-left: 25px;
        }

        .equals {
            grid-column: span 2;
            border-radius: 32px;
        }
    </style>
</head>

<body>
    <div class="calculator">
        <div class="history" id="history"></div>
        <input type="text" id="display" disabled placeholder="0">

        <div class="buttons">
            <!-- Row 1 -->
            <button class="func" onclick="clearAll()">AC</button>
            <button class="func" onclick="toggleSign()">+/-</button>
            <button class="func" onclick="append('(')">(</button>
            <button class="func" onclick="append(')')">)</button>
            <button class="operator" onclick="append('/')">÷</button>

            <!-- Row 2 -->
            <button onclick="append('7')">7</button>
            <button onclick="append('8')">8</button>
            <button onclick="append('9')">9</button>
            <button class="func" onclick="squareRoot()">√</button>
            <button class="operator" onclick="append('*')">×</button>

            <!-- Row 3 -->
            <button onclick="append('4')">4</button>
            <button onclick="append('5')">5</button>
            <button onclick="append('6')">6</button>
            <button class="func" onclick="square()">x²</button>
            <button class="operator" onclick="append('-')">−</button>

            <!-- Row 4 -->
            <button onclick="append('1')">1</button>
            <button onclick="append('2')">2</button>
            <button onclick="append('3')">3</button>
            <button class="func" onclick="percentage()">%</button>
            <button class="operator" onclick="append('+')">+</button>

            <!-- Row 5 -->
            <button class="func" onclick="showHistory()">H</button>
            <button class="zero" onclick="append('0')">0</button>
            <button onclick="append('.')">.</button>
            <button class="func" onclick="deleteLast()">⌫</button>
            <button class="operator equals" onclick="calculate()">=</button>
        </div>
    </div>

    <script>
        const display = document.getElementById('display');
        const historyDiv = document.getElementById('history');
        let calcHistory = [];
        let lastResult = null;

        function append(value) {
            if (display.value === 'Error' || display.value === '0') display.value = '';
            display.value += value;
        }

        function clearAll() {
            display.value = '';
            historyDiv.innerText = '';
            lastResult = null;
        }

        function deleteLast() {
            display.value = display.value.slice(0, -1);
        }

        function toggleSign() {
            try {
                if (display.value) {
                    display.value = eval(display.value) * -1;
                }
            } catch {
                display.value = 'Error';
            }
        }

        function percentage() {
            try {
                if (display.value) {
                    display.value = eval(display.value) / 100;
                }
            } catch {
                display.value = 'Error';
            }
        }

        function squareRoot() {
            try {
                if (display.value) {
                    let num = eval(display.value);
                    if (num < 0) throw new Error('Negative root');
                    historyDiv.innerText = `√(${display.value})`;
                    display.value = Math.sqrt(num);
                }
            } catch {
                display.value = 'Error';
            }
        }

        function square() {
            try {
                if (display.value) {
                    let num = eval(display.value);
                    historyDiv.innerText = `(${display.value})²`;
                    display.value = Math.pow(num, 2);
                }
            } catch {
                display.value = 'Error';
            }
        }

        function calculate() {
            try {
                if (!display.value) return;
                let expression = display.value;
                let result = eval(expression);

                // Handle Infinity and NaN
                if (!isFinite(result)) {
                    display.value = 'Error';
                    return;
                }

                // Round to avoid floating point issues like 0.1+0.2
                result = Math.round(result * 1000000000) / 1000000000;

                historyDiv.innerText = expression + ' =';
                calcHistory.push(expression + ' = ' + result);
                if (calcHistory.length > 10) calcHistory.shift(); // Keep last 10

                display.value = result;
                lastResult = result;
            } catch {
                display.value = 'Error';
            }
        }

        function showHistory() {
            if (calcHistory.length === 0) {
                alert('No calculations yet');
            } else {
                alert('Calculation History:\n\n' + calcHistory.slice(-5).join('\n'));
            }
        }

        // Keyboard support
        document.addEventListener('keydown', (event) => {
            const key = event.key;
            if (key >= '0' && key <= '9' || key === '.') append(key);
            else if (key === '+' || key === '-' || key === '*' || key === '/') append(key);
            else if (key === '(' || key === ')') append(key);
            else if (key === 'Enter' || key === '=') calculate();
            else if (key === 'Backspace') deleteLast();
            else if (key === 'Escape') clearAll();
            else if (key === '%') percentage();
        });
    </script>
</body>

</html>
