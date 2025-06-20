<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Earnify | Income Panel</title>
  <script src="https://telegram.org/js/telegram-web-app.js"></script>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #f0f8ff, #e1f5fe);
      text-align: center;
      padding-top: 100px;
      color: #333;
    }
    h2 {
      margin-bottom: 10px;
    }
    .card {
      background: white;
      margin: auto;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 10px 20px rgba(0,0,0,0.1);
      max-width: 400px;
    }
    .income {
      font-size: 28px;
      font-weight: bold;
      color: green;
    }
    button {
      background: #0088cc;
      color: white;
      border: none;
      padding: 12px 24px;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 20px;
    }
    button:hover {
      background: #006699;
    }
  </style>
</head>
<body>
  <div class="card">
    <h2>👤 ইউজার: <span id="username">লোড হচ্ছে...</span></h2>
    <p>💰 আপনার ইনকাম:</p>
    <div class="income" id="income">৳0</div>
    <button onclick="withdraw()">🔁 উইথড্র করুন</button>
  </div>

  <script>
    const tg = window.Telegram.WebApp;
    tg.expand();

    const user = tg.initDataUnsafe.user;
    document.getElementById('username').textContent = user?.first_name || 'Unknown';

    const incomeAmount = Math.floor(Math.random() * 100 + 50);
    document.getElementById('income').textContent = "৳" + incomeAmount;

    function withdraw() {
      tg.sendData("Withdraw requested for ৳" + incomeAmount);
      tg.close();
    }
  </script>
</body>
</html>
