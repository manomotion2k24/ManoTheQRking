<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comanda Acum: Nike Free Matcon, rosu</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
    <style>
      /* stilurile tale aici */
    </style>
</head>
<body>

<div style="text-align: left; padding: 15px;">
    <!-- conținutul tău aici -->
    <model-viewer id="modelViewer" src="Avatar4.glb" ios-src="Avatar4.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="Nike Free Matcon, rosu">
      <button slot="ar-button" class="ar-button">
          <span class="levitate">👋</span> Activează modul AR
      </button>
    </model-viewer>
    <!-- restul conținutului tău -->
</div>

<script>
  const models = [
    { glb: "Avatar1.glb", usdz: "Avatar1.usdz" },
    { glb: "Avatar2.glb", usdz: "Avatar2.usdz" },
    { glb: "Avatar4.glb", usdz: "Avatar4.usdz" }
  ]; // Specifică calea pentru fiecare model GLB și USDZ
  let currentIndex = 2; // Începe cu Avatar4 care este indexul 2 în array-ul nostru

  const viewer = document.getElementById('modelViewer');

  function changeModel(step) {
    currentIndex += step;

    if (currentIndex >= models.length) {
      currentIndex = 0;
    } else if (currentIndex < 0) {
      currentIndex = models.length - 1;
    }

    viewer.setAttribute('src', models[currentIndex].glb);
    viewer.setAttribute('ios-src', models[currentIndex].usdz);
  }

  let startX;

  viewer.addEventListener('touchstart', (e) => {
    startX = e.touches[0].pageX;
  });

  viewer.addEventListener('touchend', (e) => {
    const endX = e.changedTouches[0].pageX;

    if (startX - endX > 50) {
      changeModel(1); // Swipe la stânga
    } else if (startX - endX < -50) {
      changeModel(-1); // Swipe la dreapta
    }
  });
</script>

</body>
</html>
