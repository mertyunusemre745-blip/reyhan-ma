<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>❤️ Bizim Hikayemiz ❤️</title>

<p style="text-align:center; font-size:12px; opacity:0.6;">
  Bu site kalpten yapıldı 💖
</p>
  
<button id="loveBtn">💖 Tıkla 💖</button>


  <style>
#loveBtn {
  padding: 12px 24px;
  border: none;
  border-radius: 20px;
  background: #ff6b9a;
  color: white;
  font-size: 16px;
  cursor: pointer;
}

.heart {
  position: fixed;
  bottom: 0;
  font-size: 20px;
  animation: floatUp 3s linear forwards;
  pointer-events: none;
}

@keyframes floatUp {
  from {
    transform: translateY(0);
    opacity: 1;
  }
  to {
    transform: translateY(-100vh);
    opacity: 0;
  }
}
    img {
  transition: 0.3s;
}
img:hover {
  transform: scale(1.03);
}

.poem {
  animation: fadeIn 1.5s ease forwards;
  margin-bottom: 12px;
}
    .poems {
  position: fixed;
  left: 30px;
  top: 150px;
  width: 220px;
  color: white;
  font-size: 16px;
  line-height: 1.8;
  z-index: 5;
}

.poems p {
  background: rgba(255, 255, 255, 0.15);
  padding: 10px 14px;
  border-radius: 12px;
  margin-bottom: 12px;
  animation: fadeIn 1s ease forwards;
}
    body {
      margin: 0;
      height: 100vh;
      overflow: hidden;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(120deg, #ff9a9e, #fad0c4);
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: white;
    }

    h1 {
      font-size: 3rem;
    }

    .note {
      font-size: 1.5rem;
      margin-top: 400px;
      animation: fade 5s infinite;
    }

    @keyframes fade {
      0% { opacity: 0; }
      20% { opacity: 1; }
      80% { opacity: 1; }
      100% { opacity: 0; }
    }

    .slideshow img {
      width: 500px;
      height: 350px;
      object-fit: cover;
      border-radius: 20px;
      position: absolute;
      opacity: 0;
      animation: slide 15s infinite;
    }

    .slideshow img:nth-child(1) { animation-delay: 0s; }
    .slideshow img:nth-child(2) { animation-delay: 5s; }
    .slideshow img:nth-child(3) { animation-delay: 10s; }

    @keyframes slide {
      0% { opacity: 0; }
      10% { opacity: 1; }
      30% { opacity: 1; }
      40% { opacity: 0; }
      100% { opacity: 0; }
    }

    .heart {
      position: fixed;
      top: -10px;
      font-size: 20px;
      animation: fall linear forwards;
    }

    @keyframes fall {
      to {
        transform: translateY(100vh);
        opacity: 0;
      }
    }

    #locked {
      display: none;
    }
  </style>
</head>

<body>

    <div class="poems">
  <p>Sen gülünce dünya duruyor 💗</p>
  <p>Adını anınca kalbim hızlanıyor ✨</p>
  <p>Yanımda olman yetiyor bana 🌙</p>
  <p>İyi ki biz olmuşuz ❤️</p>
  <p>Bir ömür sen 🫶</p>
</div>
<script>
document.querySelectorAll('.poem').forEach(p => {
  p.addEventListener('click', () => {
    p.innerHTML += " ❤️ ";
  });
});
</script>

<div id="locked">
  <h1>🔒 Henüz Zamanı Değil</h1>
  <p>💌 08.03.2026 tarihinde açılacak</p>
</div>

<div id="content">
  <h1>💖 İyi ki Varsın Aşkım 💖</h1>

  <div class="slideshow">
    <img src="resim1.jpg">
    <img src="resim2.jpg">
    <img src="resim3.jpg">
    <img src="resim4.jpg">
    <img src="resim5.jpg">
    <img src="resim6.jpg">
    <img src="resim7.jpg">
    <img src="resim8.jpg">
    <img src="resim9.jpg">
    <img src="resim10.jpg">
    
    
  </div>

  <div class="note" id="note"></div>

  
  <iframe data-testid="embed-iframe" style="border-radius:12px"
   src="https://open.spotify.com/embed/track/3FoxsQsG5Z9bMuqdF5szJO?utm_source=generator" 
  width="100%" height="352" frameBorder="0" allowfullscreen="" 
  allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" 
  loading="lazy"></iframe>
</div>

<script>
  const openDate = new Date(2020, 2, 8);
  const today = new Date();

  const locked = document.getElementById("locked");
  const content = document.getElementById("content");

  if (today < openDate) {
    locked.style.display = "block";
    content.style.display = "none";
  } else {
    locked.style.display = "none";
    content.style.display = "block";
  }

  const notes = [
    "08.03.2025 – Her şey seninle başladı ❤️",
    "1 yıldır yan yanayız 💕",
    "Nice yıllarımıza aşkım 😘",
    "Seni çok seviyorum 💖"
  ];

  let index = 0;
  const noteElement = document.getElementById("note");

  setInterval(() => {
    noteElement.textContent = notes[index];
    index = (index + 1) % notes.length;
  }, 5000);

  setInterval(() => {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (3 + Math.random() * 3) + "s";
    document.body.appendChild(heart);

    setTimeout(() => heart.remove(), 6000);
  }, 300);
</script>

<script>
document.getElementById("loveBtn").addEventListener("click", () => {
  const emojis = ["💖", "💗", "💘", "😻", "🐱"];

  for (let i = 0; i < 25; i++) {
    const item = document.createElement("div");
    item.className = "heart";
    item.innerText = emojis[Math.floor(Math.random() * emojis.length)];
    item.style.left = Math.random() * 100 + "vw";
    item.style.animationDuration = (2 + Math.random() * 2) + "s";
    item.style.fontSize = (16 + Math.random() * 14) + "px";

    document.body.appendChild(item);

    setTimeout(() => {
      item.remove();
    }, 3000);
  }
});
</script>
</body>
</html>
