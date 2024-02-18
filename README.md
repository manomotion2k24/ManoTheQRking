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
      @keyframes levitate {
        0%, 100% {
          transform: translateY(0);
        }
        50% {
          transform: translateY(-10px);
        }
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
      h2 {
        font-size: 20px; /* Ajustat pentru a fi mai lizibil */
        margin: 10px 0; /* Spațiere ajustată */
      }
      h3 {
        font-size: 18px; /* Ajustat pentru a fi mai lizibil */
        margin: 20px 0 Participant 0;
      }
      p {
        font-size: 16px; /* Ajustat pentru a fi mai lizibil */
      }
      .bold-link {
        font-weight: bold;
      }
    </style>
</head>
<body>

<div style="text-align: left; padding: 15px;">
    <h2><a href="https://www.nike.com/ro/t/free-metcon-4-workout-shoes-2g2hts" target="_blank">Comanda Acum: Nike Free Matcon, rosu</a></h2>
    <h3>Workout Shoes</h3>
    <model-viewer id="modelViewer" src="Avatar4.glb" ios-src="Avatar4.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="Nike Free Matcon, rosu">
      <button slot="ar-button" class="ar-button">
          <span class="levitate">👋</span> Activează modul AR
      </button>
    </model-viewer>
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
  const models = ["Avatar1.glb", "Avatar2.glb", "Avatar4.glb"]; // Adaugă calea pentru fiecare model
  let currentIndex = 2; // Începe cu Avatar4.glb care este indexul 2 în array-ul nostru

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

  let startX;

  viewer.addEventListener('touchstart', (e) => {
    startX = e.touches[0].pageX;
  });

  viewer.addEventListener('touchend', (e) => {
    const endX = e.changedTouches[0].pageX;

    if (startX - endX > 50) {
      changeModel(1); // Swipe left
    } else if (startX - endX < -50) {
      changeModel(-1); // Swipe right
    }
  });
</script>

</body>
</html>
