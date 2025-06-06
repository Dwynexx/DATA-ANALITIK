<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>🎂 Selamat Ulang Tahun Skay!</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive;
      overflow: hidden;
      background: linear-gradient(to top left, #ffe0ec, #e0c3fc);
    }
    .layer {
      position: absolute;
      top: 0; left: 0;
      width: 100vw;
      height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 40px;
      text-align: center;
      transition: opacity 1s ease;
      background: rgba(255,255,255,0.9);
    }
    .hidden {
      opacity: 0;
      pointer-events: none;
    }
    h1 {
      color: #e84393;
      font-size: 2.5em;
      margin-bottom: 10px;
    }
    p {
      font-size: 1.3em;
      color: #2d3436;
      max-width: 800px;
      margin: 10px 0;
      line-height: 1.6;
    }
    button {
      margin-top: 25px;
      padding: 12px 25px;
      font-size: 1.1em;
      background-color: #fd79a8;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
    button:hover {
      background-color: #e17055;
    }
    .confetti {
      position: absolute;
      top: -20px;
      font-size: 2em;
      animation: fall 3s linear forwards;
    }
    @keyframes fall {
      to { transform: translateY(100vh); opacity: 0; }
    }
    .emoji {
      font-size: 2em;
      margin: 15px 0;
    }
  </style>
</head>
<body>

  <div class="layer" id="layer1">
    <h1>Hai Skay! 🌟</h1>
    <p>Selamat ulang tahun ya! Semoga hari ini Skay dapet banyak banget kado, surprise, dan tentu aja pelukan hangat dari orang-orang terdekat.</p>
    <button onclick="next(1)">Lanjut ➡️</button>
  </div>

  <div class="layer hidden" id="layer2">
    <p>Hari spesial kayak gini harus banget dirayain dengan penuh senyum dan hati yang bahagia.</p>
    <p>Dika doain semoga di umur baru ini, semua mimpi Skay makin deket buat diwujudkan.</p>
    <button onclick="next(2)">Lanjut ➡️</button>
  </div>

  <div class="layer hidden" id="layer3">
    <p>Semoga Skay selalu sehat, makin kece, dan penuh semangat ngejar apa pun yang Skay pengenin.</p>
    <p>Jangan lupa, istirahat yang cukup dan makan makanan favorit biar makin happy! 🍜🍰</p>
    <button onclick="next(3)">Lanjut ➡️</button>
  </div>

  <div class="layer hidden" id="layer4">
    <p>Ingat ya, hidup itu penuh warna. Kadang ada yang seru, kadang ada yang bikin mikir, tapi semua itu yang bikin kita tumbuh jadi pribadi yang lebih keren dan kuat.</p>
    <p>Nikmati setiap detik perjalanan Skay, termasuk yang lucu, awkward, dan memorable!</p>
    <button onclick="next(4)">Lanjut ➡️</button>
  </div>

  <div class="layer hidden" id="layer5">
    <p>Pokoknya, terus jadi Skay yang selalu ceria, baik hati, dan penuh inspirasi buat orang sekitar.</p>
    <p>Skay itu keren banget, dan Dika yakin dunia ini bakal jadi tempat yang lebih indah karena Skay ada 💖</p>
    <button onclick="next(5)">Lanjut ➡️</button>
  </div>

  <div class="layer hidden" id="layer6">
    <p>Jangan lupa buat sesekali manjain diri sendiri, jalan-jalan, ketawa lepas, dan kumpul sama teman-teman yang selalu support Skay.</p>
    <p>Karena Skay layak dapetin semua hal baik dan kebahagiaan.</p>
    <button onclick="next(6)">Lanjut ➡️</button>
  </div>

  <div class="layer hidden" id="layer7">
    <h1>🎉 Sekali lagi... Selamat Ulang Tahun Skay! 🎂</h1>
    <p>Semoga tahun ini jadi babak baru yang penuh kejutan menyenangkan dan cerita seru.</p>
    <p>Dika selalu ada di sini, dukung Skay dari jauh 💌</p>
    <div class="emoji">💖🎁🎊🎉🎂</div>
    <button onclick="showConfetti()">🎊 Klik untuk Surprise!</button>
  </div>

  <script>
    function next(current) {
      document.getElementById("layer" + current).classList.add("hidden");
      document.getElementById("layer" + (current + 1)).classList.remove("hidden");
    }

    function showConfetti() {
      for (let i = 0; i < 80; i++) {
        let confetti = document.createElement("div");
        confetti.className = "confetti";
        confetti.innerText = ["🎉", "✨", "💖", "🎊"][Math.floor(Math.random() * 4)];
        confetti.style.left = Math.random() * window.innerWidth + "px";
        confetti.style.animationDuration = (Math.random() * 2 + 2) + "s";
        document.body.appendChild(confetti);
        setTimeout(() => confetti.remove(), 4000);
      }
      alert("🥳 Happy Birthday Skay! Dari Dika ❤️");
    }
  </script>

</body>
</html>
