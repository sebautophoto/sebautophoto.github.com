<!DOCTYPE html><html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sebix – Photographe Automobile</title>
  <meta name="description" content="Photographe automobile – action, paddock, esthétique. Disponible pour collaborations 2026." />
  <style>
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background-color: #0f0f0f;
      color: #f2f2f2;
    }
    header {
      height: 100vh;
      background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('hero.jpg') center/cover no-repeat;
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
      letter-spacing: 2px;
    }
    header p {
      max-width: 700px;
      font-size: 1.1rem;
      opacity: 0.9;
    }
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(0,0,0,0.85);
      padding: 15px 0;
      text-align: center;
      z-index: 10;
    }
    nav a {
      color: #ffffff;
      text-decoration: none;
      margin: 0 15px;
      font-weight: bold;
      letter-spacing: 1px;
    }
    section {
      padding: 80px 10%;
    }
    h2 {
      font-size: 2rem;
      margin-bottom: 40px;
      border-left: 4px solid #e10600;
      padding-left: 15px;
    }
    .about {
      max-width: 800px;
      line-height: 1.7;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 15px;
    }
    .gallery img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 6px;
    }
    .contact {
      max-width: 600px;
    }
    .contact p {
      margin-bottom: 10px;
    }
    footer {
      text-align: center;
      padding: 30px;
      background: #000000;
      font-size: 0.9rem;
      opacity: 0.7;
    }
    @media (max-width: 768px) {
      header h1 {
        font-size: 2.2rem;
      }
      section {
        padding: 60px 8%;
      }
    }
  </style>
</head>
<body>  <nav>
    <a href="#accueil">Accueil</a>
    <a href="#apropos">À propos</a>
    <a href="#portfolio">Portfolio</a>
    <a href="#contact">Contact</a>
  </nav>  <header id="accueil">
    <h1>Sebix</h1>
    <p>Photographe automobile – Action, esthétique et ambiance paddock. Disponible pour collaborations et projets professionnels à partir de 2026.</p>
  </header>  <section id="apropos">
    <h2>À propos</h2>
    <div class="about">
      <p>Passionné par l’automobile et la compétition, je pratique la photographie automobile avec l’objectif de capturer la vitesse, les lignes et l’émotion qui entourent chaque véhicule et chaque événement.</p>
      <p>Après plusieurs projets personnels et des retours positifs sur mon travail, je souhaite aujourd’hui me professionnaliser et proposer mes services aux teams, préparateurs et acteurs du sport automobile.</p>
    </div>
  </section>  <section id="portfolio">
    <h2>Portfolio
