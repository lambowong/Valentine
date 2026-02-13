<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Will You Be My Valentine?</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #e6c7ff, #f7e9ff);
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      padding: env(safe-area-inset-top) env(safe-area-inset-right) env(safe-area-inset-bottom) env(safe-area-inset-left);
      color: #333;
      overflow: hidden;
    }

    .card {
      background: white;
      border-radius: 20px;
      padding: 40px 30px;
      max-width: 420px;
      width: 90%;
      text-align: center;
      box-shadow: 0 20px 40px rgba(0,0,0,0.15);
      animation: fadeIn 1.2s ease;
      position: relative;
      z-index: 1;
    }

    h1 {
      font-size: 2rem;
      margin-bottom: 10px;
      font-weight: normal;
    }

    .valentine-title {
      font-family: 'Great Vibes', cursive;
      font-size: 2.6rem;
      margin-top: 20px;
    }

    .orchids {
      font-size: 1.8rem;
      margin-bottom: 15px;
      animation: float 3s ease-in-out infinite;
    }

    p {
      font-size: 1.05rem;
      line-height: 1.5;
      margin-bottom: 30px;
    }

    .buttons {
      display: flex;
      gap: 15px;
      justify-content: center;
      flex-wrap: wrap;
    }

    button {
      padding: 12px 22px;
      font-size: 1rem;
      border-radius: 999px;
      border: none;
      cursor: pointer;
      transition: transform 0.15s ease, box-shadow 0.15s ease;
      touch-action: manipulation;
    }

    @media (hover: hover) {
      button:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 18px rgba(0,0,0,0.15);
      }
    }

    button:active {
      transform: scale(0.97);
    }

    .yes {
      background: #ff4d6d;
      color: white;
    }

    .maybe {
      background: #f1f1f1;
      color: #333;
    }

    .response {
      margin-top: 25px;
      font-size: 1.1rem;
      display: none;
      opacity: 0;
      transition: opacity 0.8s ease;
    }

    .response.show {
      display: block;
      opacity: 1;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(15px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-6px); }
      100% { transform: translateY(0); }
    }

    .firework, .heart {
      position: fixed;
      pointer-events: none;
      border-radius: 50%;
      animation: explode 1s ease-out forwards;
    }

    .firework {
      width: 6px;
      height: 6px;
    }

    .heart {
      width: 14px;
      height: 14px;
      background: red;
      clip-path: polygon(50% 0%, 61% 10%, 75% 25%, 75% 45%, 50% 70%, 25% 45%, 25% 25%, 39% 10%);
      animation: floatHeart 3s ease-out forwards;
    }

    @keyframes explode {
      from { transform: scale(0.2); opacity: 1; }
      to { transform: scale(1.8); opacity: 0; }
    }

    @keyframes floatHeart {
      0% { transform: translateY(0) scale(1); opacity: 1; }
      100% { transform: translateY(-200px) scale(1.2); opacity: 0; }
    }
  </style>
</head>
<body>
  <div class="card">
    <div class="orchids">🌸 🌸 🌸</div>
    <h1>Mansi</h1>
    <p>I know Valentine’s Day is just another day to you, but hopefully you will say yes to this :)</p>

    <h1 class="valentine-title">Will you be my Valentine?</h1>

    <div class="buttons">
      <button class="yes" onclick="sayYes()">Yes 🫶</button>
      <button class="maybe" onclick="sayMaybe()">Let’s talk about it</button>
    </div>

    <div class="response" id="response"></div>
  </div>

  <script>
    function sayYes() {
      const r = document.getElementById('response');
      r.classList.add('show');
      r.innerText = "I'm glad you said yes, I feel like the luckiest guy around.";
      launchFireworks();
      launchHearts();
    }

    function sayMaybe() {
      const r = document.getElementById('response');
      r.classList.add('show');
      r.innerText = ":(";
    }

    function launchFireworks() {
      for (let i = 0; i < 25; i++) {
        setTimeout(() => {
          const fw = document.createElement('div');
          fw.className = 'firework';
          fw.style.left = Math.random() * window.innerWidth + 'px';
          fw.style.top = Math.random() * window.innerHeight + 'px';
          fw.style.background = 'hsl(' + (Math.random() * 360) + ', 100%, 70%)';
          document.body.appendChild(fw);
          setTimeout(() => fw.remove(), 1000);
        }, i * 50);
      }
    }

    function launchHearts() {
      for (let i = 0; i < 15; i++) {
        setTimeout(() => {
          const heart = document.createElement('div');
          heart.className = 'heart';
          heart.style.left = Math.random() * window.innerWidth + 'px';
          heart.style.top = window.innerHeight + 'px';
          document.body.appendChild(heart);
          setTimeout(() => heart.remove(), 3000);
        }, i * 200);
      }
    }
  </script>
</body>
</html>
