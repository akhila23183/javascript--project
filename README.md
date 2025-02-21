<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        .calculator {
            width: 250px;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            text-align: center;
        }
        .screen {
            width: 100%;
            height: 50px;
            font-size: 1.5em;
            text-align: right;
            margin-bottom: 10px;
            padding: 5px;
        }
        .buttons button {
            width: 22%;
            height: 50px;
            margin: 5px;
            font-size: 1.2em;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" class="screen" id="screen" disabled>
        <div class="buttons">
            <button onclick="clearScreen()">C</button>
            <button onclick="appendValue('/')">/</button>
            <button onclick="appendValue('')"></button>
            <button onclick="appendValue('-')">-</button>
            <button onclick="appendValue('7')">7</button>
            <button onclick="appendValue('8')">8</button>
            <button onclick="appendValue('9')">9</button>
            <button onclick="appendValue('+')">+</button>
            <button onclick="appendValue('4')">4</button>
            <button onclick="appendValue('5')">5</button>
            <button onclick="appendValue('6')">6</button>
            <button onclick="calculate()">=</button>
            <button onclick="appendValue('1')">1</button>
            <button onclick="appendValue('2')">2</button>
            <button onclick="appendValue('3')">3</button>
            <button onclick="appendValue('0')">0</button>
        </div>
    </div><script>
    function appendValue(value) {
        document.getElementById('screen').value += value;
    }
    function clearScreen() {
        document.getElementById('screen').value = '';
    }
    function calculate() {
        try {
            document.getElementById('screen').value = eval(document.getElementById('screen').value);
        } catch {
            alert('Invalid Expression');
        }
    }
</script>

</body>
</html>
