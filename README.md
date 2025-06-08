<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio Piotra K</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #0D1C3F;
      color: #ffffff;
    }

    header, nav, footer {
      background-color: #000;
      color: white;
      width: 100%;
    }

    header {
      padding: 40px 20px;
      text-align: center;
    }

    nav {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      padding: 10px 20px;
    }

    .hamburger {
      display: none;
      font-size: 24px;
      cursor: pointer;
      background: none;
      border: none;
      color: white;
      margin-bottom: 10px;
    }

    .nav-buttons {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
      width: 100%;
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
      margin: 20px auto;
      max-width: 1400px;
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

    /* Lightbox */
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

    /* Mobile menu */
    @media (max-width: 768px) {
      .nav-buttons {
        overflow: hidden;
        max-height: 0;
        opacity: 0;
        transition: max-height 0.5s ease, opacity 0.5s ease;
        flex-direction: column;
        width: 100%;
        background-color: #000;
      }

      .nav-buttons.show {
        max-height: 500px;
        opacity: 1;
      }

      .hamburger {
        display: block;
      }
    }
  </style>
</head>
<body>

<header>
  <h1>Portfolio Piotra K</h1>
  <p>Przeglądaj zdjęcia w różnych kategoriach: Auta, Ludzie, Motory</p>
</header>

<nav>
  <button class="hamburger" onclick="toggleMenu()">☰ Menu</button>
  <div class="nav-buttons" id="navMenu">
    <button class="active-tab" onclick="showSection('auta', this)">Auta</button>
    <button onclick="showSection('ludzie', this)">Ludzie</button>
    <button onclick="showSection('motory', this)">Motory</button>
    <button onclick="showSection('o-mnie', this)">O mnie</button>
    <button onclick="showSection('kontakt', this)">Kontakt</button>
  </div>
</nav>

<!-- Auta -->
<section id="auta" class="category-section active">
  <h2>Zdjęcia Aut</h2>
  <h3>Sesja Supra</h3>
  <div class="gallery">
    <img loading="lazy" src="supra 1.jpg" alt="Supra 1" onclick="openLightbox(this)">
    <img loading="lazy" src="supra 2.jpg" alt="Supra 2" onclick="openLightbox(this)">
    <img loading="lazy" src="supra 3.jpg" alt="Supra 3" onclick="openLightbox(this)">
    <img loading="lazy" src="supra 6.jpg" alt="Supra 4" onclick="openLightbox(this)">
    <img loading="lazy" src="supra 5.jpg" alt="Supra 5" onclick="openLightbox(this)">
    <img loading="lazy" src="supra 4.jpg" alt="Supra 6" onclick="openLightbox(this)">
  </div>
</section>

<!-- Ludzie -->
<section id="ludzie" class="category-section">
  <h2>Portrety Ludzi</h2>
  <h3>Sesja Natalii</h3>
  <div class="gallery">
    <img loading="lazy" src="natalia 1.jpg" alt="Portret Natalia 1" onclick="openLightbox(this)">
    <img loading="lazy" src="natalia 2.jpg" alt="Portret Natalia 2" onclick="openLightbox(this)">
    <img loading="lazy" src="natalia 6.jpg" alt="Portret Natalia 3" onclick="openLightbox(this)">
    <img loading="lazy" src="natalia 4.jpg" alt="Portret Natalia 4" onclick="openLightbox(this)">
    <img loading="lazy" src="natalia 5.jpg" alt="Portret Natalia 5" onclick="openLightbox(this)">
    <img loading="lazy" src="natalia 8.jpg" alt="Portret Natalia 6" onclick="openLightbox(this)">
  </div>
</section>

<!-- Motory -->
<section id="motory" class="category-section">
  <h2>Motocykle</h2>
  <div class="gallery">
    <img loading="lazy" src="grzesiu 1.jpg" alt="Grzesiu 1" onclick="openLightbox(this)">
    <img loading="lazy" src="kask malgosia.jpg" alt="Małgosia 1" onclick="openLightbox(this)">
    <img loading="lazy" src="malgosia 2.jpg" alt="Małgosia 2" onclick="openLightbox(this)">
    <img loading="lazy" src="malgosia 3.jpg" alt="Małgosia 3" onclick="openLightbox(this)">
    <img loading="lazy" src="malowanie.jpg" alt="Malowanie" onclick="openLightbox(this)">
    <img loading="lazy" src="stunt duke.jpg" alt="Stunt" onclick="openLightbox(this)">
  </div>
</section>

<!-- O mnie -->
<section id="o-mnie" class="category-section">
  <h2>O mnie</h2>
  <p>Cześć! Nazywam się Piotr K. Zajmuję się fotografią pasjonacko, a moje ulubione tematy to motory, auta i portrety.</p>
</section>

<!-- Kontakt -->
<section id="kontakt" class="category-section">
  <h2>Kontakt</h2>
  <p><strong>Instagram:</strong> <a href="https://www.instagram.com/pan_kaczan____/" target="_blank">@pan_kaczan____</a></p>
  <p><strong>E-mail:</strong> <a href="mailto:kontakt@twojadomena.pl">kontakt@twojadomena.pl</a></p>
</section>

<!-- Stopka -->
<footer>
  &copy; 2025 Portfolio Piotra K. Wszystkie prawa zastrzeżone.
</footer>

<!-- Lightbox -->
<div id="lightbox" onclick="this.style.display='none'">
  <img id="lightbox-img" src="" alt="">
</div>

<!-- Skrypty -->
<script>
  function showSection(id, btn) {
    const sections = document.querySelectorAll('.category-section');
    const buttons = document.querySelectorAll('nav button');
    sections.forEach(section => section.classList.remove('active'));
    buttons.forEach(b => b.classList.remove('active-tab'));
    document.getElementById(id).classList.add('active');
    btn.classList.add('active-tab');
    if (window.innerWidth <= 768) toggleMenu(); // zamknij menu po kliknięciu
  }

  function openLightbox(img) {
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    lightboxImg.src = img.src;
    lightbox.style.display = 'flex';
  }

  function toggleMenu() {
    document.getElementById('navMenu').classList.toggle('show');
  }
</script>

</body>
</html>

