<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio Piotra K</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      background-color: #f0f0f0;
      color: #333;
    }

    header {
      background-color: #1e1e1e;
      color: white;
      padding: 40px 20px;
      text-align: center;
    }

    nav {
      background-color: #2c2c2c;
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
      border-bottom: 2px solid #f39c12;
    }

    .category-section {
      display: none;
      padding: 30px 20px;
    }

    .category-section.active {
      display: block;
    }

    .category-section h2 {
      margin-bottom: 20px;
      border-left: 6px solid #f39c12;
      padding-left: 10px;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 15px;
    }

    .gallery img {
      width: 100%;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    .divider {
      margin: 40px 0;
      border: none;
      border-top: 2px dashed #aaa;
    }

    #o-mnie, #kontakt {
      background-color: #ffffff;
      padding: 40px 20px;
      margin-top: 20px;
      border-top: 4px solid #f39c12;
    }

    #o-mnie h2, #kontakt h2 {
      margin-top: 0;
      color: #1e1e1e;
    }

    #kontakt a {
      color: #f39c12;
      text-decoration: none;
    }

    #kontakt a:hover {
      text-decoration: underline;
    }

    footer {
      text-align: center;
      padding: 20px;
      background-color: #1e1e1e;
      color: white;
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
  <div class="gallery">
    <img src="supra 1.jpg" alt="Auto 1">
    <img src="supra 2.jpg" alt="Auto 2">
    <img src="supra 3.jpg" alt="Auto 3">
    <img src="supra 6.jpg" alt="Auto 4">
    <img src="supra 5.jpg" alt="Auto 5">
    <img src="supra 4.jpg" alt="Auto 6">
     </div>
  <hr class="divider">
  <div class="gallery">
    <img src="gren 1.jpg" alt="Auto 7">
    <img src="gren%206.jpg" alt="Auto 8">
    <img src="gren 3.jpg" alt="Auto 9">
    <img src="gren 4.jpg" alt="Auto 10">
    <img src="gren 5.jpg" alt="Auto 11">
    <img src="gren%202.jpg" alt="Auto 12">
  </div>
  <hr class="divider">
  <div class="gallery">
    <img src="kamil 1.jpg" alt="Auto 13">
    <img src="kamil 2.jpg" alt="Auto 14">
    <img src="kamil 3.jpg" alt="Auto 15">
    <img src="gabi 1.jpg" alt="Auto 16">
    <img src="gabi 2.jpg" alt="Auto 17">
    <img src="gabi 3.jpg" alt="Auto 18">
    <img src="gabi 4.jpg" alt="Auto 19">
    <img src="gabi 5.jpg" alt="Auto 20">
    <img src="gabi 6.jpg" alt="Auto 21">
    
  </div>
  
</section>

<section id="ludzie" class="category-section">
  <h2>Portrety Ludzi</h2>
  <div class="gallery">
    <img src="natalia 1.jpg" alt="Portret 1">
    <img src="natalia 2.jpg" alt="Portret 2">
    <img src="natalia 6.jpg" alt="Portret 3">
    <img src="natalia 4.jpg" alt="Portret 4">
    <img src="natalia 5.jpg" alt="Portret 5">
    <img src="natalia%208.jpg" alt="Portret 6">
  </div>
  
  </div>
  <hr class="divider">
  <div class="gallery">
    <img src="ruda.jpg" alt="Portret 11">
    <img src="ruda%202.jpg" alt="Portret 12">
   <img src="ruda%203.jpg" alt="Portret 13">
    <img src="ruda%204.jpg" alt="Portret 14">
    <img src="ruda%205.jpg" alt="Portret 15">
    <img src="rada1.jpg" alt="Portret 16">
    
    
    
    
  </div>
  
</section>

<section id="motory" class="category-section">
  <h2>Motocykle</h2>
  <div class="gallery">
    <img src="grzesiu 1.jpg" alt="Motor 1">
    <img src="kask malgosia.jpg" alt="Motor 2">
    <img src="malgosia%202.jpg" alt="Motor 3">
    <img src="malgosia%203.jpg" alt="Motor 4">
    <img src="malowanie.jpg" alt="Motor 5">
    <img src="stunt duke.jpg" alt="Motor 6">
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

<script>
  function showSection(id) {
    const sections = document.querySelectorAll('.category-section');
    const buttons = document.querySelectorAll('nav button');

    sections.forEach(section => section.classList.remove('active'));
    buttons.forEach(btn => btn.classList.remove('active-tab'));

    document.getElementById(id).classList.add('active');
    event.target.classList.add('active-tab');
  }
</script>

</body>
</html>

