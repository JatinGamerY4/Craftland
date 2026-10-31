<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#070914">
<title>JATINGAMERY4 | Craftland Creator Hub</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;600;700;800&family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #070914;
  --cyan: #00eaff;
  --purple: #a855f7;
  --text: #f4f7ff;
  --muted: #929bb5;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  background: var(--bg);
  color: var(--text);
  font-family: 'Inter', sans-serif;
  overflow-x: hidden;
  min-height: 100vh;
}

body::before {
  content: "";
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: -1;
  background:
    radial-gradient(ellipse at 15% 10%, #172d5b55, transparent 40%),
    radial-gradient(ellipse at 90% 35%, #6d28d933, transparent 38%),
    radial-gradient(ellipse at 50% 100%, #003d5540, transparent 45%);
}

body::after {
  content: "";
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: -1;
  opacity: .12;
  background-image: radial-gradient(#8ca8ff 0.7px, transparent 0.7px);
  background-size: 28px 28px;
}

/* CURSOR GLOW */

#cursor-glow {
  position: fixed;
  width: 220px;
  height: 220px;
  border-radius: 50%;
  pointer-events: none;
  z-index: 9999;
  background: radial-gradient(circle,
    #00eaff22 0%,
    #536dff12 40%,
    transparent 70%);
  transform: translate(-50%, -50%);
  display: none;
}

@media (hover: hover) and (pointer: fine) {
  #cursor-glow {
    display: block;
  }
}

/* NAVIGATION */

.navbar {
  max-width: 1250px;
  width: calc(100% - 40px);
  margin: 24px auto 0;
  padding: 13px 18px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 15px;
  background: #101426c9;
  border: 1px solid #ffffff17;
  border-radius: 16px;
  backdrop-filter: blur(18px);
  box-shadow: 0 8px 35px #0005;
}

.logo {
  font-family: 'Orbitron', sans-serif;
  font-weight: 800;
  font-size: 17px;
  letter-spacing: 1px;
}

.logo span {
  color: var(--cyan);
  text-shadow: 0 0 15px #00eaff88;
}

.nav-buttons {
  display: flex;
  gap: 10px;
}

.nav-btn {
  text-decoration: none;
  color: #dce7ff;
  padding: 11px 22px;
  border-radius: 10px;
  border: 1px solid #ffffff19;
  background: #ffffff08;
  font-size: 12px;
  font-weight: 800;
  letter-spacing: 1px;
  transition: .3s;
}

.nav-btn:hover {
  color: white;
  border-color: var(--cyan);
  background: #00eaff14;
  box-shadow: 0 0 18px #00eaff35;
  transform: translateY(-2px);
}

/* HERO */

.hero {
  max-width: 1100px;
  margin: 95px auto 75px;
  padding: 0 20px;
  text-align: center;
}

.hero-label {
  display: inline-block;
  padding: 9px 18px;
  border-radius: 30px;
  border: 1px solid #00eaff55;
  color: var(--cyan);
  background: #00eaff0c;
  font-size: 11px;
  font-weight: 800;
  letter-spacing: 2px;
  box-shadow: 0 0 20px #00eaff15;
}

.hero h1 {
  font-family: 'Orbitron', sans-serif;
  font-size: clamp(35px, 7vw, 76px);
  font-weight: 800;
  margin-top: 25px;
  letter-spacing: 2px;
  line-height: 1.2;
  background: linear-gradient(100deg, #ffffff, #00eaff, #a855f7);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  filter: drop-shadow(0 0 20px #00eaff20);
}

.hero p {
  max-width: 600px;
  margin: 20px auto 0;
  color: var(--muted);
  font-size: 15px;
  line-height: 1.8;
}

.hero-line {
  width: 100px;
  height: 3px;
  margin: 30px auto 0;
  border-radius: 5px;
  background: linear-gradient(90deg, var(--cyan), var(--purple));
  box-shadow: 0 0 15px var(--cyan);
}

/* SOCIAL BUTTONS */

.social-row {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 14px;
  margin-top: 35px;
}

.social-btn {
  text-decoration: none;
  padding: 14px 25px;
  border-radius: 11px;
  color: white;
  font-size: 12px;
  font-weight: 800;
  letter-spacing: .5px;
  transition: .3s;
  border: 1px solid #ffffff20;
}

.instagram {
  background: linear-gradient(110deg, #833ab4, #fd1d1d, #fcb045);
}

.discord {
  background: linear-gradient(110deg, #4752c4, #7289ff);
}

.email {
  background: linear-gradient(110deg, #075c82, #007f9d);
}

.social-btn:hover {
  transform: translateY(-4px) scale(1.03);
  filter: brightness(1.2);
}

/* VIDEO SECTION */

.content {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 20px 70px;
}

.section-heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 15px;
  margin-bottom: 25px;
}

.section-heading h2 {
  font-family: 'Orbitron', sans-serif;
  font-size: clamp(18px, 3vw, 25px);
  letter-spacing: 1px;
}

.section-heading h2 span {
  color: var(--cyan);
}

.section-heading p {
  color: var(--muted);
  font-size: 11px;
  letter-spacing: 1px;
}

.playlist-shell {
  width: 100%;
  padding: 12px;
  border-radius: 18px;
  background: linear-gradient(135deg, #101b35, #17102b);
  border: 1px solid #00eaff55;
  box-shadow: 0 0 30px #00eaff12;
  overflow: hidden;
}

#playlist-player {
  width: 100%;
  aspect-ratio: 16 / 9;
  border-radius: 12px;
  overflow: hidden;
  background: #080b17;
}

#playlist-player iframe {
  width: 100%;
  height: 100%;
  border: 0;
}

/* LOADING */

.loading-text {
  text-align: center;
  color: var(--cyan);
  padding: 35px 10px;
  font-size: 13px;
  letter-spacing: 1px;
}

.loading-dot {
  display: inline-block;
  animation: blink 1s infinite;
}

@keyframes blink {
  50% { opacity: .3; }
}

/* FOOTER */

footer {
  border-top: 1px solid #ffffff12;
  padding: 30px 20px;
  text-align: center;
  background: #080b17;
}

footer h3 {
  font-family: 'Orbitron', sans-serif;
  font-size: 17px;
  letter-spacing: 2px;
}

footer h3 span {
  color: var(--cyan);
}

footer p {
  margin-top: 12px;
  color: var(--muted);
  font-size: 11px;
  line-height: 1.8;
}

footer a {
  color: var(--cyan);
  text-decoration: none;
}

/* MOBILE */

@media (max-width: 600px) {

  .navbar {
    flex-direction: column;
    padding: 17px 12px;
  }

  .logo {
    font-size: 16px;
  }

  .nav-buttons {
    width: 100%;
    gap: 7px;
  }

  .nav-btn {
    flex: 1;
    text-align: center;
    padding: 12px 5px;
    font-size: 10px;
  }

  .hero {
    margin: 65px auto 55px;
  }

  .hero p {
    font-size: 13px;
  }

  .social-row {
    gap: 9px;
  }

  .social-btn {
    padding: 13px 14px;
    font-size: 10px;
  }

  .section-heading {
    align-items: flex-start;
    flex-direction: column;
  }

  .playlist-shell {
    padding: 6px;
  }
}

</style>
</head>

<body>

<div id="cursor-glow"></div>

<!-- NAVIGATION -->

<nav class="navbar">

  <div class="logo">
    JATIN<span>GAMERY4</span>
  </div>

  <div class="nav-buttons">

    <a href="map.html" class="nav-btn">
      MAPS
    </a>

    <a href="https://0xme.github.io/ItemID2/?mode=2&page=1"
       target="_blank" rel="noopener" class="nav-btn">
      CODES
    </a>

    <a href="assets.html" class="nav-btn">
      ASSETS
    </a>

  </div>

</nav>

<!-- HERO -->

<section class="hero">

  <div class="hero-label">
    CRAFTLAND CREATOR HUB
  </div>

  <h1>JATINGAMERY4</h1>

  <p>
    Welcome to my official Craftland hub.
    Explore my latest tutorials, discover useful
    scripts, find maps and access Craftland resources
    all in one place.
  </p>

  <div class="hero-line"></div>

  <div class="social-row">

    <a class="social-btn instagram"
       href="https://www.instagram.com/jatingamery4/"
       target="_blank" rel="noopener">
       INSTAGRAM ↗
    </a>

    <a class="social-btn discord"
       href="https://discord.gg/QXuW5FtUbz"
       target="_blank" rel="noopener">
       JOIN DISCORD ↗
    </a>

    <a class="social-btn email"
       href="mailto:jatingamery411@gmail.com">
       CONTACT ME ↗
    </a>

  </div>

</section>

<!-- AUTOMATIC YOUTUBE PLAYLIST -->

<main class="content">

  <div class="section-heading">

    <h2>
      CRAFTLAND <span>VIDEOS</span>
    </h2>

    <p>
      MY YOUTUBE PLAYLIST
    </p>

  </div>

  <div class="playlist-shell">

    <div id="playlist-player">

      <div class="loading-text">
        LOADING VIDEOS
        <span class="loading-dot">...</span>
      </div>

    </div>

  </div>

</main>

<!-- FOOTER -->

<footer>

  <h3>
    JATIN<span>GAMERY4</span>
  </h3>

  <p>
    Craftland Tutorials · Maps · Scripts · Assets
    <br>

    Email:
    <a href="mailto:jatingamery411@gmail.com">
      jatingamery411@gmail.com
    </a>

    <br><br>

    © 2026 JATINGAMERY4. All Rights Reserved.

  </p>

</footer>

<script>

/* ======================================
   YOUTUBE AUTOMATIC PLAYLIST PLAYER
   ====================================== */

let playlistPlayer;

function onYouTubeIframeAPIReady() {

  playlistPlayer = new YT.Player("playlist-player", {

    width: "100%",
    height: "100%",

    playerVars: {

      listType: "playlist",

      list: "PLFI5jnn1AiNRahLYeGpvl9EpXfwlNOknC",

      playsinline: 1,

      rel: 0

    },

    events: {

      onReady: function(event) {

        event.target.setShuffle(true);

      },

      onError: function(event) {

        document.getElementById("playlist-player").innerHTML = `
          <div class="loading-text">
            Unable to load playlist.
            <br><br>
            <a href="https://www.youtube.com/playlist?list=PLFI5jnn1AiNRahLYeGpvl9EpXfwlNOknC"
               target="_blank"
               rel="noopener"
               style="color:#00eaff;">
               OPEN PLAYLIST ON YOUTUBE ↗
            </a>
          </div>
        `;

      }

    }

  });

}

/* LOAD YOUTUBE API */

const youtubeAPI = document.createElement("script");

youtubeAPI.src = "https://www.youtube.com/iframe_api";

document.head.appendChild(youtubeAPI);


/* ======================================
   SMOOTH CURSOR FOLLOWING GLOW
   ====================================== */

const glow = document.getElementById("cursor-glow");

let mouseX = 0;
let mouseY = 0;

let glowX = 0;
let glowY = 0;

document.addEventListener("mousemove", (e) => {

  mouseX = e.clientX;
  mouseY = e.clientY;

});

function animateGlow() {

  glowX += (mouseX - glowX) * 0.12;
  glowY += (mouseY - glowY) * 0.12;

  glow.style.left = glowX + "px";
  glow.style.top = glowY + "px";

  requestAnimationFrame(animateGlow);

}

animateGlow();

</script>

</body>
</html>
