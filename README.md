
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Craftland</title>

  <style>
    body {
      margin: 0;
      padding: 20px;
      background-color: #f4f4f4;
      font-family: Arial, sans-serif;
    }

    .subheading {
      font-size: 28px;
      font-weight: bold;
      color: #1976d2;
      margin-bottom: 20px;
    }

    .button-row {
      display: flex;
      gap: 20px;
      margin-bottom: 20px;
    }

    .top-button, .bottom-button {
      flex: 1;
      height: 60px;
      border: none;
      color: white;
      font-size: 16px;
      font-weight: bold;
      border-radius: 8px;
      background: linear-gradient(to right, green, orange);
      cursor: pointer;
    }

    .video-section {
      display: flex;
      flex-direction: column;
      gap: 20px;
      margin-bottom: 30px;
    }

    .video-link {
      display: flex;
      align-items: center;
      text-decoration: none;
      color: #000;
      border: 1px solid #ccc;
      border-radius: 8px;
      overflow: hidden;
      background-color: #fff;
    }

    .video-thumbnail {
      width: 160px;
      height: 90px;
      object-fit: cover;
    }

    .video-title {
      padding: 10px;
      font-size: 16px;
      font-weight: bold;
    }

    .bottom-section {
      display: flex;
      flex-direction: column;
      gap: 15px;
      margin-top: 20px;
    }
  </style>
</head>

<body>

  <div class="subheading">Main Page</div>

  <div class="button-row">
    <button class="top-button" onclick="location.href='maps.html'">Maps</button>
    <button class="top-button" onclick="location.href='https://0xme.github.io/ItemID2/?mode=2'">Codes</button>
    <button class="top-button" onclick="location.href='assets.html'">Assets</button>
  </div>

  <div class="video-section">

    <a class="video-link" href="https://youtu.be/CnAU9C-dseg" target="_blank">
      <img class="video-thumbnail" src="https://img.youtube.com/vi/CnAU9C-dseg/hqdefault.jpg">
      <div class="video-title">Video 1</div>
    </a>

    <a class="video-link" href="https://youtu.be/QfLS0kn8MWw" target="_blank">
      <img class="video-thumbnail" src="https://img.youtube.com/vi/QfLS0kn8MWw/hqdefault.jpg">
      <div class="video-title">Video 2</div>
    </a>

    <a class="video-link" href="https://youtu.be/SYV8RvdVBnI" target="_blank">
      <img class="video-thumbnail" src="https://img.youtube.com/vi/SYV8RvdVBnI/hqdefault.jpg">
      <div class="video-title">Video 3</div>
    </a>

  </div>

  <div class="bottom-section">
    <button class="bottom-button"
      onclick="window.open('https://www.instagram.com/jatingamery4','_blank')">
      Follow on Instagram
    </button>

    <button class="bottom-button"
      onclick="window.open('https://discord.gg/official-craftland-creators-india-1338827872781205556','_blank')">
      Join Discord
    </button>
  </div>

</body>
</html>
