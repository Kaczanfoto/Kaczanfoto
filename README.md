<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio Piotra K</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      background: navy; /* nowy kolor tła */
      color: #f0f0f0;
    }

    header {
      background-color: #000;
      color: white;
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
      color: white;
      font-size: 16px;
      padding: 10px 20px;
      cursor: pointer;
      transition: 0.3s;
    }

    nav button:hover,
    nav button.active-tab {
      border-bottom: 2px solid #66ccff; /* jasnoniebieski akcent */
    }

    .category-section {
      display: none;
      padding: 30px 20px;
      background-color: rgba(255, 255, 255, 0.05);
      color: #f0f0f0;
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
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);
      cursor: pointer;
      transition: 0.3s;
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

    #o-mnie h2, #kontakt h2 {
      margin-top: 0;
      color: #66ccff;
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
      background-color: #000;
      color: white;
    }

    /* LIGHTBOX STYLES */
    #lightbox {
      position: fixed;
      display: none;
      justify-content: center;
      align-items: center;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-color: rgba(0, 0, 0, 0.95);
      z-index: 9999;
      animation: fadeIn 0.5s ease-in;
    }

    #lightbox img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
      box-shadow: 0 0 20px #66ccff;
    }

    #lightbox-close {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 40px;
      color: #66ccff;
      cursor: pointer;
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
      }
      to {
        opacity: 1;
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
  <button class="active-tab" onclick="showSection('auta')">Auta</button>
  <button onclick="showSection('ludzie')">Ludzie</button>
  <button onclick="showSection('motory')">Motory</button>
  <button onclick="showSection('o-mnie')">O mnie</button>
  <button onclick="showSection('kontakt')">Kontakt</button>
</nav>

<section id="auta" class="category-section active">
  <h2>Zdjęcia Aut</h2>
  <!-- Galerie -->
<h3>Sesja Supra</h3>
  <div class="gallery">
    <img src="supra 1.jpg" alt="Supra 1">
    <img src="supra 2.jpg" alt="Supra 2">
    <img src="supra 3.jpg" alt="Supra 3">
    <img src="supra 6.jpg" alt="Supra 4">
    <img src="supra 5.jpg" alt="Supra 5">
    <img src="supra 4.jpg" alt="Supra 6">
  </div>

  <h3>Sesja g3m_green_g0blin</h3>
  <div class="gallery">
    <img src="gren 1.jpg" alt="Gren 1">
    <img src="gren 6.jpg" alt="Gren 2">
    <img src="gren 3.jpg" alt="Gren 3">
    <img src="gren 4.jpg" alt="Gren 4">
    <img src="gren 5.jpg" alt="Gren 5">
    <img src="gren 2.jpg" alt="Gren 6">
  </div>

  <h3>Sesja Kamil</h3>
  <div class="gallery">
    <img src="kamil 1.jpg" alt="Kamil 1">
    <img src="kamil 2.jpg" alt="Kamil 2">
    <img src="kamil 3.jpg" alt="Kamil 3">
  </div>

  <h3>Sesja Gabi</h3>
  <div class="gallery">
    <img src="gabi 1.jpg" alt="Gabi 1">
    <img src="gabi 2.jpg" alt="Gabi 2">
    <img src="gabi 3.jpg" alt="Gabi 3">
    <img src="gabi 4.jpg" alt="Gabi 4">
    <img src="gabi 5.jpg" alt="Gabi 5">
    <img src="gabi 6.jpg" alt="Gabi 6">
  </div>
  
</section>

<section id="ludzie" class="category-section">
  <h2>Portrety Ludzi</h2>
  <!-- Galerie -->
<h3>Sesja Natalii</h3>
  <div class="gallery">
    <img src="natalia 1.jpg" alt="Portret Natalia 1">
    <img src="natalia 2.jpg" alt="Portret Natalia 2">
    <img src="natalia 6.jpg" alt="Portret Natalia 3">
    <img src="natalia 4.jpg" alt="Portret Natalia 4">
    <img src="natalia 5.jpg" alt="Portret Natalia 5">
    <img src="natalia 8.jpg" alt="Portret Natalia 6">
  </div>

  <h3>Sesja Rudej</h3>
  <div class="gallery">
    <img src="ruda.jpg" alt="Ruda 1">
    <img src="ruda 2.jpg" alt="Ruda 2">
    <img src="ruda 3.jpg" alt="Ruda 3">
    <img src="ruda 4.jpg" alt="Ruda 4">
    <img src="ruda 5.jpg" alt="Ruda 5">
    <img src="rada1.jpg" alt="Ruda 6">
  </div>

  
</section>

<section id="motory" class="category-section">
  <h2>Motocykle</h2>
  <!-- Galerie -->
 <div class="gallery">
    <img src="grzesiu 1.jpg" alt="Grzesiu 1">
    <img src="kask malgosia.jpg" alt="Małgosia 1">
    <img src="malgosia 2.jpg" alt="Małgosia 2">
    <img src="malgosia 3.jpg" alt="Małgosia 3">
    <img src="malowanie.jpg" alt="Malowanie">
    <img src="stunt duke.jpg" alt="Stunt">
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
  <img src="" alt="powiększone zdjęcie" />
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

  const lightbox = document.getElementById('lightbox');
  const lightboxImg = lightbox.querySelector('img');
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

