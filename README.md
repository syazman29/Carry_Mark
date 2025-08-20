<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Carry Mark Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
    }
    .container {
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0px 4px 10px rgba(0,0,0,0.2);
      width: 300px;
    }
    h2 {
      text-align: center;
    }
    label {
      display: block;
      margin-top: 10px;
    }
    input {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    button {
      margin-top: 15px;
      width: 100%;
      padding: 10px;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background: #0056b3;
    }
    .result {
      margin-top: 15px;
      font-size: 18px;
      text-align: center;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Carry Mark Calculator</h2>
    <label>Test 1 (10%)</label>
    <input type="number" id="test1" placeholder="Masukkan markah">

    <label>Test 2 (10%)</label>
    <input type="number" id="test2" placeholder="Masukkan markah">

    <label>Assignment 1 (10%)</label>
    <input type="number" id="ass1" placeholder="Masukkan markah">

    <label>Assignment 2 (10%)</label>
    <input type="number" id="ass2" placeholder="Masukkan markah">

    <label>Final Exam (60%)</label>
    <input type="number" id="final" placeholder="Masukkan markah">

    <button onclick="calculate()">Kira Carry Mark</button>

    <div class="result" id="result"></div>
  </div>

  <script>
    function calculate() {
      let test1 = document.getElementById("test1").value || 0;
      let test2 = document.getElementById("test2").value || 0;
      let ass1 = document.getElementById("ass1").value || 0;
      let ass2 = document.getElementById("ass2").value || 0;
      let final = document.getElementById("final").value || 0;

      let total = (test1 * 0.1) + (test2 * 0.1) + (ass1 * 0.1) + (ass2 * 0.1) + (final * 0.6);

      document.getElementById("result").innerText = "Total Carry Mark: " + total.toFixed(2) + "%";
    }
  </script>
</body>
</html>
