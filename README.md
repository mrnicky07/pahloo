<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Paglo, Baat Karo 😢</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      background: linear-gradient(to top left, #fff0f5, #ffe6f0);
      font-family: 'Segoe UI', sans-serif;
      text-align: center;
      color: #99004d;
    }

    h1 {
      margin-top: 20vh;
      font-size: 2.5em;
      animation: fadeIn 2s ease-in;
    }

    p {
      font-size: 1.3em;
      padding: 20px;
      animation: fadeIn 3s ease-in;
    }

    button {
      padding: 12px 30px;
      font-size: 1.1em;
      background: #fff;
      color: #ff3399;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #ffe6f0;
    }

    .footer {
      margin-top: 30px;
      font-size: 0.9em;
      color: #993355;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 6s linear infinite;
      opacity: 0.5;
    }

    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% { top: -10%; }
      100% { top: 110%; }
    }
  </style>
</head>
<body>

  <h1>Paglo... kya hua? 😔</h1>
  <p>Baat kyon nahi kar rahi ho? Tumse baat na ho toh sab suna suna lagta hai 💔</p>
  <button onclick="alert('Chalo na, baat kar lo 😢')">Maaf kar do 😢</button>

  <div class="footer">~ Tumhara pagal dost jo har roz wait karta hai ❤️</div>

  <!-- Falling hearts -->
  <script>
    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = Math.random() * 2 + 4 + 's';
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 6000);
    }
    setInterval(createHeart, 300);
  </script>

  <!-- Background Music -->
  <audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

</body>
</html>
