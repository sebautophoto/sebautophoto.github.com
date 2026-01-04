<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sébastien – Photographe Automobile</title>
<style>
body {margin:0; font-family:Arial, Helvetica, sans-serif; color:#f2f2f2; background-color:#111;}
nav {position: fixed; top:0; width:100%; background: rgba(0,0,0,0.85); text-align:center; padding:15px 0; z-index:10;}
nav a {color:#fff; margin:0 15px; text-decoration:none; font-weight:bold;}
header {height:100vh; background: url('background.jpg') center/cover no-repeat; display:flex; flex-direction:column; justify-content:center; align-items:center; text-align:center; padding:20px;}
header h1 {font-size:3rem; margin-bottom:10px;}
header p {max-width:700px; opacity:0.9;}
section {padding:80px 10%;}
h2 {font-size:2rem; margin-bottom:40px; border-left:4px solid #e10600; padding-left:15px;}
.gallery {display:grid; grid-template-columns: repeat(auto-fit, minmax(250px,1fr)); gap:15px;}
.gallery img {width:100%; border-radius:6px; object-fit:cover;}
.calendar {background:#222; padding:20px; border-radius:6px; max-width:500px;}
.calendar label, .calendar input, .calendar button {display:block; width:100%; margin:5px 0; padding:10px;}
.reservation-list {margin-top:20px; background:#333; padding:15px; border-radius:6px; max-height:400px; overflow-y:auto;}
.reservation-item {border-bottom:1px solid #555; padding:5px 0; display:flex; justify-content:space-between; align-items:center;}
.reservation-text {flex:1;}
.reservation-buttons button {margin-left:5px; padding:5px 10px;}
footer {text-align:center; padding:30px; background:#000; font-size:0.9rem; opacity:0.7;}
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
<p>Choisissez votre créneau et indiquez le lieu et l'événement :</p>

<label for="start">Date de début :</label>
<input type="date" id="start">

<label for="end">Date de fin :</label>
<input type="date" id="end">

<label for="location">Lieu :</label>
<input type="text" id="location" placeholder="Ex : Circuit de Nogaro">

<label for="event">Événement :</label>
<input type="text" id="event" placeholder="Ex : Course, shooting voiture">

<button onclick="requestBooking()">Réserver</button>
<p id="message"></p>

<div class="reservation-list" id="reservationList">
<strong>Historique des réservations :</strong>
</div>
</div>
</section>

<section id="contact">
<h2>Contact</h2>
<p>Email : sebastienzozoferrer@gmail.com</p>
<p>Instagram : Seb_autophoto</p>
</section>

<footer>
© 2026 – Sébastien | Photographe Automobile
</footer>

<script>
function getReservations(){ return JSON.parse(localStorage.getItem('reservations')) || []; }
function saveReservations(reservations){ localStorage.setItem('reservations', JSON.stringify(reservations)); }

function requestBooking(){
  const start = document.getElementById('start').value;
  const end = document.getElementById('end').value;
  const location = document.getElementById('location').value.trim();
  const event = document.getElementById('event').value.trim();
  const messageEl = document.getElementById('message');

  if(!start || !end || !location || !event){
    messageEl.innerText = "Veuillez remplir toutes les informations.";
    return;
  }

  let reservations = getReservations();
  reservations.push({start, end, location, event, status:"En attente"});
  saveReservations(reservations);

  const subject = encodeURIComponent("Demande réservation photo");
  const body = encodeURIComponent(
    `Bonjour Sébastien,\n\nJe souhaite réserver un créneau du ${start} au ${end}.\nLieu : ${location}\nÉvénement : ${event}\n\nMerci.\n\nCordialement.`
  );
  window.location.href = `mailto:sebastienzozoferrer@gmail.com?subject=${subject}&body=${body}`;

  renderReservations();
  messageEl.innerText = "Réservation enregistrée et mail préparé.";
}

function renderReservations(){
  const reservationList = document.getElementById('reservationList');
  let reservations = getReservations();
  reservationList.innerHTML = "<strong>Historique des réservations :</strong>";
  
  reservations.forEach((r,index)=>{
    const div = document.createElement('div');
    div.className = 'reservation-item';
    
    const textDiv = document.createElement('div');
    textDiv.className = 'reservation-text';
    textDiv.innerText = `${r.start} → ${r.end} | ${r.location} | ${r.event} | Statut : ${r.status}`;
    
    const btnDiv = document.createElement('div');
    btnDiv.className = 'reservation-buttons';
    
    const approveBtn = document.createElement('button');
    approveBtn.innerText = "✅ Approuver";
    approveBtn.onclick = () => { updateStatus(index,"Approuvé"); };
    
    const rejectBtn = document.createElement('button');
    rejectBtn.innerText = "❌ Refuser";
    rejectBtn.onclick = () => { updateStatus(index,"Refusé"); };
    
    btnDiv.appendChild(approveBtn);
    btnDiv.appendChild(rejectBtn);
    
    div.appendChild(textDiv);
    div.appendChild(btnDiv);
    reservationList.appendChild(div);
  });
}

function updateStatus(index, status){
  let reservations = getReservations();
  reservations[index].status = status;
  saveReservations(reservations);
  renderReservations();
}

// Initialisation
renderReservations();
</script>

</body>
</html>
