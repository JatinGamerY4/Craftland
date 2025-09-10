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
      margin-bottom: 20px;
      flex-wrap: nowrap;
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

    .random-video {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
    }

    .random-video img {
      width: 320px;
      height: 180px;
      object-fit: cover;
    }

    .bottom-section {
      display: flex;
      flex-direction: column;
      gap: 15px;
      margin-top: 20px;
    }

    .email-text {
      font-weight: bold;
      text-align: center;
    }
  </style>
</head>
<body>

<div class="heading"></div>
<div class="subheading">Main Page</div>

<div class="button-row">
  <button class="top-button" onclick="location.href='maps.html'">Maps</button>
  <button class="top-button" onclick="location.href='https://0xme.github.io/ItemID2/?mode=2'">Codes</button>
  <button class="top-button" onclick="location.href='assets.html'">Assets</button>
</div>

<div class="video-section">
  <a class="video-link" href="https://youtu.be/CqiRcReBlj0?si=ttx3INx9ud9Nk0PS" target="_blank">
    <img class="video-thumbnail" src="https://img.youtube.com/vi/CqiRcReBlj0/hqdefault.jpg" alt="Video 1">
    <div class="video-title">Point Arrow</div>
  </a>

  <a class="video-link" href="https://youtu.be/o9V2s5r7Wx4?si=dvTZRrZFbJnkqS58" target="_blank">
    <img class="video-thumbnail" src="https://img.youtube.com/vi/o9V2s5r7Wx4/hqdefault.jpg" alt="Video 2">
    <div class="video-title">Ai NPC</div>
  </a>

  <a class="video-link" href="https://youtu.be/h0ttgy1eW_M?si=A53IgLrFSVsmZXY7" target="_blank">
    <img class="video-thumbnail" src="https://img.youtube.com/vi/h0ttgy1eW_M/hqdefault.jpg" alt="Video 3">
    <div class="video-title">Random Pass</div>
  </a>

  <div class="random-video">
    <div class="video-title">RANDOM VIDEO</div>
    <div id="random-video-container"></div>
  </div>
</div>

<div class="bottom-section">
  <button class="bottom-button" onclick="location.href='https://youtube.com/@jatingamery4?si=HIaEeaxK8dG6gf0U'">Watch More</button>
  <button class="bottom-button" onclick="location.href='https://discord.gg/THYBW9ER'">Discord Server</button>
  <button class="bottom-button" onclick="location.href='https://www.instagram.com/jatingamery4'">Instagram</button>
  <div class="email-text">Email: jatingamery411@gmail.com</div>
</div>

<script>
  // Video data
  const videos = [
    { url: 'https://youtu.be/CqiRcReBlj0', thumbnail: 'https://img.youtube.com/vi/CqiRcReBlj0/hqdefault.jpg', title: 'Point Arrow' },
    { url: 'https://youtu.be/o9V2s5r7Wx4', thumbnail: 'https://img.youtube.com/vi/o9V2s5r7Wx4/hqdefault.jpg', title: 'Ai NPC' },
    { url: 'https://youtu.be/h0ttgy1eW_M', thumbnail: 'https://img.youtube.com/vi/h0ttgy1eW_M/hqdefault.jpg', title: 'Random Pass' },
    { url: 'https://youtu.be/BXfGjZ8QOv8', thumbnail: 'https://img.youtube.com/vi/BXfGjZ8QOv8/hqdefault.jpg', title: 'Pet Transform' },
    { url: 'https://youtu.be/w9LwYS8II0c', thumbnail: 'https://img.youtube.com/vi/w9LwYS8II0c/hqdefault.jpg', title: 'GTA-V Map Update' },
    { url: 'https://youtu.be/Y7_Pdjc9ARE', thumbnail: 'https://img.youtube.com/vi/Y7_Pdjc9ARE/hqdefault.jpg', title: 'Custom Banner' },
    { url: 'https://youtu.be/0We-XFLkI4M', thumbnail: 'https://img.youtube.com/vi/0We-XFLkI4M/hqdefault.jpg', title: 'Calculator in Craftland' },
    { url: 'https://youtu.be/MeazvgyvoSY', thumbnail: 'https://img.youtube.com/vi/MeazvgyvoSY/hqdefault.jpg', title: 'Learning Script' }
  ];

  // Filter out shorts and live streams
  const longVideos = videos.filter(video => {
    const duration = getVideoDuration(video.url);
    return duration > 60; // 1 minutes
  });

  // Select a random video
  const randomVideo = longVideos[Math.floor(Math.random() * longVideos.length)];

  // Display the random video
  const randomVideoContainer = document.getElementById('random-video-container');
  const randomVideoElement = document.createElement('a');
  randomVideoElement.href = randomVideo.url;
  randomVideoElement.target = '_blank';
  randomVideoElement.className = 'video-link';

  const randomVideoThumbnail = document.createElement('img');
  randomVideoThumbnail.src = randomVideo.thumbnail;
  randomVideoThumbnail.alt = randomVideo.title;
  randomVideoThumbnail.className = 'video-thumbnail';

  randomVideoElement.appendChild(randomVideoThumbnail);
  randomVideoContainer.appendChild(randomVideoElement);

  // Function to get video duration (in seconds)
  function getVideoDuration(url) {
    // For the sake of this example, we'll return a fixed duration
    // In a real implementation, you would fetch the video metadata to get the actual duration
    return 1200; // 20 minutes
  }
</script>

</body>
</html>
