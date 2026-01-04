
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sébastien – Photographe Automobile</title>
  <style>
    body {
      margin:0;
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
      z-index:10;
    }
    nav a { color:#fff; margin:0 15px; text-decoration:none; font-weight:bold; }
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
    header h1 { font-size: 3rem; margin-bottom: 10px; }
    header p { max-width: 700px; opacity: 0.9; }
    section { padding:80px 10%; }
    h2 { font-size:2rem; margin-bottom:40px; border-left:4px solid #e10600; padding-left:15px; }
    .gallery { display:grid; grid-template-columns: repeat(auto-fit, minmax(250px,1fr)); gap:15px; }
    .gallery img { width:100%; border-radius:6px; object-fit:cover; }
    .calendar { background:#222; padding:20px; border-radius:6px; max-width:400px; }
    .calendar input, .calendar button { padding:10px; margin:5px 0; width:100%; }
    footer { text-align:center; padding:30px; background:#000; font-size:0.9rem; opacity:0.7; }
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
  <p>Photographe automobile – Capturer la vitesse, la ligne et l’ambiance paddock. Disponible pour collaborations et projets professionnels 2026.</p>
</header>

<section id="apropos">
  <h2>À propos</h2>
  <p>Passionné par l’automobile, je photographie la compétition, les véhicules et l’ambiance qui les entoure. Mon objectif : mettre en valeur l’action et l’esthétique de chaque scène.</p>
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

<section id="calendar">
  <h2>Réservations</h2>
  <div class="calendar">
    <p>Choisissez votre créneau (minimum 2 jours) :</p>
    <label for="start">Date de début :</label>
    <input type="date" id="start">
    <label for="end">Date de fin :</label>
    <input type="date" id="end">
    <button onclick="requestBooking()">Demander réservation</button>
    <p id="message"></p>
  </div>
</section>

<section id="contact">
  <h2>Contact</h2>
  <p>Email : sebastienzozoferrer@gmail.com</p>
  <p>Instagram : @sebastien.photo</p>
</section>

<footer>
  © 2026 – Sébastien | Photographe Automobile
</footer>

<script>
function requestBooking() {
  const start = document.getElementById('start').value;
  const end = document.getElementById('end').value;
  const messageEl = document.getElementById('message');

  if(!start || !end){
    messageEl.innerText = "Veuillez sélectionner les deux dates.";
    return;
  }

  const startDate = new Date(start);
  const endDate = new Date(end);
  const diffTime = endDate - startDate;
  const diffDays = diffTime / (1000 * 60 * 60 * 24) + 1; // inclut le jour de début

  if(diffDays < 2){
    messageEl.innerText = "Vous devez sélectionner un minimum de 2 jours.";
    return;
  }

  const subject = encodeURIComponent("Demande réservation photo");
  const body = encodeURIComponent(`Bonjour Sébastien,\n\nJe souhaite réserver un créneau du ${start} au ${end}.\nMerci.\n\nCordialement.`);
  window.location.href = `mailto:sebastienzozoferrer@gmail.com?subject=${subject}&body=${body}`;
}
</script>

</body>
</html>
