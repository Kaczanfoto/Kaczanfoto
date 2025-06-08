<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio Piotra K</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      background-color: #0D1C3F;
      color: #ffffff;
    }

    header, nav, footer {
      background-color: #000;
      color: white;
    }

    header {
      padding: 40px 20px;
      text-align: center;
    }

    nav {
      display: flex;
      justify-content: center;
      padding: 10px;
      gap: 20px;
      flex-wrap: wrap;
    }

    nav button {
      background: none;
      border: 2px solid transparent;
      color: white;
      font-size: 16px;
      padding: 10px 20px;
      cursor: pointer;
      transition: 0.3s;
    }

    nav button:hover,
    nav button.active-tab {
      border-bottom: 2px solid #66ccff;
    }

    .category-section {
      display: none;
      padding: 30px 20px;
      background-color: rgba(255, 255, 255, 0.05);
      border-radius: 10px;
      margin: 20px;
    }

    .category-section.active {
      display: block;
    }

    .category-section h2 {
      margin-bottom: 20px;
      border-left: 6px solid #66ccff;
      padding-left: 10px;
      color: #66ccff;
    }

    .category-section h3 {
      margin-top: 40px;
      color: #66ccff;
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
      cursor: pointer;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);
      transition: transform 0.2s ease;
    }

    .gallery img:hover {
      transform: scale(1.02);
    }

    #o-mnie, #kontakt {
      background-color: rgba(255, 255, 255, 0.07);
      padding: 40px 20px;
      margin-top: 20px;
      border-top: 4px solid #66ccff;
      border-radius: 10px;
    }

    #kontakt a {
      color: #66ccff;
      text-decoration: none;
    }

    #kontakt a:hover {
      text-decoration: underline;
    }

    footer {
      text-align: center;
      padding: 20px;
    }

    #lightbox {
      position: fixed;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.8);
      display: none;
      justify-content: center;
      align-items: center;
      z-index: 9999;
      animation: fadeIn 0.5s ease-in-out;
    }

    #lightbox img {
      max-width: 90%;
      max-height: 80%;
      border-radius: 8px;
      box-shadow: 0 0 20px #66ccff;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
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

<!-- Tutaj zaczynają się sekcje -->
<section id="auta" class="category-section active">
  <h2>Zdjęcia Aut</h2>

  <h3>Sesja Supra</h3>
  <div class="gallery">
    <img src="img/supra 1.jpg" alt="Supra 1" loading="lazy" onclick="openLightbox(this)">
    <img src="img/supra 2.jpg" alt="Supra 2" loading="lazy" onclick="openLightbox(this)">
    <img src="img/supra 3.jpg" alt="Supra 3" loading="lazy" onclick="openLightbox(this)">
    <img src="img/supra 4.jpg" alt="Supra 4" loading="lazy" onclick="openLightbox(this)">
    <img src="img/supra 5.jpg" alt="Supra 5" loading="lazy" onclick="openLightbox(this)">
    <img src="img/supra 6.jpg" alt="Supra 6" loading="lazy" onclick="openLightbox(this)">
  </div>

  <h3>Sesja g3m_green_g0blin</h3>
  <div class="gallery">
    <img src="img/gren 1.jpg" alt="Gren 1" loading="lazy" onclick="openLightbox(this)">
    <img src="img/gren 2.jpg" alt="Gren 2" loading="lazy" onclick="openLightbox(this)">
    <img src="img/gren 3.jpg" alt="Gren 3" loading="lazy" onclick="openLightbox(this)">
    <img src="img/gren 4.jpg" alt="Gren 4" loading="lazy" onclick="openLightbox(this)">
    <img src="img/gren 5.jpg" alt="Gren 5" loading="lazy" onclick="openLightbox(this)">
    <img src="img/gren 6.jpg" alt="Gren 6" loading="lazy" onclick="openLightbox(this)">
  </div>

  <h3>Sesja Kamil</h3>
  <div class="gallery">
    <img src="img/kamil 1.jpg" alt="Kamil 1" loading="lazy" onclick="openLightbox(this)">
    <img src="img/kamil 2.jpg" alt="Kamil 2" loading="lazy" onclick="openLightbox(this)">
    <img src="img/kamil 3.jpg" alt="Kamil 3" loading="lazy" onclick="openLightbox(this)">
    <img src="img/kamil 4.jpg" alt="Kamil 4" loading="lazy" onclick="openLightbox(this)">
    <img src="img/kamil 5.jpg" alt="Kamil 5" loading="lazy" onclick="openLightbox(this)">
    <img src="img/kamil 6.jpg" alt="Kamil 6" loading="lazy" onclick="openLightbox(this)">
  </div>

  <h3>Sesja Gabi</h3>
  <div class="gallery">
    <img src="img/gabi 1.jpg" alt="Gabi 1" loading="lazy" onclick="openLightbox(this)">
    <img src="img/gabi 2.jpg" alt="Gabi 2" loading="lazy" onclick="openLightbox(this)">
    <img src="img/gabi 3.jpg" alt="Gabi 3" loading="lazy" onclick="openLightbox(this)">
    <img src="img/gabi 4.jpg" alt="Gabi 4" loading="lazy" onclick="openLightbox(this)">
    <img src="img/gabi 5.jpg" alt="Gabi 5" loading="lazy" onclick="openLightbox(this)">
    <img src="img/gabi 6.jpg" alt="Gabi 6" loading="lazy" onclick="openLightbox(this)">
  </div>
</section>
<!-- Dalej są sekcje Ludzie, Motory itd., analogicznie z poprawionymi ścieżkami -->

<!-- Lightbox -->
<div id="lightbox" onclick="this.style.display='none'">
  <img id="lightbox-img" src="" alt="">
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

  function openLightbox(img) {
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    lightboxImg.src = img.src;
    lightbox.style.display = 'flex';
  }
</script>

</body>
</html>
