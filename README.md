<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Portfolio Piotra K</title>
  <style>
    * {
      box-sizing: border-box;
    }

    html, body {
      margin: 0;
      padding: 0;
      width: 100%;
      height: 100%;
      font-family: 'Segoe UI', sans-serif;
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
      margin: 20px auto;
      width: 100%;
      max-width: 1600px;
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

    /* RESPONSYWNOŚĆ */
    @media (max-width: 768px) {
      nav {
        flex-direction: column;
        align-items: center;
      }

      nav button {
        width: 100%;
        max-width: 300px;
      }

      .gallery {
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
      }

      header {
        padding: 30px 10px;
      }

      .category-section {
        margin: 10px;
        padding: 20px 10px;
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
  <button class="active-tab" onclick="showSection('auta', event)">Auta</button>
  <button onclick="showSection('ludzie', event)">Ludzie</button>
  <button onclick="showSection('motory', event)">Motory</button>
  <button onclick="showSection('o-mnie', event)">O mnie</button>
  <button onclick="showSection('kontakt', event)">Kontakt</button>
</nav>

<section id="auta" class="category-section active">
  <h2>Zdjęcia Aut</h2>

  <h3>Sesja Supra</h3>
  <div class="gallery">
    <img src="supra 1.jpg" alt="Supra 1" onclick="openLightbox(this)">
    <img src="supra 2.jpg" alt="Supra 2" onclick="openLightbox(this)">
    <img src="supra 3.jpg" alt="Supra 3" onclick="openLightbox(this)">
    <img src="supra 6.jpg" alt="Supra 4" onclick="openLightbox(this)">
    <img src="supra 5.jpg" alt="Supra 5" onclick="openLightbox(this)">
    <img src="supra 4.jpg" alt="Supra 6" onclick="openLightbox(this)">
  </div>

  <h3>Sesja g3m_green_g0blin</h3>
  <div class="gallery">
    <img src="gren 1.jpg" alt="Gren 1" onclick="openLightbox(this)">
    <img src="gren 6.jpg" alt="Gren 2" onclick="openLightbox(this)">
    <img src="gren 3.jpg" alt="Gren 3" onclick="openLightbox(this)">
    <img src="gren 4.jpg" alt="Gren 4" onclick="openLightbox(this)">
    <img src="gren 5.jpg" alt="Gren 5" onclick="openLightbox(this)">
    <img src="gren 2.jpg" alt="Gren 6" onclick="openLightbox(this)">
  </div>

  <h3>Sesja Kamil</h3>
  <div class="gallery">
    <img src="kamil 1.jpg" alt="Kamil 1" onclick="openLightbox(this)">
    <img src="kamil 2.jpg" alt="Kamil 2" onclick="openLightbox(this)">
    <img src="kamil 3.jpg" alt="Kamil 3" onclick="openLightbox(this)">
    <img src="kamil 4.jpg" alt="Kamil 4" onclick="openLightbox(this)">
    <img src="kamil 5.jpg" alt="Kamil 5" onclick="openLightbox(this)">
    <img src="kamil 6.jpg" alt="Kamil 6" onclick="openLightbox(this)">
  </div>

  <h3>Sesja Gabi</h3>
  <div class="gallery">
    <img src="gabi 1.jpg" alt="Gabi 1" onclick="openLightbox(this)">
    <img src="gabi 2.jpg" alt="Gabi 2" onclick="openLightbox(this)">
    <img src="gabi 3.jpg" alt="Gabi 3" onclick="openLightbox(this)">
    <img src="gabi 4.jpg" alt="Gabi 4" onclick="openLightbox(this)">
    <img src="gabi 5.jpg" alt="Gabi 5" onclick="openLightbox(this)">
    <img src="gabi 6.jpg" alt="Gabi 6" onclick="openLightbox(this)">
  </div>
</section>

<section id="ludzie" class="category-section">
  <h2>Portrety Ludzi</h2>

  <h3>Sesja Natalii</h3>
  <div class="gallery">
    <img src="natalia 1.jpg" alt="Portret Natalia 1" onclick="openLightbox(this)">
    <img src="natalia 2.jpg" alt="Portret Natalia 2" onclick="openLightbox(this)">
    <img src="natalia 6.jpg" alt="Portret Natalia 3" onclick="openLightbox(this)">
    <img src="natalia 4.jpg" alt="Portret Natalia 4" onclick="openLightbox(this)">
    <img src="natalia 5.jpg" alt="Portret Natalia 5" onclick="openLightbox(this)">
    <img src="natalia 8.jpg" alt="Portret Natalia 6" onclick="openLightbox(this)">
  </div>

  <h3>Sesja Rudej</h3>
  <div class="gallery">
    <img src="Ruda.jpg" alt="Ruda 1" onclick="openLightbox(this)">
    <img src="Ruda 2.jpg" alt="Ruda 2" onclick="openLightbox(this)">
    <img src="Ruda 3.jpg" alt="Ruda 3" onclick="openLightbox(this)">
    <img src="Ruda 4.jpg" alt="Ruda 4" onclick="openLightbox(this)">
    <img src="Ruda 5.jpg" alt="Ruda 5" onclick="openLightbox(this)">
    <img src="Ruda 1.jpg" alt="Ruda 6" onclick="openLightbox(this)">
  </div>
</section>

<section id="motory" class="category-section">
  <h2>Motocykle</h2>
  <div class="gallery">
    <img src="grzesiu 1.jpg" alt="Grzesiu 1" onclick="openLightbox(this)">
    <img src="kask malgosia.jpg" alt="Małgosia 1" onclick="openLightbox(this)">
    <img src="malgosia 2.jpg" alt="Małgosia 2" onclick="openLightbox(this)">
    <img src="malgosia 3.jpg" alt="Małgosia 3" onclick="openLightbox(this)">
    <img src="malowanie.jpg" alt="Malowanie" onclick="openLightbox(this)">
    <img src="stunt duke.jpg" alt="Stunt" onclick="openLightbox(this)">
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

<!-- Lightbox -->
<div id="lightbox" onclick="this.style.display='none'">
  <img id="lightbox-img" src="" alt="">
</div>

<script>
  function showSection(id, event) {
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

