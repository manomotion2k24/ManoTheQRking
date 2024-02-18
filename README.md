<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comanda Acum: Nike Free Matcon, rosu</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
    <style>
      body {
        margin: 0;
        padding: 0;
        font-family: Arial, sans-serif;
      }
      model-viewer {
        width: 100%;
        height: 300px;
      }
      .navigation {
        display: flex;
        justify-content: space-between;
        margin-top: 40px;
        padding: 0 20px;
      }
      .nav-button, .ar-button {
        cursor: pointer;
        background-color: #007BFF;
        border: none;
        border-radius: 20px;
        padding: 10px 20px;
        font-size: 16px;
        color: white;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        transition: background-color 0.3s, box-shadow 0.3s;
        display: block; /* Asigură că butonul este bloc pentru a respecta margin-top */
        width: fit-content;
        margin: 20px auto; /* Centrează butonul și adaugă spațiu deasupra și dedesubt */
      }
      .nav-button:hover, .ar-button:hover {
        background-color: #0056b3;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
      }
      .content {
        max-width: 800px;
        margin: auto;
        padding: 20px;
      }
      .features {
        margin-top: 40px;
      }
    </style>
</head>
<body>

<div class="content">
    <h2 style="text-align: center;"><a href="https://www.nike.com/ro/t/free-metcon-4-workout-shoes-2g2hts" target="_blank">Comanda Acum: Nike Free Matcon, rosu</a></h2>
    <div class="model-and-navigation">
      <h3>Workout Shoes</h3>
      <model-viewer id="modelViewer" src="Avatar4.glb" ios-src="Avatar4.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="Nike Free Matcon, rosu">
      </model-viewer>
      <!-- Container nou pentru butonul AR -->
      <button class="ar-button" onclick="activateAR()">
          <span class="levitate">👋</span> Activează modul AR
      </button>
      <div class="navigation">
          <button class="nav-button" onclick="changeModel(-1)">⇦ prev</button>
          <button class="nav-button" onclick="changeModel(1)">next ⇨</button>
      </div>
    </div>
    <div class="features">
      <p>
          ✔️Blast From the Past<br>
          ✔️Flexibility for Speed<br>
          ✔️Stability for Strength<br>
          ✔️Colour Shown: Team Red/Cave Purple/Bright Crimson
      </p>
    </div>
    <p><a href="https://manomotion2k24.github.io/Pizza/" class="bold-link" target="_blank">Pizza Quattro Formaggie</a></p>
    <p><a href="https://manomotion2k24.github.io/My-Beloved-Girl/" class="bold-link" target="_blank">Rama Foto Familie</a></p>
    <p><a href="https://manomotion2k24.github.io/cactus/" class="bold-link" target="_blank">Cactus Opuntia Albispina</a></p>
</div>

<script>
  const models = ["guler2.glb", "Avatar2.glb", "Avatar4.glb"];
  let currentIndex = 2;

  const viewer = document.getElementById('modelViewer');

  function changeModel(step) {
    currentIndex += step;

    if (currentIndex >= models.length) {
      currentIndex = 0;
    } else if (currentIndex < 0) {
      currentIndex = models.length - 1;
    }

    viewer.src = models[currentIndex];
  }

  // Funcția pentru activarea modului AR trebuie definită
  function activateAR() {
    // Cod pentru activarea modului AR aici
  }
</script>

</body>
</html>
