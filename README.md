<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calculator App</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #f4f4f4;
    }
    .calculator {
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    .display {
      width: 100%;
      height: 40px;
      text-align: right;
      margin-bottom: 10px;
      font-size: 24px;
      padding: 5px;
      border: 1px solid #ccc;
    }
    .buttons {
      display: grid;
      grid-template-columns: repeat(4, 60px);
      gap: 10px;
    }
    button {
      height: 50px;
      font-size: 18px;
      border: none;
      background-color: #eee;
      border-radius: 5px;
      cursor: pointer;
    }
    button.operator {
      background-color: #f9a825;
      color: #fff;
    }
    button.equals {
      background-color: #4caf50;
      color: #fff;
    }
    button.clear {
      background-color: #f44336;
      color: #fff;
    }
  </style>
</head>
<body>
  <div class="calculator">
    <input type="text" class="display" id="display" readonly>
    <div class="buttons">
      <button onclick="press('7')">7</button>
      <button onclick="press('8')">8</button>
      <button onclick="press('9')">9</button>
      <button class="operator" onclick="press('/')">/</button><button onclick="press('4')">4</button>
  <button onclick="press('5')">5</button>
  <button onclick="press('6')">6</button>
  <button class="operator" onclick="press('*')">*</button>

  <button onclick="press('1')">1</button>
  <button onclick="press('2')">2</button>
  <button onclick="press('3')">3</button>
  <button class="operator" onclick="press('-')">-</button>

  <button onclick="press('0')">0</button>
  <button onclick="press('.')">.</button>
  <button class="equals" onclick="calculate()">=</button>
  <button class="operator" onclick="press('+')">+</button>

  <button class="clear" onclick="clearDisplay()">C</button>
</div>

  </div>  <script>
    let display = document.getElementById('display');

    function press(value) {
      display.value += value;
    }

    function calculate() {
      try {
        display.value = eval(display.value);
      } catch {
        display.value = 'Error';
      }
    }

    function clearDisplay() {
      display.value = '';
    }
  </script></body>
</html>
