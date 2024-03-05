<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Deniz's Portfolio</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom, #8A2BE2, #5F9EA0);
      color: #000;
    }

    #container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }

    #content {
      text-align: center;
    }

    button {
      background-color: transparent;
      color: #fff;
      border: 2px solid #fff;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    button:hover {
      background-color: #fff;
      color: #000;
    }

    #local-time {
      position: absolute;
      top: 10px;
      left: 10px;
      color: #fff;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <div id="container">
    <div id="content">
      <h1>👋🏼 Hi, I'm Deniz 🦄</h1>
      <p>
        I'm a frontend engineer based in Lisbon. Currently, I'm working at Wope.
        Known for my interest in modern art and minimalist works, I'm also passionate about music.
        I'm continuously developing my musical skills, enjoying exploring new genres.
        You can follow me on <a href="https://github.com/deniz" target="_blank">GitHub</a> to stay updated on my projects.
        For a deeper dive into my professional background and past projects, feel free to check out my <a href="https://linkedin.com/in/deniz" target="_blank">LinkedIn</a> profile.
        Additionally, I share snippets of my life on <a href="https://twitter.com/deniz" target="_blank">Twitter</a> and <a href="https://instagram.com/deniz" target="_blank">Instagram</a>.
        If you want to reach me, you can email me at <a href="mailto:hi@deniz.dev">hi@deniz.dev</a>.
      </p>
      <button onclick="toggleTheme()">Toggle Theme</button>
    </div>
  </div>

  <div id="local-time"></div>

  <script>
    function toggleTheme() {
      const body = document.querySelector('body');
      const currentTheme = body.classList.contains('dark-theme') ? 'light-theme' : 'dark-theme';
      body.className = currentTheme;
    }

    function updateTime() {
      const now = new Date();
      const hours = now.getHours().toString().padStart(2, '0');
      const minutes = now.getMinutes().toString().padStart(2, '0');
      const seconds = now.getSeconds().toString().padStart(2, '0');
      document.getElementById('local-time').textContent = `Local Time: ${hours}:${minutes}:${seconds}`;
    }

    updateTime();
    setInterval(updateTime, 1000);
  </script>
</body>
</html>
