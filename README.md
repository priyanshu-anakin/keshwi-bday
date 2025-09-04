<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday 🎂</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: white;
      font-family: 'Arial', sans-serif;
      overflow: hidden;
    }
    .cake {
      position: relative;
      width: 200px;
      height: 200px;
      background: #ff6f61;
      border-radius: 10px;
      box-shadow: 0 0 40px rgba(255, 255, 255, 0.3);
    }
    .cake::before {
      content: '';
      position: absolute;
      width: 100%;
      height: 40px;
      background: #f8c291;
      top: -40px;
      left: 0;
      border-radius: 10px 10px 0 0;
    }
    .candle {
      position: absolute;
      top: -60px;
      left: 50%;
      width: 10px;
      height: 40px;
      background: white;
      transform: translateX(-50%);
      cursor: pointer;
    }
    .flame {
      position: absolute;
      top: -20px;
      left: 50%;
      width: 20px;
      height: 20px;
      background: radial-gradient(circle, yellow 40%, transparent 70%);
      border-radius: 50%;
      transform: translateX(-50%);
      animation: flicker 0.2s infinite;
    }
    @keyframes flicker {
      0% { transform: translateX(-50%) scale(1); opacity: 1; }
      50% { transform: translateX(-50%) scale(1.2); opacity: 0.8; }
      100% { transform: translateX(-50%) scale(1); opacity: 1; }
    }
    h1 {
      margin-top: 40px;
      font-size: 26px;
      text-align: center;
      animation: fadeIn 2s ease-in-out forwards;
      opacity: 0;
    }
    @keyframes fadeIn {
      to { opacity: 1; transform: translateY(20px); }
    }
  </style>
</head>
<body>
  <div class="cake">
    <div class="candle" onclick="blowCandle()">
      <div class="flame" id="flame"></div>
    </div>
  </div>
  <h1 id="wish">🎂 Happiest Birthday Keshwi 🎉<br>You are my fav ❤️</h1>

  <script>
    function blowCandle() {
      const flame = document.getElementById("flame");
      flame.style.display = "none"; // flame disappears
      const wish = document.getElementById("wish");
      wish.innerHTML = "💨 You blew the candle! 🎉<br>Happiest Birthday Keshwi ❤️ You are my fav 🚀";
    }
  </script>
</body>
</html>
