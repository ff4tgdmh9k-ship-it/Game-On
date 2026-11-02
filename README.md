# Game-On
Tu veux t’améliorer rapidement sur fortnite roblox Magnicraft ou autre ? 
index.html 
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NEXPLAY - Gaming</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
  <a href="#" class="logo">NEX<span>PLAY</span></a>
  <nav>
    <a href="#accueil">Accueil</a>
    <a href="#actus">Actualités</a>
    <a href="#jeux">Jeux</a>
    <a href="#outils">Outils</a>
  </nav>
</header>

<section class="hero" id="accueil">
  <p class="tag">TON UNIVERS GAMING</p>
  <h1>JOUE.<br><span>PROGRESSE.</span><br>DOMINE.</h1>
  <p>Actualités, astuces et outils pour tous les passionnés de jeux vidéo.</p>
  <a href="#actus" class="btn">Découvrir le site →</a>
</section>

<section id="actus">
  <h2>ACTUALITÉS <span>GAMING</span></h2>
  <div class="cards">
    <article class="card">
      <div class="visual purple">F</div>
      <h3>Univers Fortnite</h3>
      <p>Retrouve des astuces et des guides pour progresser.</p>
    </article>
    <article class="card">
      <div class="visual red">R</div>
      <h3>Univers Roblox</h3>
      <p>Découvre des expériences et des conseils Roblox.</p>
    </article>
    <article class="card">
      <div class="visual blue">PC</div>
      <h3>PC Gaming</h3>
      <p>Conseils, réglages et performances pour ton PC.</p>
    </article>
  </div>
</section>

<section id="jeux">
  <h2>CHOISIS TON <span>JEU</span></h2>
  <div class="games">
    <a href="#actus">FORTNITE ↗</a>
    <a href="#actus">ROBLOX ↗</a>
    <a href="#actus">PC GAMING ↗</a>
  </div>
</section>

<section id="outils">
  <h2>OUTILS <span>GRATUITS</span></h2>
  <div class="tool">
    <h3>Générateur de pseudos</h3>
    <p id="pseudo">Ton prochain pseudo...</p>
    <button onclick="genererPseudo()">Générer un pseudo</button>
  </div>

  <div class="tool">
    <h3>Calculateur de ratio</h3>
    <input type="number" id="kills" placeholder="Éliminations">
    <input type="number" id="deaths" placeholder="Morts">
    <button onclick="calculerRatio()">Calculer</button>
    <p id="resultat">Ton ratio apparaîtra ici.</p>
  </div>
</section>

<footer>
  <h2>NEXPLAY</h2>
  <p>Ton univers gaming commence ici.</p>
  <p>© 2026 NEXPLAY</p>
</footer>

<script src="script.js"></script>
</body>
</html>

style.css 
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  background: #090b12;
  color: white;
  font-family: Arial, sans-serif;
}

header {
  height: 75px;
  padding: 0 8%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #101421;
  border-bottom: 1px solid #27243c;
}

.logo {
  font-size: 25px;
  font-weight: 900;
  color: white;
  text-decoration: none;
}

.logo span, h2 span {
  color: #a66aff;
}

nav {
  display: flex;
  gap: 25px;
}

nav a {
  color: #aaa;
  text-decoration: none;
  font-size: 14px;
}

nav a:hover {
  color: #a66aff;
}

.hero {
  min-height: 520px;
  padding: 110px 10%;
  background: radial-gradient(circle at 80%, #322052, #090b12 60%);
}

.tag {
  color: #b78aff;
  letter-spacing: 3px;
  font-size: 12px;
}

.hero h1 {
  font-size: clamp(55px, 8vw, 95px);
  font-weight: 900;
  margin: 20px 0;
}

.hero h1 span {
  color: #a66aff;
}

.hero p {
  color: #aaa;
  margin-bottom: 25px;
  line-height: 1.6;
}

.btn {
  display: inline-block;
  padding: 15px 25px;
  background: #9054e8;
  color: white;
  text-decoration: none;
  font-weight: bold;
  border-radius: 5px;
}

section:not(.hero) {
  padding: 85px 10%;
}

h2 {
  font-size: 35px;
  margin-bottom: 35px;
}

.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.card, .tool {
  background: #141a28;
  padding: 25px;
  border: 1px solid #282e40;
  border-radius: 8px;
}

.card:hover, .tool:hover {
  border-color: #a66aff;
  transform: translateY(-4px);
  transition: .2s;
}

.visual {
  height: 130px;
  display: grid;
  place-items: center;
  font-size: 65px;
  font-weight: 900;
  margin-bottom: 20px;
  border-radius: 5px;
}

.purple { background: #33204f; color: #c4a0ff; }
.red { background: #451e2e; color: #ff819e; }
.blue { background: #142f4a; color: #66bdff; }

.card p, .tool p {
  color: #aaa;
  margin-top: 12px;
  line-height: 1.5;
}

.games {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
}

.games a {
  padding: 40px 20px;
  background: #171d2b;
  color: white;
  text-decoration: none;
  font-weight: bold;
  text-align: center;
  border: 1px solid #343047;
}

.games a:hover {
  background: #372253;
}

.tool {
  margin-bottom: 20px;
}

.tool h3 {
  margin-bottom: 15px;
}

input {
  background: #090e19;
  border: 1px solid #45405c;
  padding: 12px;
  color: white;
  margin: 5px;
  width: 140px;
}

button {
  background: #9054e8;
  border: none;
  padding: 12px 18px;
  color: white;
  cursor: pointer;
  font-weight: bold;
  border-radius: 4px;
}

button:hover, .btn:hover {
  background: #713bc0;
}

footer {
  text-align: center;
  padding: 40px;
  background: #101421;
  color: #aaa;
  line-height: 2;
}

@media(max-width: 700px) {
  header {
    height: auto;
    padding: 20px;
    flex-direction: column;
    gap: 20px;
  }

  nav {
    gap: 13px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .cards, .games {
    grid-template-columns: 1fr;
  }

  .hero {
    padding: 90px 7%;
  }

  section:not(.hero) {
    padding: 60px 7%;
  }
}
y
script.js 
function genererPseudo() {
  const debut = [
    "Shadow", "Nova", "Pixel",
    "Turbo", "Ghost", "Blaze",
    "Dark", "Hyper", "Frost"
  ];

  const fin = [
    "Fox", "Storm", "X",
    "Wolf", "Rush", "Legend",
    "Fire", "Pro", "Gaming"
  ];

  const a = debut[Math.floor(Math.random() * debut.length)];
  const b = fin[Math.floor(Math.random() * fin.length)];
  const nombre = Math.floor(Math.random() * 99);

  document.getElementById("pseudo").textContent =
    a + b + nombre;
}

function calculerRatio() {
  const kills = Number(document.getElementById("kills").value);
  const deaths = Number(document.getElementById("deaths").value);

  if (kills < 0 || deaths < 0 ||
      document.getElementById("kills").value === "" ||
      document.getElementById("deaths").value === "") {
    document.getElementById("resultat").textContent =
      "Entre deux nombres positifs.";
    return;
  }

  const ratio = deaths === 0
    ? (kills === 0 ? "0.00" : "∞")
    : (kills / deaths).toFixed(2);

  document.getElementById("resultat").textContent =
    "Ton ratio : " + ratio;
}
