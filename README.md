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

<div class="video-section" id="video-section">
  <!-- Videos will be inserted here by JavaScript -->
</div>

<div class="bottom-section">
  <button class="bottom-button" onclick="location.href='https://youtube.com/@jatingamery4?si=HIaEeaxK8dG6gf0U'">Watch More</button>
  <button class="bottom-button" onclick="location.href='https://discord.gg/THYBW9ER'">Discord Server</button>
  <button class="bottom-button" onclick="location.href='https://www.instagram.com/jatingamery4'">Instagram</button>
  <div class="email-text">Email: jatingamery411@gmail.com</div>
</div>

<script>
  // Array of video objects with URL, thumbnail, and title
  const videos = [
    { url: 'https://youtu.be/CqiRcReBlj0', thumbnail: 'https://img.youtube.com/vi/CqiRcReBlj0/hqdefault.jpg', title: 'How to Make a Pointing Arrow in Craftland' },
    { url: 'https://youtu.be/o9V2s5r7Wx4', thumbnail: 'https://img.youtube.com/vi/o9V2s5r7Wx4/hqdefault.jpg', title: 'Make AI NPC In Craftland' },
    { url: 'https://youtu.be/h0ttgy1eW_M', thumbnail: 'https://img.youtube.com/vi/h0ttgy1eW_M/hqdefault.jpg', title: 'Random Pass in Craftland' },
    { url: 'https://youtu.be/BXfGjZ8QOv8', thumbnail: 'https://img.youtube.com/vi/BXfGjZ8QOv8/hqdefault.jpg', title: 'Transform Into Pet in Craftland' },
    { url: 'https://youtu.be/w9LwYS8II0c', thumbnail: 'https://img.youtube.com/vi/w9LwYS8II0c/hqdefault.jpg', title: 'GTA-V Craftland Map Update' },
    { url: 'https://youtu.be/Y7_Pdjc9ARE', thumbnail: 'https://img.youtube.com/vi/Y7_Pdjc9ARE/hqdefault.jpg', title: 'Make Custom Banner in Craftland' },
    { url: 'https://youtu.be/0We-XFLkI4M', thumbnail: 'https://img.youtube.com/vi/0We-XFLkI4M/hqdefault.jpg', title: 'I Made Calculator in Craftland' },
    { url: 'https://youtu.be/MeazvgyvoSY', thumbnail: 'https://img.youtube.com/vi/MeazvgyvoSY/hqdefault.jpg', title: 'How I Started Learning Script' }
  ];

  // Function to get a random video
  function getRandomVideo() {
    const randomIndex = Math.floor(Math.random() * videos.length);
    return videos[randomIndex];
  }

  // Function to update the video section with random videos
  function updateVideos() {
    const videoSection = document.getElementById('video-section');
    videoSection.innerHTML = ''; // Clear existing videos

    for (let i = 0; i < 3; i++) {
      const video = getRandomVideo();
      const videoLink = document.createElement('a');
      videoLink.classList.add('video-link');
      videoLink.href = video.url;
      videoLink.target = '_blank';

      const thumbnail = document.createElement('img');
      thumbnail.classList.add('video-thumbnail');
      thumbnail.src = video.thumbnail;
      thumbnail.alt = video.title;

      const title = document.createElement('div');
      title.classList.add('video-title');
      title.textContent = video.title;

      videoLink.appendChild(thumbnail);
      videoLink.appendChild(title);
      videoSection.appendChild(videoLink);
    }
  }

  // Update videos on page load
  window.onload = updateVideos;
</script>

</body>
</html>
