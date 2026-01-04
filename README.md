<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sébastien Zozoferrer - Photographe Auto</title>

    <!-- CSS -->
    <link rel="stylesheet" href="style.css">

    <!-- FullCalendar pour calendrier interactif -->
    <link href="https://cdn.jsdelivr.net/npm/fullcalendar@6.1.8/index.global.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/fullcalendar@6.1.8/index.global.min.js"></script>

    <!-- Lightbox (GLightbox) -->
    <link href="https://cdn.jsdelivr.net/npm/glightbox/dist/css/glightbox.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/glightbox/dist/js/glightbox.min.js"></script>
</head>
<body>
    <!-- Menu -->
    <header>
        <nav>
            <ul>
                <li><a href="#home">Accueil</a></li>
                <li><a href="#about">À propos</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#gallery">Galerie</a></li>
                <li><a href="#booking">Réservation</a></li>
                <li><a href="#testimonials">Témoignages</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#instagram">Instagram</a></li>
            </ul>
        </nav>
    </header>

    <!-- Accueil -->
    <section id="home" class="hero">
        <h1>Sébastien Zozoferrer</h1>
        <p>Photographe automobile passionné. Capturer la beauté et la puissance de chaque véhicule.</p>
    </section>

    <!-- À propos -->
    <section id="about">
        <h2>À propos de moi</h2>
        <p>Je suis Sébastien, photographe automobile depuis plus de 10 ans. Mon objectif est de sublimer chaque véhicule, qu'il s'agisse de voitures de collection, de sportives ou de créations uniques. Je travaille sur différents événements, circuits et shooting privés.</p>
    </section>

    <!-- Services -->
    <section id="services">
        <h2>Services</h2>
        <ul class="services-list">
            <li>Shooting photo sur circuits</li>
            <li>Shooting extérieur personnalisé</li>
            <li>Retouche professionnelle des photos</li>
            <li>Couverture d’événements automobiles</li>
            <li>Galerie et impressions pour les clients</li>
        </ul>
    </section>

    <!-- Galerie -->
    <section id="gallery">
        <h2>Galerie</h2>
        <div class="photo-grid">
            <a href="images/photo1.jpg" class="glightbox"><img src="images/photo1.jpg" alt="Photo 1"></a>
            <a href="images/photo2.jpg" class="glightbox"><img src="images/photo2.jpg" alt="Photo 2"></a>
            <a href="images/photo3.jpg" class="glightbox"><img src="images/photo3.jpg" alt="Photo 3"></a>
            <a href="images/photo4.jpg" class="glightbox"><img src="images/photo4.jpg" alt="Photo 4"></a>
            <a href="images/photo5.jpg" class="glightbox"><img src="images/photo5.jpg" alt="Photo 5"></a>
        </div>
    </section>

    <!-- Réservation -->
    <section id="booking">
        <h2>Réservation</h2>
        <div class="booking-container">
            <div id="calendar"></div>
            <form id="bookingForm">
                <label for="name">Nom :</label>
                <input type="text" id="name" name="name" required>

                <label for="email">Email :</label>
                <input type="email" id="email" name="email" required>

                <label for="eventLocation">Lieu et Événement :</label>
                <input type="text" id="eventLocation" name="eventLocation" placeholder="Ex: Circuit de Nogaro, Drift Day" required>

                <label for="timeSlot">Créneau :</label>
                <select id="timeSlot" name="timeSlot" required>
                    <option value="10:00-12:00">10:00 - 12:00</option>
                    <option value="12:00-14:00">12:00 - 14:00</option>
                    <option value="14:00-16:00">14:00 - 16:00</option>
                    <option value="16:00-18:00">16:00 - 18:00</option>
                </select>

                <button type="submit">Envoyer la réservation</button>
            </form>
        </div>
        <p id="bookingMessage"></p>
    </section>

    <!-- Témoignages -->
    <section id="testimonials">
        <h2>Témoignages</h2>
        <div class="testimonial">
            <p>"Super photographe, vraiment professionnel et créatif!"</p>
            <span>- Client heureux</span>
        </div>
        <div class="testimonial">
            <p>"Les photos de ma voiture sont incroyables, je recommande fortement!"</p>
            <span>- Passionné auto</span>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact">
        <h2>Contact</h2>
        <p>Email : <a href="mailto:sebastienzozoferrer@gmail.com">sebastienzozoferrer@gmail.com</a></p>
    </section>

    <!-- Instagram -->
    <section id="instagram">
        <h2>Instagram</h2>
        <p>Suivez-moi : <a href="https://www.instagram.com/seb-autophoto/" target="_blank">@seb-autophoto</a></p>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Sébastien Zozoferrer. Tous droits réservés.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
