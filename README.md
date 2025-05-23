<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>YoungWork SARL - Accueil</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0; padding: 0;
      background-color: #f4f4f4;
      color: #333;
    }
    header {
      background-color: #004d99;
      color: white;
      padding: 20px;
      text-align: center;
      animation: logoBounce 2s infinite;
    }
    @keyframes logoBounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    nav {
      display: flex;
      justify-content: center;
      background-color: #0073e6;
      padding: 10px;
    }
    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
    }
    nav a:hover {
      text-decoration: underline;
    }
    .language-selector {
      text-align: center;
      margin: 10px;
    }
    button.lang-btn {
      margin: 0 5px;
      padding: 5px 10px;
      background-color: #0073e6;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button.lang-btn:hover {
      background-color: #005bb5;
    }
    .section {
      padding: 40px 20px;
      max-width: 900px;
      margin: 20px auto;
      background-color: white;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    footer {
      background-color: #004d99;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 20px;
    }
    form {
      max-width: 400px;
      margin: 20px auto 0;
      background: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    input, textarea {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border-radius: 5px;
      border: 1px solid #ccc;
      font-size: 16px;
      box-sizing: border-box;
    }
    form button {
      background-color: #28a745;
      color: white;
      border: none;
      padding: 12px;
      width: 100%;
      border-radius: 5px;
      font-size: 18px;
      cursor: pointer;
    }
    form button:hover {
      background-color: #218838;
    }
  </style>
</head>
<body>

  <header>
    <h1>YoungWork SARL</h1>
    <p>Construisons Demain, Naturellement.</p>
  </header>

  <div class="language-selector">
    <button class="lang-btn" onclick="changeLanguage('fr')">Français</button>
    <button class="lang-btn" onclick="changeLanguage('ar')">العربية</button>
    <button class="lang-btn" onclick="changeLanguage('ber')">ⴰⵎⴰⵣⵉⵖ</button>
  </div>

  <nav>
    <a href="#">Accueil</a>
    <a href="#">À propos</a>
    <a href="#">Nos Services</a>
    <a href="#">Nos Réalisations</a>
    <a href="#contactSection">Contactez-nous</a>
  </nav>

  <section class="section">
    <h2>À propos</h2>
    <p id="aboutText">YoungWork SARL est une entreprise dynamique et innovante opérant dans plusieurs secteurs stratégiques...</p>
  </section>

  <section class="section" id="contactSection">
    <h2 id="contactTitle">Contactez-nous</h2>
    <p>MEARADI Fakhreddine - Téléphone: +212 666 257 924</p>
    <p>RAQI Mouhcine - Téléphone: +212 603 052 072</p>
    <p>MAACH Mouhcine - Téléphone: +212 624 438 135</p>
    <p>GRAIDI Mohammed - Téléphone: +212 641 681 312</p>

    <form action="https://formspree.io/f/xovdbaen" method="POST">
      <input type="email" name="email" placeholder="Votre email" required />
      <textarea name="message" placeholder="Votre message" rows="5" required></textarea>
      <button type="submit">Envoyer</button>
    </form>
  </section>

  <footer>
    © 2025 YoungWork SARL - Tous droits réservés
  </footer>

  <script>
    const texts = {
      fr: {
        about: "YoungWork SARL est une entreprise dynamique et innovante opérant dans plusieurs secteurs stratégiques...",
        contact: "Contactez-nous",
      },
      ar: {
        about: "YoungWork SARL هي شركة ديناميكية ومبتكرة تنشط في عدة مجالات استراتيجية...",
        contact: "اتصل بنا",
      },
      ber: {
        about: "YoungWork SARL d yan taddart n tsnaḍfi deg kra n yimanen imudan...",
        contact: "ⴰⴷⴷⴰⵔⴰⵏ ⵏⵓ",
      },
    };

    function changeLanguage(lang) {
      document.getElementById("aboutText").innerText = texts[lang].about;
      document.getElementById("contactTitle").innerText = texts[lang].contact;
    }
  </script>

</body>
</html>
