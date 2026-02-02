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
      margin-bottom: 24px;
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

    img {
      max-width: 100%;
      border-radius: 12px;
      margin-top: 16px;
    }

    .hidden {
      display: none;
    }
  </style>
</head>
<body>

  <!-- QUESTION CARD -->
  <div class="card" id="question">
    <h1>Hey Renuka ❤️</h1>

    <p>
      I’ve been thinking about you.<br/>
      About us.<br/>
      And how everything feels warmer when you’re around.
    </p>

    <h1>Will you be my Valentine?</h1>

    <button class="yes" onclick="normalYes()">Yes 💖</button>
    <button class="hell" onclick="hellYes()">Hell Yeah Poo 😌</button>
  </div>

  <!-- NORMAL YES -->
  <div class="card hidden" id="yesCard">
    <h1>You made my day 🥹</h1>
    <p>
      I can’t wait to make memories with you.<br/>
      Happy Valentine’s, Renuka ❤️
    </p>
  </div>

  <!-- HELL YEAH GIF CELEBRATION -->
  <div class="card hidden" id="gifCard">
    <h1>LET’S GOOOO 🥳💖</h1>
    <p>
      That’s the energy I was waiting for.
    </p>

    <!-- Replace GIF link if you want -->
    <[img src="https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif" alt="Celebration GIF" /](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExaDh6dmphZzZrOXU4czBhc3Fub203eXlscWd0NXZ0dmNxY3ZnNXdiOCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/t3sZxY5zS5B0z5zMIz/giphy.gif)>

    <p>
      Happy Valentine’s, Renuka ❤️
    </p>
  </div>

  <script>
    function normalYes() {
      document.getElementById("question").classList.add("hidden");
      document.getElementById("yesCard").classList.remove("hidden");
    }

    function hellYes() {
      document.getElementById("question").classList.add("hidden");
      document.getElementById("gifCard").classList.remove("hidden");
    }
  </script>

</body>
</html>
