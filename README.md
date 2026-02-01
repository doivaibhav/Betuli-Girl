<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>For Renuka ❤️</title>

  <style>
    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #ffdde1, #fff1f4);
      font-family: system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      text-align: center;
      color: #333;
    }

    .card {
      background: white;
      padding: 36px 28px;
      border-radius: 18px;
      max-width: 420px;
      box-shadow: 0 25px 50px rgba(0,0,0,0.12);
    }

    h1 {
      font-size: 28px;
      margin-bottom: 12px;
    }

    p {
      font-size: 16px;
      line-height: 1.6;
      margin-bottom: 26px;
    }

    button {
      font-size: 16px;
      padding: 12px 22px;
      border-radius: 999px;
      border: none;
      cursor: pointer;
      margin: 8px;
    }

    .yes {
      background: #ff4d6d;
      color: white;
    }

    .hell {
      background: #ffd166;
      color: #333;
      font-weight: 600;
    }

    .hidden {
      display: none;
    }
  </style>
</head>
<body>

  <div class="card" id="question">
    <h1>Hey Renuka ❤️</h1>

    <p>
      I’ve been thinking about you.<br/>
      About us.<br/>
      And how everything feels warmer when you’re around.
    </p>

    <h1>Will you be my Valentine?</h1>

    <button class="yes" onclick="accept()">Yes 💖</button>
    <button class="hell" onclick="accept()">Hell Yeah Poo 😌</button>
  </div>

  <div class="card hidden" id="answer">
    <h1>You made my day 🥹</h1>
    <p>
      I can’t wait to make memories with you.<br/>
      Thank you for being you.
    </p>
    <p>
      Happy Valentine’s, Renuka ❤️
    </p>
  </div>

  <script>
    function accept() {
      document.getElementById("question").classList.add("hidden");
      document.getElementById("answer").classList.remove("hidden");
      hearts();
    }

    function hearts() {
      for (let i = 0; i < 80; i++) {
        const span = document.createElement("span");
        span.innerHTML = "💗";
        span.style.position = "fixed";
        span.style.left = Math.random() * 100 + "vw";
        span.style.top = "-20px";
        span.style.fontSize = "20px";
        span.style.animation = "fall 2s linear";
        document.body.appendChild(span);
        setTimeout(() => span.remove(), 2000);
      }
    }
  </script>

  <style>
    @keyframes fall {
      to {
        transform: translateY(110vh);
        opacity: 0;
      }
    }
  </style>

</body>
</html>
