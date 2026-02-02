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
      overflow: hidden;
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
      position: relative;
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

    .runaway {
      transition: transform 0.12s ease;
    }

    .hidden {
      display: none;
    }

    img {
      max-width: 100%;
      border-radius: 12px;
      margin-top: 16px;
    }
  </style>
</head>
<body>

  <!-- AUDIO -->
  <audio id="loveSong" preload="auto">
    <source src="make-you-mine.mp3" type="audio/mpeg">
  </audio>

  <!-- QUESTION -->
  <div class="card" id="question">
    <h1>Priya Renuka Ji ❤️</h1>

    <p>
      I’ve been thinking about your beautiful eyes all the time.<br/>
      And how everything feels warmer when you’re around.
    </p>

    <h1>Will you be my Valentine forever?</h1>

    <button class="yes" onclick="normalYes()">Yes 💖</button>
    <button class="hell runaway" id="runawayBtn" onclick="hellYes()">
      Ohh Hell Yeah Poo 😌
    </button>
  </div>

  <!-- YES SCREEN -->
  <div class="card hidden" id="yesCard">
    <h1>You made my day 🥹</h1>
    <p>Happy Valentine’s, Renuka ❤️</p>
  </div>

  <!-- HELL YEAH SCREEN -->
  <div class="card hidden" id="gifCard">
    <h1>Dayum GIRLLL 🥳💖</h1>
    <img src="celebrate.gif" alt="Celebration GIF" />
    <p>Happy Valentine’s, Renuka Ji ❤️</p>
  </div>

  <script>
    const btn = document.getElementById("runawayBtn");
    const unlockTime = Date.now() + 30000; // 30 seconds from load
    let unlocked = false;

    setTimeout(() => {
      unlocked = true;
      btn.classList.remove("runaway");
