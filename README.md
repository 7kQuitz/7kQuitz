<p align="center">
<img width="1200" height="400" alt="Untitled_Artwork 4" src="https://github.com/user-attachments/assets/7274096a-2be0-4f53-8b79-cf977d0c3682" />


<p align="center">
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Typewriter Effect</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #0d0d0d;
      color: white;
      font-family: "Courier New", monospace;
      overflow: hidden;
    }

    .typewriter {
      font-size: 2rem;
      white-space: pre-line;
      border-right: 3px solid white;
      width: fit-content;
      animation: blink 0.7s infinite;
    }

    @keyframes blink {
      50% {
        border-color: transparent;
      }
    }
  </style>
</head>
<body>

  <div class="typewriter" id="text"></div>

  <script>
    const text = `I'm trying to sleep
But I can't when you all have
guns for hands!`;

    const speed = 60;
    let i = 0;

    function typeWriter() {
      if (i < text.length) {
        document.getElementById("text").innerHTML += text.charAt(i);
        i++;
        setTimeout(typeWriter, speed);
      }
    }

    typeWriter();
  </script>

</body>
</html>
