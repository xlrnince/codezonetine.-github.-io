<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Girlfriend?</title>

  <style>
    body {
      font-family: 'Arial', sans-serif;
      text-align: center;
      background: linear-gradient(135deg, #ffb6c1, #ffe4ec);
      height: 100vh;
      overflow: hidden;
      margin: 0;
    }

    h1 {
      margin-top: 80px;
      font-size: 40px;
      color: #ff2e63;
      text-shadow: 2px 2px white;
    }

    .btn {
      padding: 15px 30px;
      font-size: 20px;
      margin: 10px;
      border: none;
      border-radius: 15px;
      cursor: pointer;
      transition: 0.3s;
      position: relative;
    }

    #yes {
      background: #ff4d6d;
      color: white;
      font-weight: bold;
      box-shadow: 0 0 10px #ff4d6d;
    }

    #no {
      background: gray;
      color: white;
      position: absolute;
    }

    /* floating stickers */
    .heart {
      position: absolute;
      font-size: 25px;
      animation: floatUp 5s linear infinite;
      opacity: 0.7;
    }

    @keyframes floatUp {
      0% { transform: translateY(100vh) scale(1); opacity: 0; }
      50% { opacity: 1; }
      100% { transform: translateY(-10vh) scale(1.5); opacity: 0; }
    }
  </style>
</head>

<body>

  <h1>Will you be my girlfriend? 💖</h1>

  <button id="yes" class="btn">Yes 💕</button>
  <button id="no" class="btn">No 😢</button>

  <script>
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");

    // move NO button when clicked
    noBtn.addEventListener("click", () => {
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 100);

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";

      // make YES bigger each time NO is clicked
      let currentSize = parseFloat(window.getComputedStyle(yesBtn).fontSize);
      yesBtn.style.fontSize = (currentSize + 5) + "px";
      yesBtn.style.transform = "scale(1.1)";
    });

    // YES click message
    yesBtn.onclick = () => {
      document.body.innerHTML = "<h1>YAYYY 💖 You made me the happiest person!</h1>";
    };

    // floating hearts generator
    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerText = "💖";

      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (3 + Math.random() * 3) + "s";

      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 6000);
    }

    setInterval(createHeart, 500);
  </script>

</body>
</html>
