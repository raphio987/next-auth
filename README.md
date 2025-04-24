<!DOCTYPE html><html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>UC PlayStation - Gagne des UC Gratuitement</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: #0f0f0f;
      color: #ffffff;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    header {
      background: linear-gradient(to right, #1e1e2f, #29294d);
      width: 100%;
      padding: 20px;
      text-align: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }
    h1 {
      margin: 0;
      font-size: 2rem;
    }
    .cta, .form-section {
      margin: 30px auto;
      padding: 20px;
      max-width: 90%;
      background: #1a1a2e;
      border-radius: 15px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.5);
      text-align: center;
    }
    .cta p {
      font-size: 1.1rem;
    }
    .cta a {
      display: inline-block;
      margin-top: 15px;
      padding: 10px 20px;
      background-color: #04d9ff;
      color: #000;
      font-weight: bold;
      border-radius: 8px;
      text-decoration: none;
      transition: background 0.3s;
    }
    .cta a:hover {
      background-color: #00b3cc;
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 10px;
      margin-top: 15px;
    }
    input, textarea, button {
      padding: 10px;
      border-radius: 8px;
      border: none;
      font-size: 1rem;
    }
    button {
      background-color: #04d9ff;
      color: #000;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s;
    }
    button:hover {
      background-color: #00b3cc;
    }
    #confirmation {
      color: #00ffcc;
      font-weight: bold;
    }
    footer {
      margin-top: 40px;
      padding: 15px;
      font-size: 0.9rem;
      color: #aaa;
    }
  </style>
</head>
<body>
  <header>
    <h1>UC PlayStation</h1>
    <p>Gagne des UC facilement et gratuitement !</p>
  </header>  <div class="cta">
    <p>Complète des missions simples (pubs, apps, sondages) et gagne des UC chaque semaine.</p>
    <a href="#formulaire">Commencer maintenant</a>
  </div>  <div class="form-section" id="formulaire">
    <h2>Formulaire de Demande UC</h2>
    <form id="uc-form">
      <input type="text" name="pseudo" placeholder="Ton pseudo PUBG Mobile" required>
      <input type="email" name="email" placeholder="Ton email (pour confirmation)" required>
      <textarea name="message" rows="4" placeholder="Explique comment tu as complété les missions."></textarea>
      <button type="submit">Envoyer ma demande</button>
      <p id="confirmation" style="display:none; margin-top:10px;">Demande envoyée avec succès !</p>
    </form>
  </div>  <footer>
    &copy; 2025 UC PlayStation. Site non affilié à PUBG ou Tencent.
  </footer>  <script>
  document.getElementById('uc-form').addEventListener('submit', function(e) {
    e.preventDefault();
    const form = e.target;
    const data = {
      pseudo: form.pseudo.value,
      email: form.email.value,
      message: form.message.value
    };

    fetch("TON_URL_DÉPLOIEMENT_SCRIPT", {
      method: "POST",
      body: JSON.stringify(data),
      headers: {
        "Content-Type": "application/json"
      }
    }).then(res => {
      if(res.ok) {
        document.getElementById('confirmation').style.display = 'block';
        form.reset();
      }
    });
  });
  </script></body>
</html>