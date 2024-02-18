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
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        background-color: #f0f0f0;
      }
      model-viewer {
        width: 100%;
        height: 500px; /* Ajustat pentru a îmbunătăți vizualizarea */
        max-width: 800px; /* Limitarea lățimii pentru a evita întinderea excesivă */
      }
      .navigation {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        cursor: pointer;
        font-size: 24px;
        user-select: none;
        color: #333;
      }
      .left-arrow {
        left: 10px;
      }
      .right-arrow {
        right: 10px;
      }
      /* Restul stilurilor tale */
    </style>
</head>
<body>

<div style="text-align: center; width: 100%;">
    <!-- Restul conținutului tău HTML -->
    <div class="navigation left-arrow" onclick="changeModel(-1)">&#8592;</div>
    <div class="navigation right-arrow" onclick="changeModel(1)">&#8594;</div>
</div>

<script>
  const models = [
    { glb: "Avatar1.glb", usdz: "Avatar1.usdz" },
    { glb: "Avatar2.glb", usdz: "Avatar2.usdz" },
    { glb: "Avatar4.glb", usdz: "Avatar4.usdz" }
  ]; // Specifică calea pentru fiecare model GLB și USDZ
  let currentIndex = 2; // Începe cu Avatar4

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

  // Codul pentru gestionarea swipe-ului rămâne neschimbat
</script>

</body>
</html>
