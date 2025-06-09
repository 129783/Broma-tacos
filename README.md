# Broma-tacos
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Broma de Tacos</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 100px;
    }

    h1 {
      font-size: 24px;
    }

    .opciones {
      margin-top: 30px;
    }

    .btn {
      padding: 10px 20px;
      margin: 10px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.2s;
    }

    .escapista {
      position: relative;
    }
  </style>
</head>
<body>
  <h1>Te invito a los tacos, tú pagas, ¿aceptas?</h1>
  <div class="opciones">
    <button class="btn" onclick="alert('¡Sabía que dirías que sí! 🌮😁')">
      Claro, yo encantada de pagar todos los tacos que te comas
    </button>

    <button class="btn escapista" id="mover1">
      En vez de que tú pagues
    </button>

    <button class="btn escapista" id="mover2">
      A ver, mejor yo te invito y tú pagas
    </button>
  </div>

  <script>
    const mover1 = document.getElementById("mover1");
    const mover2 = document.getElementById("mover2");

    function moverBoton(boton) {
      const x = Math.floor(Math.random() * 300) - 150;
      const y = Math.floor(Math.random() * 300) - 150;
      boton.style.transform = `translate(${x}px, ${y}px)`;
    }

    mover1.addEventListener("mouseover", () => moverBoton(mover1));
    mover2.addEventListener("mouseover", () => moverBoton(mover2));
  </script>
</body>
</html>
