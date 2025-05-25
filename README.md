
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

    .heading {
      font-size: 32px;
      font-weight: bold;
      color: #1976d2;
      margin-bottom: 10px;
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
      margin-bottom: 30px;
      flex-wrap: nowrap;
    }

    .top-button {
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
  </style>
</head>
<body>

<audio id="clickSound" src="mixkit-hard-typewriter-click-1119.wav"></audio>
<script>
  function playSound() {
    const sound = document.getElementById("clickSound");
    sound.currentTime = 0;
    sound.play();
  }

  window.onload = function () {
    const buttons = document.querySelectorAll("button, a");
    buttons.forEach(button => {
      button.addEventListener("click", playSound);
    });
  };
</script>

<div class="heading">Craftland</div>
<div class="subheading">Main Page</div>

<div class="button-row">
  <button class="top-button" onclick="location.href='maps.html'">Maps</button>
  <button class="top-button" onclick="location.href='https://0xme.github.io/ItemID2/?mode=2'">Codes</button>
  <button class="top-button" onclick="location.href='assets.html'">Assets</button>
</div>

<div class="video-section">
  <a class="video-link" href="https://youtu.be/Eyu900UIuc4?si=rywJf-6CzVtbWtkQ" target="_blank">
    <img class="video-thumbnail" src="https://img.youtube.com/vi/Eyu900UIuc4/hqdefault.jpg" alt="Video 1">
    <div class="video-title">Add Limits</div>
  </a>

  <a class="video-link" href="https://youtu.be/C9HkfSy-iDI" target="_blank">
    <img class="video-thumbnail" src="https://img.youtube.com/vi/C9HkfSy-iDI/hqdefault.jpg" alt="Video 2">
    <div class="video-title">2D Camera</div>
  </a>

  <a class="video-link" href="https://youtu.be/ik5kmfaoCbw?si=AQCklWg7zf-XcCDX" target="_blank">
    <img class="video-thumbnail" src="https://img.youtube.com/vi/ik5kmfaoCbw/hqdefault.jpg" alt="Video 3">
    <div class="video-title">Spin Wheel</div>
  </a>
</div>

</body>
</html>
