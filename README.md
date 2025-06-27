<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Status Rotator</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color: white;
    }

    .rotator {
      font-size: 2rem;
      text-align: center;
      padding: 20px 40px;
      background-color: rgba(255, 255, 255, 0.05);
      border-radius: 12px;
      box-shadow: 0 0 20px rgba(0, 255, 255, 0.4);
      backdrop-filter: blur(5px);
    }

    .fade {
      opacity: 0;
      transition: opacity 0.5s ease-in-out;
    }

    .fade.show {
      opacity: 1;
    }
  </style>
</head>
<body>

  <div class="rotator">
    <span id="statusText" class="fade show">Cargando estado...</span>
  </div>

  <script>
    const statuses = [
      "✅ En línea y funcionando",
      "🔧 Mantenimiento en curso",
      "🚀 Nuevas funciones disponibles",
      "📡 Conectando con el servidor...",
      "⚡ Todo va súper rápido hoy"
    ];

    let index = 0;
    const statusText = document.getElementById("statusText");

    function rotateStatus() {
      statusText.classList.remove("show");
      setTimeout(() => {
        index = (index + 1) % statuses.length;
        statusText.textContent = statuses[index];
        statusText.classList.add("show");
      }, 500);
    }

    setInterval(rotateStatus, 3000);
  </script>

</body>
</html>
