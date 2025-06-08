<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio Piotra K</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      background: linear-gradient(180deg, #0a0a0a, #1a0000);
      color: #fff;
    }

    header {
      background-color: #000;
      color: #ff3c00;
      padding: 40px 20px;
      text-align: center;
    }

    nav {
      background-color: #000;
      display: flex;
      justify-content: center;
      padding: 10px;
      gap: 20px;
      flex-wrap: wrap;
    }

    nav button {
      background: none;
      border: 2px solid transparent;
      color: #fff;
      font-size: 16px;
      padding: 10px 20px;
      cursor: pointer;
      transition: 0.3s;
    }

    nav button:hover,
    nav button.active-tab {
      border-bottom: 2px solid #ff4500;
      color: #ff4500;
    }

    .category-section {
      display: none;
      padding: 30px 20px;
      background-color: rgba(20, 0, 0, 0.8);
      color: #fff;
      border-radius: 10px;
      margin: 20px;
    }

    .category-section.active {
      display: block;
    }

    .category-section h2 {
      margin-bottom: 20px;
      border-left: 6px solid #ff3c00;
      padding-left: 10px;
      color: #ff3c00;
    }

    .category-section h3 {
      margin-top: 40px;
      color: #ff6347;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 15px;
      margin-bottom: 30px;
    }

    .gallery img {
      width: 100%;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(255, 69, 0, 0.3);
      cursor: pointer;
      transition: 0.3s;
    }

    .gallery img:hover {
      transform: scale(1.02);
    }

    #o-mnie, #kontakt {
      background-color: rgba(30, 0, 0, 0.9);
      padding: 40px 20px;
      margin-top: 20px;
      border-top: 4px solid #ff4500;
      border-radius: 10px;
    }

    #o-mnie h2, #kontakt h2 {
      margin-top: 0;
      color: #ff3c00;
    }

    #kontakt a {
      color: #ff6347;
      text-decoration: none;
    }

    #kontakt a:hover {
      text-decoration: underline;
    }

    footer {
      text-align: center;
      padding: 20px;
      background-color: #000;
      color: #fff;
    }

    /* LIGHTBOX STYLES */
    #lightbox {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      display: none;
      justify-content: center;
      align-items: center;
      background-color: rgba(0, 0, 0, 0.9);
      z-index: 9999;
    }

    #lightbox img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
      box-shadow: 0 0 20px #ff3c00;
    }

    #lightbox-close {
      position: absolute;
      top: 30px;
      right: 40px;
      font-size: 40px;
      color: #fff;
      cursor: pointer;
      z-index: 10000;
    }
  </style>
</head>
<body>

<header>
  <h1>Portfolio Piotra K</h1>
  <p>Przeglądaj zdjęcia w różnych kategoriach: Auta, Ludzie, Motory</p>
</header>

<nav>
  <button class="active-tab" onclick="showSection('auta')">Auta</button>
  <button onclick="showSection('ludzie')">Ludzie</button>
  <button onclick="showSection('motory')">Motory</button>
  <button onclick="showSection('o-mnie')">O mnie</button>
  <button onclick="showSection('kontakt')">Kontakt</button>
</nav>

<section id="auta" class="category-section active">
  <h2>Zdjęcia Aut</h2>

  <h3>Sesja Supra</h3>
  <div class="gallery">
    <img src="supra 1.jpg" alt="">
    <img src="supra 2.jpg" alt="">
    <img src="supra 3.jpg" alt="">
  </div>
</section>

<section id="ludzie" class="category-section">
  <h2>Portrety Ludzi</h2>
  <h3>Sesja Natalii</h3>
  <div class="gallery">
    <img src="natalia 1.jpg" alt="">
    <img src="natalia 2.jpg" alt="">
    <img src="natalia 3.jpg" alt="">
  </div>
</section>

<section id="motory" class="category-section">
  <h2>Motocykle</h2>
  <div class="gallery">
    <img src="motor 1.jpg" alt="">
    <img src="motor 2.jpg" alt="">
    <img src="motor 3.jpg" alt="">
  </div>
</section>

<section id="o-mnie" class="category-section">
  <h2>O mnie</h2>
  <p>Cześć! Nazywam się Piotr K. Zajmuję się fotografią pasjonacko, a moje ulubione tematy to motory, auta i portrety.</p>
</section>

<section id="kontakt" class="category-section">
  <h2>Kontakt</h2>
  <p><strong>Instagram:</strong> <a href="https://www.instagram.com/pan_kaczan____/" target="_blank">@pan_kaczan____</a></p>
  <p><strong>E-mail:</strong> <a href="mailto:kontakt@twojadomena.pl">kontakt@twojadomena.pl</a></p>
</section>

<footer>
  &copy; 2025 Portfolio Piotra K. Wszystkie prawa zastrzeżone.
</footer>

<!-- LIGHTBOX -->
<div id="lightbox">
  <span id="lightbox-close">&times;</span>
  <img id="lightbox-img" src="" alt="lightbox" />
</div>

<script>
  function showSection(id) {
    const sections = document.querySelectorAll('.category-section');
    const buttons = document.querySelectorAll('nav button');

    sections.forEach(section => section.classList.remove('active'));
    buttons.forEach(btn => btn.classList.remove('active-tab'));

    document.getElementById(id).classList.add('active');
    event.target.classList.add('active-tab');
  }

  // Lightbox logic
  const lightbox = document.getElementById('lightbox');
  const lightboxImg = document.getElementById('lightbox-img');
  const closeBtn = document.getElementById('lightbox-close');

  document.querySelectorAll('.gallery img').forEach(img => {
    img.addEventListener('click', () => {
      lightboxImg.src = img.src;
      lightbox.style.display = 'flex';
    });
  });

  closeBtn.addEventListener('click', () => {
    lightbox.style.display = 'none';
  });

  lightbox.addEventListener('click', (e) => {
    if (e.target === lightbox || e.target === closeBtn) {
      lightbox.style.display = 'none';
    }
  });
</script>

</body>
</html>
