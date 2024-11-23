<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Game Embed</title>
  <style>
    body, html, iframe {
      margin: 0;
      padding: 0;
      height: 100%;
      width: 100%;
      overflow: hidden;
    }
    /* Set iframe to fill the entire window */
    iframe {
      width: 100%;  /* Make the iframe take up full width */
      height: 100vh;  /* Make the iframe take up full height of the viewport */
      border: none;  /* Remove the border */
    }
    .forceIosScrolling {
      overflow: scroll;
      -webkit-overflow-scrolling: touch;
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
