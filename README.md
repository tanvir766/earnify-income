<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Earnify | Home</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: #f4f9ff;
    }

    header {
      background: #fff;
      padding: 15px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
    }

    .logo {
      font-size: 22px;
      font-weight: bold;
      color: #2c3e50;
    }

    .balance {
      font-size: 16px;
      font-weight: bold;
      color: #34495e;
    }

    .section-title {
      padding: 20px 20px 10px;
      font-size: 18px;
      font-weight: bold;
      color: #2d3436;
    }

    .card-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 12px;
      padding: 0 20px;
    }

    .card {
      background: #26c6da;
      color: #fff;
      text-align: center;
      padding: 20px 10px;
      border-radius: 12px;
      font-size: 18px;
      font-weight: bold;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      animation: fadeIn 0.4s ease forwards;
      opacity: 0;
    }

    .card .title {
      font-size: 16px;
      display: block;
      margin-bottom: 6px;
      font-weight: 500;
    }

    .card .value {
      font-size: 24px;
      font-weight: bold;
    }

    .card:nth-child(1) { animation-delay: 0.1s; }
    .card:nth-child(2) { animation-delay: 0.2s; }
    .card:nth-child(3) { animation-delay: 0.3s; }
    .card:nth-child(4) { animation-delay: 0.4s; }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .work-section {
      padding: 10px 20px 30px;
    }

    .task {
      background: #03a9f4;
      color: white;
      border-radius: 10px;
      padding: 15px;
      margin-bottom: 12px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-weight: bold;
      font-size: 16px;
      transition: 0.3s;
    }

    .task:hover {
      background: #0288d1;
    }

    .task a {
      background: white;
      color: #03a9f4;
      border: none;
      border-radius: 25px;
      padding: 6px 14px;
      font-weight: bold;
      text-decoration: none;
    }

    .task a:hover {
      background: #e0f7fa;
    }

    footer {
      background: #1a1a1a;
      color: #fff;
      padding: 12px;
      text-align: center;
      font-size: 13px;
    }

    footer a {
      color: #00e5ff;
      text-decoration: none;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="logo">EARNIFY</div>
    <div class="balance" id="balance-amount">BDT: 00TK</div>
  </header>

  <!-- Earnings -->
  <div class="section-title">Dashboard</div>
  <div class="card-grid">
    <div class="card">
      <span class="title" id="sell-title">Sell</span>
      <span class="value" id="sell-value">00</span>
    </div>
    <div class="card">
      <span class="title" id="income-title">Income</span>
      <span class="value" id="income-value">00</span>
    </div>
    <div class="card">
      <span class="title" id="user-title">Pending Work</span>
      <span class="value" id="user-value">00</span>
    </div>
    <div class="card">
      <span class="title" id="total-title">Total Income</span>
      <span class="value" id="total-value">05TK</span>
    </div>
  </div>

  <!-- Work Section -->
  <div class="section-title">Available work</div>
  <div class="work-section">
    <div class="task">
      Gmail Sell 7 TK
      <a href="https://example.com/task1" target="_blank">View</a>
    </div>
    <div class="task">
      Gmail Sell 10 TK
      <a href="https://example.com/task2" target="_blank">View</a>
    </div>
    <div class="task">
      Maicro Task
      <a href="https://example.com/task3" target="_blank">View</a>
    </div>
    <div class="task">
      Processing...
      <a href="https://example.com/task4" target="_blank">View</a>
    </div>
  </div>

  <!-- Footer -->
  <footer>
    Terms & <a href="#">Support</a> | Designed with ❤️ by Earnify
  </footer>

  <!-- Optional Script to dynamically change data -->
  <script>
    // Example: Changing values dynamically
    document.getElementById("sell-title").innerText = "New Sell";
    document.getElementById("sell-value").innerText = "00";

    document.getElementById("income-title").innerText = "Today Income";
    document.getElementById("income-value").innerText = "00TK";

    document.getElementById("total-title").innerText = "Total Earned";
    document.getElementById("total-value").innerText = "00TK";

    document.getElementById("balance-amount").innerText = "BDT: 00TK";
  </script>

</body>
</html>
