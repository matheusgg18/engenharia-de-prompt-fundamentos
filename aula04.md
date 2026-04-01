# ATIVIDADE AULA 4

<img width="795" height="802" alt="image" src="https://github.com/user-attachments/assets/bc3210d5-09f2-434d-a061-59eb1aabb022" />
<img width="688" height="800" alt="image" src="https://github.com/user-attachments/assets/99f3e218-cb65-4536-86fe-c55a606b8fd5" />
<img width="683" height="743" alt="image" src="https://github.com/user-attachments/assets/d6e18470-8abb-47bb-af47-da5b791f4c52" />

o codigo:
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Calculadora</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #f0f0f0;
    }
    .calculator {
      background: #222;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.3);
    }
    #display {
      width: 100%;
      height: 50px;
      font-size: 20px;
      margin-bottom: 10px;
      text-align: right;
      padding: 10px;
      border: none;
      border-radius: 5px;
    }
    .buttons {
      display: grid;
      grid-template-columns: repeat(4, 60px);
      gap: 10px;
    }
    button {
      height: 60px;
      font-size: 18px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .operator { background: orange; color: white; }
    .equal { background: green; color: white; grid-column: span 2; }
    .clear { background: red; color: white; }
  </style>
</head>
<body>
  <div class="calculator">
    <input type="text" id="display" disabled>
    <div class="buttons">
      <button onclick="clearDisplay()" class="clear">C</button>
      <button onclick="appendValue('/')" class="operator">/</button>
      <button onclick="appendValue('*')" class="operator">*</button>
      <button onclick="appendValue('-')" class="operator">-</button>
      <button onclick="appendValue('7')">7</button>
      <button onclick="appendValue('8')">8</button>
      <button onclick="appendValue('9')">9</button>
      <button onclick="appendValue('+')" class="operator">+</button>
      <button onclick="appendValue('4')">4</button>
      <button onclick="appendValue('5')">5</button>
      <button onclick="appendValue('6')">6</button>
      <button onclick="appendValue('.')">.</button>
      <button onclick="appendValue('1')">1</button>
      <button onclick="appendValue('2')">2</button>
      <button onclick="appendValue('3')">3</button>
      <button onclick="calculate()" class="equal">=</button>
      <button onclick="appendValue('0')">0</button>
    </div>
  </div>

  <script>
    function appendValue(value) {
      document.getElementById('display').value += value;
    }

    function clearDisplay() {
      document.getElementById('display').value = '';
    }

    function calculate() {
      try {
        const result = eval(document.getElementById('display').value);
        document.getElementById('display').value = result;
      } catch (e) {
        alert('Erro na conta');
      }
    }
  </script>
</body>
</html>

------------------------------------------------------------------------------------------------------------
<img width="793" height="797" alt="image" src="https://github.com/user-attachments/assets/052b0a82-7510-47dc-aca7-844604942b4f" />
<img width="696" height="798" alt="image" src="https://github.com/user-attachments/assets/0c81857a-33f6-4f46-bcb7-859294fd0aa8" />

o codigo:
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Calculadora Reativa</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #f5f5f5;
    }
    .container {
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
      text-align: center;
    }
    input {
      width: 80px;
      padding: 10px;
      margin: 10px;
      font-size: 18px;
      text-align: center;
    }
    .result {
      margin-top: 20px;
      font-size: 22px;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div class="container">
    <h2>Calculadora Automática</h2>
    <input type="number" id="num1" placeholder="0">
    +
    <input type="number" id="num2" placeholder="0">
    <div class="result">
      Resultado: <span id="resultado">0</span>
    </div>
  </div>
  <script>
    const num1 = document.getElementById('num1');
    const num2 = document.getElementById('num2');
    const resultado = document.getElementById('resultado');
    function atualizarResultado() {
      const valor1 = parseFloat(num1.value) || 0;
      const valor2 = parseFloat(num2.value) || 0;
      resultado.textContent = valor1 + valor2;
    }
    // Atualiza automaticamente ao digitar
    num1.addEventListener('input', atualizarResultado);
    num2.addEventListener('input', atualizarResultado);
  </script>

</body>
</html>
