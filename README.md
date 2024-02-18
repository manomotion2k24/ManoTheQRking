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
      }
      model-viewer {
        width: 100%;
        height: 500px; /* Ajustat pentru a îmbunătăți vizualizarea */
      }
      .navigation {
        display: flex;
        justify-content: space-between;
        margin-top: 10px;
      }
      .nav-button {
        cursor: pointer;
        background-color: #ddd;
        border: none;
        padding: 10px 20px;
        font-size: 16px;
      }
      .nav-button:hover {
        background-color: #ccc;
      }
      .levitate {
        display: inline-block;
        animation: levitate 1s ease-in-out infinite;
      }
      .ar-button {
        background-color: white;
        border-radius: 4px;
        border: none;
        position: absolute;
        top: 8px;
        right: 8px;
      }
      h2, h3, p {
        margin-left: 15px;
        margin-right: 15px;
      }
      .bold-link {
        font-weight: bold;
      }
    </style>
</head>
<body>

<div style="text-align: left;">
    <h2><a href="https://www.nike.com/ro/t/free-metcon-4-workout-shoes-2g2hts" target="_blank">Comanda Acum: Nike Free Matcon, rosu</a></h2>
    <h3>Workout Shoes</h3>
    <model-viewer id="modelViewer" src="Avatar4.glb" ios-src="Avatar4.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="Nike Free Matcon, rosu">
      <button slot="ar-button" class="ar-button">
          <span class="levitate">👋</span> Activează modul AR
      </button>
    </model-viewer>
    <div class="navigation">
        <button class="nav-button" onclick="changeModel(-1)">⇦ prev</button>
        <button class="nav-button" onclick="changeModel(1)">next ⇨</button>
    </div>
    <p>
        ✔️Blast From the Past<br>
        ✔️Flexibility for Speed<br>
        ✔️Stability for Strength<br>
        ✔️Colour Shown: Team Red/Cave Purple/Bright Crimson
    </p>
    <p><a href="https://manomotion2k24.github.io/Pizza/" class="bold-link" target="_blank">Pizza Quattro Formaggie</a></p>
    <p><a href="https://manomotion2k24.github.io/My-Beloved-Girl/" class="bold-link" target="_blank">Rama Foto Familie</a></p>
    <p><a href="https://manomotion2k24.github.io/cactus/" class="bold-link" target="_blank">Cactus Opuntia Albispina</a></p>
</div>

<script>
  const models = ["Avatar1.glb", "Avatar2.glb", "Avatar4.glb"];
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
</script>

</body>
</html>
