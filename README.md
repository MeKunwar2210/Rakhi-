<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Raksha Bandhan Didi!</title>
  <style>
    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive;
      background: linear-gradient(to bottom right, #ffccff, #ffe6e6);
      overflow: hidden;
    }

    #welcome {
      text-align: center;
      padding-top: 100px;
      font-size: 36px;
      color: #8B0000;
      animation: fadeIn 2s ease;
    }

    #rakhiBtn {
      margin-top: 40px;
      padding: 15px 30px;
      font-size: 20px;
      background-color: #FF69B4;
      border: none;
      color: white;
      border-radius: 10px;
      cursor: pointer;
      animation: pulse 2s infinite;
    }

    #messageBox {
      display: none;
      text-align: center;
      margin-top: 50px;
      animation: fadeIn 2s ease;
    }

    #messageText {
      font-size: 28px;
      color: #5A005A;
      margin-bottom: 20px;
      white-space: pre-line;
    }

    #gallery {
      display: none;
      text-align: center;
      margin-top: 20px;
    }

    img {
      width: 200px;
      margin: 10px;
      border-radius: 10px;
      box-shadow: 0 0 10px #888;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.1); }
      100% { transform: scale(1); }
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 6s infinite;
    }

    .heart:before,
    .heart:after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .heart:before {
      top: -10px;
      left: 0;
    }

    .heart:after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% { bottom: 0; opacity: 1; }
      100% { bottom: 100%; opacity: 0; }
    }
  </style>
</head>
<body>

  <div id="welcome">🎉 Happy Raksha Bandhan, Didi! 🎉</div>
  <div style="text-align:center">
    <button id="rakhiBtn">Click to open your surprise 🎁</button>
  </div>

  <div id="messageBox">
    <div id="messageText">
      Dear Didi, 💌

      Thank you for being my best friend, protector, and constant support.
      I’m lucky to have a sister like you. Happy Rakhi!

      Love you always! ❤️
    </div>
  </div>

  <div id="gallery">
    <h2>Our Memories 📸</h2>
    <img src="https://via.placeholder.com/200x200?text=Photo+1" alt="Photo 1">
    <img src="https://via.placeholder.com/200x200?text=Photo+2" alt="Photo 2">
    <img src="https://via.placeholder.com/200x200?text=Photo+3" alt="Photo 3">
  </div>

  <!-- Floating hearts -->
  <script>
    function showSurprise() {
      document.getElementById('messageBox').style.display = 'block';
      document.getElementById('gallery').style.display = 'block';
      createHearts();
    }

    document.getElementById('rakhiBtn').addEventListener('click', showSurprise);

    function createHearts() {
      for (let i = 0; i < 20; i++) {
        const heart = document.createElement('div');
        heart.className = 'heart';
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.animationDuration = (3 + Math.random() * 3) + 's';
        document.body.appendChild(heart);

        setTimeout(() => heart.remove(), 99999999);
      }
    }
  </script>

</body>
</html>
