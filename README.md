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

  <!-- AUDIO -->
  <audio id="loveSong" preload="auto">
    <source src="make-you-mine.mp3" type="audio/mpeg">
  </audio>

  <!-- QUESTION -->
  <div class="card" id="question">
    <h1>Hey Renuka ❤️</h1>

    <p>
      I’ve been thinking about you.<br/>
      About us.<br/>
      And how everything feels warmer when you’re around.
    </p>

    <h1>Will you be my Valentine?</h1>

    <button class="yes" onclick="normalYes()">Yes 💖</button>
    <button class="hell runaway" id="runawayBtn" onclick="hellYes()">Ohh Hell Yeah Poo 😌</button>
  </div>

  <!-- YES SCREEN -->
  <div class="card hidden" id="yesCard">
    <h1>You made my day 🥹</h1>
    <p>
      I can’t wait to make memories with you.<br/>
      Happy Valentine’s, Renuka ❤️
    </p>
  </div>

  <!-- HELL YEAH SCREEN -->
  <div class="card hidden" id="gifCard">
    <h1>LET’S GOOOO 🥳💖</h1>
    <p>Worth the effort 😌</p>

    <img src="celebrate.gif" alt="Celebration GIF" />

    <p>Happy Valentine’s, Renuka ❤️</p>
  </div>

  <script>
    let escapeCount = 0;
    const maxEscapes = 6;

    function normalYes() {
      document.getElementById("question").classList.add("hidden");
      document.getElementById("yesCard").classList.remove("hidden");
    }

    function hellYes() {
      // Only clickable after 6 escapes
      if (escapeCount < maxEscapes) return;

      document.getElementById("question").classList.add("hidden");
      document.getElementById("gifCard").classList.remove("hidden");

      const song = document.getElementById("loveSong");

      song.onloadedmetadata = () => {
        song.currentTime = 47;
        song.play();
      };

      if (song.readyState >= 1) {
        song.currentTime = 47;
        song.play();
      }
    }

    const btn = document.getElementById("runawayBtn");

    document.addEventListener("mousemove", (e) => {
      if (!btn || escapeCount >= maxEscapes) return;

      const rect = btn.getBoundingClientRect();
      const btnX = rect.left + rect.width / 2;
      const btnY = rect.top + rect.height / 2;

      const distance = Math.hypot(e.clientX - btnX, e.clientY - btnY);

      if (distance < 160) {
        escapeCount++;

        const moveX = (Math.random() - 0.5) * window.innerWidth * 0.8;
        const moveY = (Math.random() - 0.5) * window.innerHeight * 0.6;

        btn.style.transform = `translate(${moveX}px, ${moveY}px)`;

        // After final escape, stop running
        if (escapeCount === maxEscapes) {
          btn.classList.remove("runaway");
          btn.style.transform = "translate(0, 0)";
        }
      }
    });
  </script>

</body>
</html>
