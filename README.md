<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <title>Meraz Hossain | বোনাস ক্যালকুলেটর</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #e9ecef;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #007BFF;
      padding: 20px;
      text-align: center;
      color: white;
    }
    .calculator-container {
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 80vh;
    }
    .calculator {
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
      width: 320px;
    }
    .calculator h2 {
      color: #007BFF;
      text-align: center;
      margin-bottom: 20px;
    }
    label {
      display: block;
      margin: 15px 0 5px;
      font-weight: bold;
      color: #333;
    }
    input {
      width: 100%;
      padding: 10px;
      margin-bottom: 5px;
      border: 1px solid #ccc;
      border-radius: 5px;
      box-sizing: border-box;
    }
    button {
      background: #007BFF;
      color: white;
      border: none;
      padding: 10px;
      width: 100%;
      cursor: pointer;
      font-size: 16px;
      margin-top: 10px;
      border-radius: 5px;
    }
    button:hover {
      background: #0056b3;
    }
    .result {
      margin-top: 15px;
      font-weight: bold;
      color: green;
      white-space: pre-line;
    }
    footer {
      text-align: center;
      padding: 15px;
      font-size: 14px;
      color: #666;
    }
  </style>
</head>
<body>

<header>
  <h1>Meraz Hossain</h1>
  <p>বোনাস ক্যালকুলেশন ওয়েব টুল</p>
</header>

<div class="calculator-container">
  <div class="calculator">
    <h2>বোনাস ক্যালকুলেটর</h2>

    <label>ডিপোজিট এমাউন্ট:</label>
    <input type="number" id="deposit" placeholder="যেমনঃ 1000">

    <label>পার্সেন্টেজ (%):</label>
    <input type="number" id="percent" placeholder="যেমনঃ 10">

    <label>টার্নওভার:</label>
    <input type="number" id="turnover" placeholder="যেমনঃ 5">

    <button onclick="calculateBonus()">হিসাব করুন</button>

    <div class="result" id="result"></div>
  </div>
</div>

<footer>
  &copy; 2025 Meraz Hossain | সকল স্বত্ব সংরক্ষিত
</footer>

<script>
  function calculateBonus() {
    const deposit = parseFloat(document.getElementById('deposit').value);
    const percent = parseFloat(document.getElementById('percent').value);
    const turnover = parseFloat(document.getElementById('turnover').value);

    if (isNaN(deposit) || isNaN(percent) || isNaN(turnover)) {
      document.getElementById('result').innerText = "সঠিক মান প্রদান করুন।";
      return;
    }

    const bonus = (deposit * percent) / 100;
    const totalTurnover = bonus * turnover;

    document.getElementById('result').innerText =
      `🎁 বোনাস: ${bonus.toFixed(2)} টাকা\n🔁 টার্নওভার প্রয়োজন: ${totalTurnover.toFixed(2)} টাকা`;
  }
</script>

</body>
</html>
