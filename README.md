# binary-to-decimal-converter
<!DOCTYPE html>
<html>
<head>
  <title>Decimal and Binary Converter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
    
    
      background-repeat: repeat;
    }
    
    h1 {
      text-align: center;
    }
    
    .container {
      max-width: 400px;
      margin: 0 auto;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
      background-color: rgba(255, 255, 255, 0.8);
    }
    
    label {
      display: block;
      margin-bottom: 10px;
      font-weight: bold;
    }
    
    input {
      width: 100%;
      padding: 8px;
      margin-bottom: 10px;
      box-sizing: border-box;
    }
    
    button {
      display: block;
      width: 100%;
      padding: 10px;
      background-color: #4CAF50;
      color: #fff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    
    .result {
      margin-top: 20px;
      padding: 10px;
      background-color: #fff;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Decimal and Binary Converter</h1>
    <div>
      <label for="decimal">Decimal:</label>
      <input type="number" id="decimal" placeholder="Enter decimal number">
    </div>
    <div>
      <label for="binary">Binary:</label>
      <input type="text" id="binary" placeholder="Enter binary number">
    </div>
    <div>
      <button onclick="convertToBinary()">Convert to Binary</button>
      <button onclick="convertToDecimal()">Convert to Decimal</button>
    </div>
    <div class="result" id="result"></div>
  </div>

  <script>
    function convertToBinary() {
      var decimalInput = document.getElementById('decimal');
      var binaryInput = document.getElementById('binary');
      var resultDiv = document.getElementById('result');

      var decimal = parseInt(decimalInput.value);

      if (!isNaN(decimal)) {
        binaryInput.value = decimal.toString(2);
        resultDiv.textContent = '';
      } else {
        resultDiv.textContent = 'Please enter a valid decimal number.';
      }
    }

    function convertToDecimal() {
      var decimalInput = document.getElementById('decimal');
      var binaryInput = document.getElementById('binary');
      var resultDiv = document.getElementById('result');

      var binary = binaryInput.value;

      if (/^[01]+$/.test(binary)) {
        decimalInput.value = parseInt(binary, 2);
        resultDiv.textContent = '';
      } else {
        resultDiv.textContent = 'Please enter a valid binary number.';
      }
    }
  </script>
</body>
</html>
