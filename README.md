
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#080b18">
  <title>JATINGAMERY4 | Craftland Creator</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;600;700;800&family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --bg: #080b18;
      --cyan: #00eaff;
      --purple: #9b5cff;
      --text: #f4f7ff;
      --muted: #9ca8c2;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      min-height: 100vh;
      overflow-x: hidden;
      color: var(--text);
      background:
        radial-gradient(ellipse at 15% 15%, rgba(0,234,255,.12), transparent 35%),
        radial-gradient(ellipse at 85% 35%, rgba(155,92,255,.13), transparent 35%),
        var(--bg);
      font-family: 'Inter', sans-serif;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      z-index: -1;
      pointer-events: none;
      background-image:
        linear-gradient(rgba(255,255,255,.018) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,.018) 1px, transparent 1px);
      background-size: 45px 45px;
      mask-image: linear-gradient(to bottom, black, transparent 85%);
    }

    .cursor-glow {
      position: fixed;
      width: 320px;
      height: 320px;
      border-radius: 50%;
      background: rgba(0,234,255,.07);
      filter: blur(75px);
      pointer-events: none;
      transform: translate(-50%, -50%);
      z-index: -1;
    }

    /* NAVIGATION */

    nav {
      width: min(1150px, 92%);
      margin: 25px auto 0;
      padding: 13px 18px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 15px;
      background: rgba(17,22,42,.72);
      border: 1px solid rgba(255,255,255,.09);
      border-radius: 16px;
      backdrop-filter: blur(15px);
      box-shadow: 0 10px 40px rgba(0,0,0,.2);
    }

    .nav-logo {
      font-family: 'Orbitron', sans-serif;
      font-size: 17px;
      font-weight: 800;
      letter-spacing: 1px;
      background: linear-gradient(90deg, var(--cyan), #fff, var(--purple));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      white-space: nowrap;
    }

    .nav-links {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
      justify-content: center;
    }

    .nav-links a {
      color: #c5cde0;
      text-decoration: none;
      font-size: 12px;
      font-weight: 700;
      letter-spacing: .7px;
      padding: 11px 15px;
      border-radius: 9px;
      transition: .25s;
    }

    .nav-links a:hover,
    .nav-links a.active {
      color: white;
      background: linear-gradient(110deg, rgba(0,234,255,.18), rgba(155,92,255,.2));
      box-shadow: inset 0 0 0 1px rgba(0,234,255,.18);
    }

    /* HERO */

    .hero {
      width: min(1050px, 92%);
      margin: 100px auto 80px;
      text-align: center;
    }

    .hero-tag {
      display: inline-block;
      padding: 9px 17px;
      border: 1px solid rgba(0,234,255,.3);
      border-radius: 50px;
      color: var(--cyan);
      background: rgba(0,234,255,.06);
      font-size: 11px;
      font-weight: 800;
      letter-spacing: 2px;
      margin-bottom: 25px;
    }

    h1 {
      font-family: 'Orbitron', sans-serif;
      font-size: clamp(35px, 7vw, 76px);
      line-height: 1.15;
      font-weight: 800;
      letter-spacing: -2px;
      background: linear-gradient(100deg, #fff 10%, var(--cyan) 48%, var(--purple) 90%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      filter: drop-shadow(0 0 25px rgba(0,234,255,.13));
    }

    .hero p {
      max-width: 650px;
      margin: 23px auto 30px;
      color: var(--muted);
      font-size: 15px;
      line-height: 1.9;
    }

    .hero-buttons {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 12px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 13px 23px;
      border-radius: 10px;
      text-decoration: none;
      color: white;
      font-size: 13px;
      font-weight: 800;
      letter-spacing: .5px;
      transition: .25s;
      border: 1px solid rgba(255,255,255,.13);
      background: rgba(255,255,255,.05);
    }

    .btn.primary {
      border: none;
      background: linear-gradient(110deg, #00bcd4, #7555ff);
      box-shadow: 0 5px 25px rgba(0,190,255,.2);
    }

    .btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 8px 28px rgba(0,234,255,.18);
    }

    /* VIDEO SECTION */

    .section {
      width: min(1050px, 92%);
      margin: 0 auto 85px;
    }

    .section-heading {
      text-align: center;
      margin-bottom: 28px;
    }

    .section-heading h2 {
      font-family: 'Orbitron', sans-serif;
      font-size: clamp(21px, 4vw, 30px);
      letter-spacing: 1px;
    }

    .section-heading p {
      color: var(--muted);
      margin-top: 10px;
      font-size: 13px;
    }

    .gradient-text {
      background: linear-gradient(90deg, var(--cyan), var(--purple));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .video-box {
      padding: 12px;
      border-radius: 18px;
      background: linear-gradient(135deg, rgba(0,234,255,.17), rgba(155,92,255,.17));
      border: 1px solid rgba(255,255,255,.1);
      box-shadow: 0 15px 60px rgba(0,0,0,.3);
    }

    .video-inner {
      position: relative;
      width: 100%;
      aspect-ratio: 16 / 9;
      overflow: hidden;
      border-radius: 11px;
      background: #050711;
    }

    #playlist-player {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
    }

    /* SOCIAL LINKS */

    .socials {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 15px;
    }

    .social-card {
      padding: 23px 15px;
      text-align: center;
      border: 1px solid rgba(255,255,255,.09);
      background: rgba(18,24,45,.7);
      border-radius: 14px;
      text-decoration: none;
      color: white;
      transition: .25s;
    }

    .social-card:hover {
      transform: translateY(-5px);
      border-color: rgba(0,234,255,.4);
      background: rgba(0,234,255,.06);
    }

    .social-card h3 {
      font-size: 15px;
      margin-bottom: 8px;
    }

    .social-card p {
      color: var(--muted);
      font-size: 11px;
    }

    /* FOOTER */

    footer {
      padding: 25px 15px;
      text-align: center;
      border-top: 1px solid rgba(255,255,255,.07);
      color: #78849f;
      font-size: 11px;
      letter-spacing: .5px;
    }

    footer span {
      color: var(--cyan);
      font-weight: 800;
    }

    /* MOBILE */

    @media (max-width: 650px) {
      nav {
        flex-direction: column;
        padding: 16px 10px;
      }

      .nav-links {
        width: 100%;
        gap: 3px;
      }

      .nav-links a {
        padding: 10px 11px;
        font-size: 10px;
      }

      .hero {
        margin-top: 75px;
      }

      .hero p {
        font-size: 13px;
      }

      .socials {
        grid-template-columns: 1fr;
      }

      .section {
        margin-bottom: 65px;
      }
    }
  </style>
</head>

<body>

  <div class="cursor-glow" id="cursorGlow"></div>

  <!-- NAVIGATION -->
  <nav>
    <div class="nav-logo">JATINGAMERY4</div>

    <div class="nav-links">
      <a href="index.html" class="active">HOME</a>
      <a href="maps.html">MAPS</a>
      <a href="https://0xme.github.io/ItemID2/?mode=2&page=1" target="_blank" rel="noopener noreferrer">CODES</a>
      <a href="assets.html">ASSETS</a>
    </div>
  </nav>

  <!-- HERO SECTION -->
  <main>
    <section class="hero">
      <div class="hero-tag">FREE FIRE CRAFTLAND CREATOR</div>

      <h1>JATINGAMERY4</h1>

      <p>
        Welcome to my official website! Explore my Craftland maps,
        discover useful asset codes, and watch my latest tutorials
        and gaming content.
      </p>

      <div class="hero-buttons">
        <a class="btn primary" href="maps.html">EXPLORE MAPS</a>
        <a class="btn" href="assets.html">ASSET LIBRARY</a>
        <a class="btn" href="https://youtube.com/@JATINGAMERY4" target="_blank" rel="noopener noreferrer">YOUTUBE CHANNEL</a>
      </div>
    </section>

    <!-- VIDEOS SECTION -->
    <section class="section">
      <div class="section-heading">
        <h2>MY <span class="gradient-text">VIDEOS</span></h2>
        <p>Watch my Craftland tutorials and latest uploads.</p>
      </div>

      <div class="video-box">
        <div class="video-inner">
          <div id="playlist-player"></div>
        </div>
      </div>
    </section>

    <!-- SOCIAL SECTION -->
    <section class="section">
      <div class="section-heading">
        <h2>CONNECT <span class="gradient-text">WITH ME</span></h2>
        <p>Follow me and join the community.</p>
      </div>

      <div class="socials">
        <a class="social-card"
           href="https://www.instagram.com/jatingamery4/"
           target="_blank"
           rel="noopener noreferrer">
          <h3>INSTAGRAM</h3>
          <p>@jatingamery4</p>
        </a>

        <a class="social-card"
           href="https://discord.gg/QXuW5FtUbz"
           target="_blank"
           rel="noopener noreferrer">
          <h3>DISCORD</h3>
          <p>Join the community</p>
        </a>

        <a class="social-card"
           href="mailto:jatingamery411@gmail.com">
          <h3>EMAIL</h3>
          <p>Contact for business</p>
        </a>
      </div>
    </section>
  </main>

  <!-- FOOTER -->
  <footer>
    © 2026 <span>JATINGAMERY4</span> — All Rights Reserved.
  </footer>

  <script>
    // Cursor glow
    const cursorGlow = document.getElementById("cursorGlow");

    if (window.matchMedia("(pointer: fine)").matches) {
      document.addEventListener("mousemove", (e) => {
        cursorGlow.style.left = e.clientX + "px";
        cursorGlow.style.top = e.clientY + "px";
      });
    } else {
      cursorGlow.style.display = "none";
    }

    // YouTube playlist player
    let player;

    function onYouTubeIframeAPIReady() {
      player = new YT.Player("playlist-player", {
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
          }
        }
      });
    }

    // Load YouTube API
    const tag = document.createElement("script");
    tag.src = "https://www.youtube.com/iframe_api";
    document.head.appendChild(tag);
  </script>

</body>
</html>
