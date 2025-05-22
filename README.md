<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Morph Chance - مورفلینگ</title>
  <style>
    body {
      background: #0b0f1a;
      color: #fff;
      font-family: 'Vazirmatn', sans-serif;
      text-align: center;
      padding: 2rem;
    }
    .container {
      max-width: 400px;
      margin: auto;
      background: #1b2233;
      border-radius: 20px;
      padding: 2rem;
      box-shadow: 0 0 20px rgba(0,255,255,0.2);
    }
    button {
      background-color: #00bcd4;
      color: #fff;
      font-size: 1.5rem;
      border: none;
      border-radius: 10px;
      padding: 1rem 2rem;
      cursor: pointer;
      margin-top: 1rem;
      transition: background 0.3s;
    }
    button:hover {
      background-color: #008ba3;
    }
    .result {
      margin-top: 2rem;
      font-size: 1.4rem;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Morph Chance</h1>
    <p>برای امتحان شانس خودت دکمه زیر رو بزن!</p>
    <button onclick="morphChance()">Morph Now</button>
    <div class="result" id="result"></div>
  </div>

  <script>
    function morphChance() {
      const percent = Math.floor(Math.random() * 71) + 30; // 30% to 100%
      const isBuff = Math.random() < 0.5;
      let resultText = درصد شما: ${percent}%;

      if (isBuff) {
        resultText += <br>شما <strong>${percent}% تخفیف</strong> گرفتید!;
      } else {
        const pay = 100 - percent;
        resultText += <br>پرداخت نهایی شما <strong>${pay}% از مبلغ اصلی</strong> است!;
      }

      document.getElementById('result').innerHTML = resultText;
    }
  </script>
</body>
</html
