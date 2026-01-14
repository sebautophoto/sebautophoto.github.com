<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sébastien – Photographe Automobile</title>

  <style>
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      color: #f2f2f2;
      background-color: #111;
    }

    nav {
      position: fixed;
      top:0;
      width:100%;
      background: rgba(0,0,0,0.85);
      text-align:center;
      padding:15px 0;
      z-index: 10;
    }

    nav a {
      color:#fff;
      margin:0 15px;
      text-decoration:none;
      font-weight:bold;
    }

    header {
      height: 100vh;
      background: url('background.jpg') center/cover no-repeat;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 20px;
    }

    header h1 {
      font-size: 3rem;
      margin-bottom: 10px;
    }

    header p {
      max-width: 700px;
      opacity: 0.9;
    }

    section {
      padding:80px 10%;
    }

    h2 {
      font-size:2rem;
      margin-bottom:40px;
      border-left:4px solid #e10600;
      padding-left:15px;
    }

    .gallery {
      display:grid;
      grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
      gap:15px;
    }

    .gallery img {
      width:100%;
      border-radius:6px;
      object-fit:cover;
    }

    #calendar iframe {
      display:block;
      margin: 0 auto;
    }

    #calendar h3 {
      font-size:1.4rem;
      margin-bottom:20px;
      border-left:4px solid #e10600;
      padding-left:12px;
    }

    footer {
      text-align:center;
      padding:30px;
      background:#000;
      font-size:0.9rem;
      opacity:0.7;
    }
  </style>
</head>

<body>

<nav>
  <a href="#accueil">Accueil</a>
  <a href="#apropos">À propos</a>
  <a href="#portfolio">Portfolio</a>
  <a href="#calendar">Réservations</a>
  <a href="#contact">Contact</a>
</nav>

<header id="accueil">
  <h1>Sébastien</h1>
  <p>
    Photographe automobile – Capturer la vitesse, la ligne et l’ambiance paddock.  
    Disponible pour collaborations et projets professionnels 2026.
  </p>
</header>

<section id="apropos">
  <h2>À propos</h2>
  <p>
    Passionné par l’automobile, je photographie la compétition, les véhicules et
    l’ambiance qui les entoure. Mon objectif : mettre en valeur l’action et
    l’esthétique de chaque scène.
  </p>
</section>

<section id="portfolio">
  <h2>Portfolio</h2>
  <div class="gallery">
    <img src="photo1.jpg" alt="Photo 1">
    <img src="photo2.jpg" alt="Photo 2">
    <img src="photo3.jpg" alt="Photo 3">
    <img src="photo4.jpg" alt="Photo 4">
    <img src="photo5.jpg" alt="Photo 5">
  </div>
</section>

<!-- SECTION RÉSERVATIONS INTÉGRÉE -->
<section id="calendar">
  <h2>Réservations</h2>

  <p style="max-width:800px; margin-bottom:30px;">
    Consulte les disponibilités ci-dessous.  
    Toute demande de réservation est soumise à validation manuelle.
  </p>

  <!-- CALENDRIER GOOGLE -->
  <iframe
    src="https://calendar.google.com/calendar/embed?src=TON_ID_CALENDRIER&ctz=Europe/Paris"
    style="border:0; width:100%; max-width:1000px; height:600px; border-radius:6px;"
    frameborder="0"
    scrolling="no">
  </iframe>

  <!-- FORMULAIRE GOOGLE -->
  <div style="margin-top:60px;">
    <h3>Demande de réservation</h3>

    <iframe
      src="https://docs.google.com/forms/d/e/TON_ID_FORMULAIRE/viewform?embedded=true"
      width="100%"
      height="900"
      frameborder="0"
      marginheight="0"
      marginwidth="0"
      style="background:#fff; border-radius:6px;">
      Chargement…
    </iframe>
  </div>
</section>

<section id="contact">
  <h2>Contact</h2>
  <p>Email : contact@sebastien-photo.fr</p>
  <p>Instagram : @sebastien.photo</p>
</section>

<footer>
  © 2026 – Sébastien | Photographe Automobile
</footer>

</body>
</html>
