<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>💖 Un correo para ti by myeya 💖</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: "Poppins", sans-serif;
      background-color: #fff;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      text-align: center;
      color: #333;
      transition: background-color 0.5s ease;
    }
    h2 {
      margin-bottom: 20px;
    }
    .screen {
      display: none;
      animation: fadeIn 0.8s ease;
      width: 90%;
      max-width: 600px;
    }
    .active {
      display: block;
    }
    .main-img {
      width: 280px;
      height: auto;
      margin-bottom: 15px;
      cursor: pointer;
      transition: transform 0.3s ease;
      border: none;
      box-shadow: none;
    }
    .main-img:hover {
      transform: scale(1.05);
    }
    .card {
      background: repeating-linear-gradient(
        white,
        white 28px,
        #e3e3e3 29px
      );
      border-radius: 0; /* esquinas en punta */
      padding: 40px 60px;
      border: 2px solid #e5e5e5;
      width: 95%;
      max-width: 900px;
      text-align: left;
      margin: 0 auto;
      box-sizing: border-box;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
      animation: fadeIn 1s ease;
    }
    .card h3 {
      font-family: 'Dancing Script', cursive;
      font-size: 2em;
      text-align: left;
      margin-bottom: 20px;
      margin-left: 10px;
      color: #444;
    }
    .card p {
      font-family: 'Dancing Script', cursive;
      font-size: 1.3em;
      line-height: 1.6;
      text-align: justify;
      color: #444;
      margin: 10px 0;
    }
    .return-btn {
      margin-top: 25px;
      padding: 10px 20px;
      font-size: 1em;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      transition: 0.3s;
      background-color: #ff4f81;
      color: white;
    }
    .return-btn:hover {
      background-color: #ff2a66;
    }
    @keyframes fadeIn {
      from {opacity: 0; transform: scale(0.95);}
      to {opacity: 1; transform: scale(1);}
    }
  </style>
</head>
<body>
  <div class="screen active" id="screen1">
    <h2>Hola, te llegó un correo</h2>
    <img src="https://acortar.link/XPC32D" alt="Correo" class="main-img" onclick="nextScreen(2)">
  </div>
  <div class="screen" id="screen2">
    <h2>Una cartita para ti</h2>
    <img src="https://acortar.link/BgOep0" alt="Carta" class="main-img" onclick="nextScreen(3)">
  </div>
  <div class="screen" id="screen3">
    <h2>¡Ábrelo!</h2>
    <img src="https://acortar.link/IieZ60" alt="Sobre" class="main-img" onclick="nextScreen(4)">
  </div>
  <div class="screen" id="screen4">
    <h2>¿Qué dirá?</h2>
    <img src="https://acortar.link/ylGOP0" alt="Carta lista" class="main-img" onclick="nextScreen(5)">
  </div>
  <div class="screen" id="screen5">
    <div class="card">
      <h3>Feliz primer mes, amorcito</h3>
      <p>Es increíble cómo ha pasado el tiempo. Recuerdo cuando mencionaste que no hay mejor forma de empezar el año y cada 1 de mes que juntos, tienes razón y lo mejor de todo es que es contigo. Tengo tantas cosas que decirte que presiento que escribiré muchas cartas, y sí, tendrás que leerlas todas.
        Gracias por todo, por tu paciencia, tu comprensión y tu cariño, por todo lo que demuestras conmigo.</p>
      <p>Es increíble cómo, estando lejos, te siento tan cerca, aunque sí me gustaría tenerte aquí, pero por ahora no se puede; sin embargo, cada mes más juntos es también un mes menos para volver a vernos. Te extraño y te tengo presente todos los días, te recuerdo y soy consciente de cuánto te quiero y de lo importante que eres para mí.</p>
      <p>Con mucho cariño,</p>
      <p>tu princesita 💌</p>
    </div>
    <div style="text-align: center;">
      <button class="return-btn" onclick="nextScreen(1)">🔙 Regresar</button>
    </div>
  </div>
  <script>
    function nextScreen(num) {
      const current = document.querySelector(".screen.active");
      if (current) current.classList.remove("active");
      document.getElementById("screen" + num).classList.add("active");
    }
  </script>
</body>
</html>
