
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Craftland</title>
  <style>
    body {
      margin: 0;
      padding: 20px;
      background-color: #f4f4f4;
      font-family: Arial, sans-serif;
    }

    .heading {
      font-size: 32px;
      font-weight: bold;
      color: #1976d2;
      margin-bottom: 20px;
    }

    .button-container {
      display: flex;
      gap: 20px;
      margin-bottom: 40px;
    }

    .top-button-link {
      width: 100px;
      height: 60px;
      border: none;
      color: white;
      font-size: 16px;
      font-weight: bold;
      border-radius: 8px;
      background: linear-gradient(to right, green, orange);
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      text-decoration: none;
    }

    .video-section {
      display: flex;
      flex-direction: column;
      gap: 20px;
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
      transition: box-shadow 0.3s;
    }

    .video-link:hover {
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
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

    .watch-more,
    .discord-button,
    .instagram-button {
      display: flex;
      justify-content: center;
      align-items: center;
      text-decoration: none;
      border: 1px solid #ccc;
      border-radius: 8px;
      background-color: #fff;
      font-size: 20px;
      font-weight: bold;
      padding: 20px;
      color: #000;
      transition: box-shadow 0.3s;
    }

    .watch-more:hover,
    .discord-button:hover,
    .instagram-button:hover {
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }

  </style>
</head>
<body>

  <div class="heading">Main Page</div>

  <div class="button-container">
    <a href="maps.html" class="top-button-link">Maps</a>
    <a href="https://0xme.github.io/ItemID2/?mode=2" class="top-button-link" target="_blank">Codes</a>
    <a href="assets.html" class="top-button-link">Assets</a>
  </div>

  <div class="video-section">
    <a class="video-link" href="https://youtu.be/MiwqlbYlPC4?si=G6rsKX1Nqx-R_PXU" target="_blank">
      <img class="video-thumbnail" src="https://img.youtube.com/vi/MiwqlbYlPC4/hqdefault.jpg" alt="Video 1 Thumbnail">
      <div class="video-title">Add Limits</div>
    </a>

    <a class="video-link" href="https://youtu.be/C9HkfSy-iDI" target="_blank">
      <img class="video-thumbnail" src="https://img.youtube.com/vi/C9HkfSy-iDI/hqdefault.jpg" alt="Video 2 Thumbnail">
      <div class="video-title">2D Camera</div>
    </a>

    <a class="video-link" href="https://youtu.be/ik5kmfaoCbw?si=AQCklWg7zf-XcCDX" target="_blank">
      <img class="video-thumbnail" src="https://img.youtube.com/vi/ik5kmfaoCbw/hqdefault.jpg" alt="Video 3 Thumbnail">
      <div class="video-title">Spin Wheel</div>
    </a>

    <a class="video-link watch-more" href="https://youtube.com/@jatingamery4?si=d_aTTv89b2sd4TJZ" target="_blank">
      Watch More
    </a>

    <a class="video-link discord-button" href="https://discord.gg/THYBW9ER" target="_blank">
      Discord Server
    </a>

    <a class="video-link instagram-button" href="https://www.instagram.com/jatingamery4" target="_blank">
      Instagram
    </a>
  </div>

</body>
</html>
