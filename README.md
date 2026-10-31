
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#070914">
<title>JATINGAMERY4 | Craftland Creator Hub</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@500;600;700;800&family=Inter:wght@400;500;600;700;800&display=swap');

:root {
  --bg: #070914;
  --panel: #101426;
  --cyan: #00eaff;
  --purple: #a855f7;
  --blue: #4169ff;
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

/* Background */

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

/* Mouse glow */

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
  transition: width .2s, height .2s;
  display: none;
}

/* Navigation */

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
  color: white;
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

/* Hero */

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

/* Social buttons */

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
  box-shadow: 0 5px 25px #e1306c20;
}

.discord {
  background: linear-gradient(110deg, #4752c4, #7289ff);
  box-shadow: 0 5px 25px #5865f230;
}

.email {
  background: linear-gradient(110deg, #075c82, #007f9d);
  box-shadow: 0 5px 25px #00eaff20;
}

.social-btn:hover {
  transform: translateY(-4px) scale(1.03);
  filter: brightness(1.2);
}

/* Video section */

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

.video-list {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.video-card {
  display: flex;
  align-items: center;
  gap: 22px;
  padding: 13px;
  background: linear-gradient(110deg, #141b31, #101426);
  border: 1px solid #ffffff12;
  border-radius: 15px;
  cursor: pointer;
  transition: .3s;
  position: relative;
  overflow: hidden;
}

.video-card::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 3px;
  height: 100%;
  background: linear-gradient(var(--cyan), var(--purple));
  opacity: .7;
}

.video-card:hover {
  transform: translateX(6px);
  border-color: #00eaff70;
  box-shadow: 0 5px 30px #00eaff12, inset 0 0 25px #00eaff05;
}

.thumbnail-wrap {
  position: relative;
  flex-shrink: 0;
  width: 190px;
  aspect-ratio: 16 / 9;
  overflow: hidden;
  border-radius: 10px;
  background: #202a40;
}

.thumbnail-wrap img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: .4s;
}

.video-card:hover img {
  transform: scale(1.07);
}

.play-icon {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 43px;
  height: 43px;
  display: grid;
  place-items: center;
  border-radius: 50%;
  background: #00dfffdb;
  color: #06121d;
  font-size: 18px;
  box-shadow: 0 0 25px #00eaff90;
  transition: .3s;
}

.video-card:hover .play-icon {
  transform: translate(-50%, -50%) scale(1.16);
  background: white;
}

.video-info {
  flex: 1;
  min-width: 0;
}

.video-number {
  color: var(--cyan);
  font-family: 'Orbitron', sans-serif;
  font-size: 10px;
  letter-spacing: 2px;
  margin-bottom: 9px;
}

.video-title {
  font-size: 16px;
  font-weight: 800;
  line-height: 1.5;
  color: #f5f7ff;
}

.video-subtitle {
  font-size: 11px;
  color: var(--muted);
  margin-top: 7px;
}

.watch-label {
  color: var(--cyan);
  font-size: 11px;
  font-weight: 800;
  letter-spacing: 1px;
  padding: 12px;
}

/* Video Modal */

.modal {
  display: none;
  position: fixed;
  inset: 0;
  z-index: 10000;
  background: #02040deF;
  backdrop-filter: blur(15px);
  justify-content: center;
  align-items: center;
  padding: 20px;
}

.modal.active {
  display: flex;
}

.modal-box {
  width: min(900px, 100%);
  background: #101426;
  border: 1px solid #00eaff55;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 0 60px #00eaff22;
}

.modal-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
  padding: 16px 20px;
}

.modal-title {
  font-weight: 800;
  font-size: 14px;
}

.close-btn {
  border: none;
  background: #ffffff12;
  color: white;
  font-size: 25px;
  width: 36px;
  height: 36px;
  border-radius: 9px;
  cursor: pointer;
}

.close-btn:hover {
  background: #ff3155;
}

.player {
  width: 100%;
  aspect-ratio: 16 / 9;
  border: none;
  display: block;
  background: black;
}

/* Footer */

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

/* Mobile */

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

  .video-card {
    gap: 12px;
    padding: 9px;
  }

  .thumbnail-wrap {
    width: 115px;
  }

  .video-title {
    font-size: 12px;
  }

  .video-number {
    font-size: 9px;
    margin-bottom: 5px;
  }

  .video-subtitle {
    font-size: 9px;
  }

  .watch-label {
    display: none;
  }

  .play-icon {
    width: 32px;
    height: 32px;
    font-size: 14px;
  }
}

@media (hover: hover) and (pointer: fine) {
  #cursor-glow {
    display: block;
  }
}
</style>
</head>

<body>

<div id="cursor-glow"></div>

<!-- NAVIGATION -->
<nav class="navbar">
  <div class="logo">JATIN<span>GAMERY4</span></div>

  <div class="nav-buttons">
    <a href="map.html" class="nav-btn">MAPS</a>
    <a href="https://0xme.github.io/ItemID2/?mode=2&page=1"
       target="_blank" rel="noopener" class="nav-btn">CODES</a>
    <a href="assets.html" class="nav-btn">ASSETS</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero">

  <div class="hero-label">CRAFTLAND CREATOR HUB</div>

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

<!-- VIDEOS -->
<main class="content">

  <div class="section-heading">
    <h2>FEATURED <span>VIDEOS</span></h2>
    <p>TOP 12 · CRAFTLAND TUTORIALS</p>
  </div>

  <div class="video-list" id="video-list"></div>

</main>

<!-- VIDEO PLAYER -->
<div class="modal" id="video-modal">
  <div class="modal-box">
    <div class="modal-top">
      <div class="modal-title" id="modal-title">Now Playing</div>
      <button class="close-btn" id="close-modal"
              aria-label="Close video">&times;</button>
    </div>

    <iframe
      class="player"
      id="video-player"
      src=""
      title="YouTube video player"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen>
    </iframe>
  </div>
</div>

<!-- FOOTER -->
<footer>
  <h3>JATIN<span>GAMERY4</span></h3>

  <p>
    Craftland Tutorials · Maps · Scripts · Assets
    <br>
    Email: <a href="mailto:jatingamery411@gmail.com">
      jatingamery411@gmail.com
    </a>
    <br><br>
    © 2026 JATINGAMERY4. All Rights Reserved.
  </p>
</footer>

<script>

/* =====================================
   ADD YOUR 12 VIDEOS HERE
   ===================================== */

const videos = [
  {
    id: "CnAU9C-dseg",
    title: "Heart Lives",
    subtitle: "Craftland Tutorial"
  },
  {
    id: "QfLS0kn8MWw",
    title: "Add Missions",
    subtitle: "Craftland Tutorial"
  },
  {
    id: "SYV8RvdVBnI",
    title: "Timer Script",
    subtitle: "Craftland Tutorial"
  },

  // Replace the next 9 entries with your videos.

  { id: "VIDEO_ID_4", title: "Your Video Title 04", subtitle: "Craftland Tutorial" },
  { id: "VIDEO_ID_5", title: "Your Video Title 05", subtitle: "Craftland Tutorial" },
  { id: "VIDEO_ID_6", title: "Your Video Title 06", subtitle: "Craftland Tutorial" },
  { id: "VIDEO_ID_7", title: "Your Video Title 07", subtitle: "Craftland Tutorial" },
  { id: "VIDEO_ID_8", title: "Your Video Title 08", subtitle: "Craftland Tutorial" },
  { id: "VIDEO_ID_9", title: "Your Video Title 09", subtitle: "Craftland Tutorial" },
  { id: "VIDEO_ID_10", title: "Your Video Title 10", subtitle: "Craftland Tutorial" },
  { id: "VIDEO_ID_11", title: "Your Video Title 11", subtitle: "Craftland Tutorial" },
  { id: "VIDEO_ID_12", title: "Your Video Title 12", subtitle: "Craftland Tutorial" }
];

/* CREATE VIDEO ROWS */

const videoList = document.getElementById("video-list");

videos.forEach((video, index) => {

  const card = document.createElement("div");
  card.className = "video-card";

  const thumb = document.createElement("div");
  thumb.className = "thumbnail-wrap";

  const img = document.createElement("img");
  img.src = `https://img.youtube.com/vi/${video.id}/hqdefault.jpg`;
  img.alt = video.title;
  img.loading = "lazy";

  const play = document.createElement("div");
  play.className = "play-icon";
  play.textContent = "▶";

  thumb.append(img, play);

  const info = document.createElement("div");
  info.className = "video-info";

  const number = document.createElement("div");
  number.className = "video-number";
  number.textContent = `VIDEO  ${String(index + 1).padStart(2, "0")}`;

  const title = document.createElement("div");
  title.className = "video-title";
  title.textContent = video.title;

  const subtitle = document.createElement("div");
  subtitle.className = "video-subtitle";
  subtitle.textContent = video.subtitle;

  info.append(number, title, subtitle);

  const watch = document.createElement("div");
  watch.className = "watch-label";
  watch.textContent = "WATCH ↗";

  card.append(thumb, info, watch);

  card.addEventListener("click", () => {
    if (!video.id || video.id.startsWith("VIDEO_ID_")) return;

    document.getElementById("modal-title").textContent = video.title;

    document.getElementById("video-player").src =
      `https://www.youtube.com/embed/${video.id}?autoplay=1&rel=0`;

    document.getElementById("video-modal").classList.add("active");
    document.body.style.overflow = "hidden";
  });

  videoList.appendChild(card);

});

/* CLOSE VIDEO */

function closeVideo() {
  document.getElementById("video-modal").classList.remove("active");
  document.getElementById("video-player").src = "";
  document.body.style.overflow = "";
}

document.getElementById("close-modal")
  .addEventListener("click", closeVideo);

document.getElementById("video-modal")
  .addEventListener("click", (e) => {
    if (e.target.id === "video-modal") closeVideo();
  });

document.addEventListener("keydown", (e) => {
  if (e.key === "Escape") closeVideo();
});

/* FOLLOWING CURSOR GLOW */

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
