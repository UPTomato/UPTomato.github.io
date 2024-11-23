<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Game Embed</title>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      width: 100%;
      display: flex;
      justify-content: center;  /* Centers iframe horizontally */
      align-items: center;  /* Centers iframe vertically */
      background-color: #f0f0f0;  /* Optional: sets background color */
    }

    /* Set iframe to a 16:9 aspect ratio, but scaled 5 times larger */
    iframe {
      width: 90%;  /* 90% of the screen width */
      height: 80%;  /* 50% of the screen height */
      max-width: 1280px;  /* Limits maximum width */
      max-height: 720px;  /* Limits maximum height */
      border: none;
    }
  </style>
</head>
<body>
  <iframe id="innerFrame" name="innerFrame" sandbox="allow-scripts allow-popups allow-forms allow-same-origin allow-popups-to-escape-sandbox allow-downloads allow-storage-access-by-user-activation" frameborder="0" allowfullscreen="" src="https://somuchmath.global.ssl.fastly.net/projects/stickman-hook/index.html" style="overflow: auto;">
  </iframe>

  <script>
    window.addEventListener('keydown', function(event) {
      const iframe = document.getElementById('innerFrame');
      if (iframe && iframe.contentWindow) {
        if (event.key === 'm' || event.key === 'M') {
          event.preventDefault();
          const spaceEvent = new KeyboardEvent('keydown', {
            key: ' ',
            code: 'Space',
            keyCode: 32,
            which: 32,
            bubbles: true
          });
          iframe.contentWindow.document.dispatchEvent(spaceEvent);
        }
      }
    });
  </script>
</body>
</html>

