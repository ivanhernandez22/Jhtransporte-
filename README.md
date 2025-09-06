<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JH Transporte</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: #f8f8f8;
      text-align: center;
    }
    header {
      background: #ff6600;
      color: white;
      padding: 15px;
      font-size: 1.5em;
      font-weight: bold;
    }
    .carousel {
      position: relative;
      max-width: 100%;
      margin: auto;
      overflow: hidden;
    }
    .slides {
      display: flex;
      transition: transform 0.5s ease-in-out;
      width: 600%;
    }
    .slides img {
      width: 100%;
      border-bottom: 5px solid #ff6600;
    }
    .buttons {
      margin: 15px;
    }
    .btn {
      display: inline-block;
      padding: 12px 20px;
      margin: 5px;
      border-radius: 8px;
      text-decoration: none;
      color: white;
      font-weight: bold;
    }
    .whatsapp {
      background: #25d366;
    }
    .email {
      background: #0072c6;
    }
    footer {
      background: #333;
      color: white;
      padding: 10px;
      margin-top: 20px;
      font-size: 0.9em;
    }
  </style>
</head>
<body>

  <header>🚛 JH Transporte</header>

  <div class="carousel">
    <div class="slides" id="slides">
      <img src="https://i.imgur.com/0cBqG2C.jpg" alt="Camión 1">
      <img src="https://i.imgur.com/HU0bbGd.jpg" alt="Camión 2">
      <img src="https://i.imgur.com/fv5RkgT.jpg" alt="Camión 3">
      <img src="https://i.imgur.com/yjxH5M5.jpg" alt="Camión 4">
      <img src="https://i.imgur.com/fpc6TjY.jpg" alt="Camión 5">
      <img src="https://i.imgur.com/8n5Z7Nb.jpg" alt="Camión 6">
    </div>
  </div>

  <div class="buttons">
    <a href="https://wa.me/5491156330148" class="btn whatsapp">📲 WhatsApp</a>
    <a href="mailto:jhtransportes1@hotmail.com" class="btn email">📧 Enviar Mail</a>
  </div>

  <footer>
    © 2025 JH Transporte - Todos los derechos reservados
  </footer>

  <script>
    let index = 0;
    const slides = document.getElementById("slides");
    const total = slides.children.length;

    function showSlide() {
      index = (index + 1) % total;
      slides.style.transform = `translateX(-${index * 100}%)`;
    }

    setInterval(showSlide, 3000);
  </script>

</body>
</html>

