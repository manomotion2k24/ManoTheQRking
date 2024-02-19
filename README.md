<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Produse de calitate superioară</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
    <style>
      body {
        margin: 0;
        padding: 0;
        font-family: Arial, sans-serif;
      }
      model-viewer {
        width: 100%;
        height: 400px;
      }
      .navigation {
        display: flex;
        justify-content: space-between;
        margin-top: 20px;
        padding: 0 20px;
      }
      .nav-button {
        cursor: pointer;
        background-color: #007BFF;
        border: none;
        border-radius: 20px;
        padding: 10px 20px;
        font-size: 16px;
        color: white;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        transition: background-color 0.3s, box-shadow 0.3s;
      }
      .nav-button:hover {
        background-color: #0056b3;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
      }
      .content {
        max-width: 800px;
        margin: auto;
        padding: 20px;
      }
      .features {
        margin-top: 20px;
      }
      .links {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 10px;
        margin-left: 20px;
      }
    </style>
</head>
<body>

<div class="content">
    <h2 style="text-align: center;"><a id="mainTitle" href="#" target="_blank">Titlu Produs</a></h2>
    <div class="model-and-navigation">
      <h3 id="subtitle">Subtitlu Produs</h3>
      <model-viewer id="modelViewer" src="Avatar4.glb" ios-src="Avatar4.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="Produs">
        <button slot="ar-button" class="ar-button">
            <span class="levitate">👋</span> Activează modul AR
        </button>
      </model-viewer>
      <div class="navigation">
          <button class="nav-button" onclick="changeModel(-1)">⇦ prev</button>
          <button class="nav-button" onclick="changeModel(1)">next ⇨</button>
      </div>
    </div>
    <div class="features" id="features">
      <p>Caracteristici produs</p>
    </div>
    <div class="links">
      <p><a href="https://manomotion2k24.github.io/Pizza/" target="_blank">Pizza Quattro Formaggie</a></p>
      <p><a href="https://manomotion2k24.github.io/My-Beloved-Girl/" target="_blank">Rama Foto Familie</a></p>
      <p><a href="https://manomotion2k24.github.io/cactus/" target="_blank">Cactus Opuntia Albispina</a></p>
    </div>
</div>

<script>
  const models = [
    { file: "guler2.glb", iosFile: "guler2.usdz", title: "Cumpara acum Guler masaj", url: "https://unizdrav.ro/produse/4021/guler-de-masaj-pentru-gat-si-umeri-unizdrav", subtitle: "Guler de masaj pentru gât și umeri", features: "✔️Pornirea și oprirea căldurii<br>✔️Schimbarea rotației capetelor de masaj<br>✔️3 niveluri de intensitate<br>✔️Oprire automată" },
    { file: "scaun.glb", iosFile: "scaun.usdz", title: "Cumpara acum Scaun sufragerie stofă", url: "https://acaju.ro/products/scaun-tapitat-k365-rosu-52x57x90-cm?gad_source=1", subtitle: "Scaun tapițat", features: "✔️Produsul nu este montat<br>✔️Asamblarea este rapida si usoara<br>✔️otel acoperit cu pulbere" },
    { file: "Avatar4.glb", iosFile: "Avatar4.usdz", title: "Cumpara acum Nike sport shoes", url: "https://www.nike.com/ro/t/free-metcon-4-workout-shoes-2g2hts", subtitle: "Nike Free Matcon, rosu", features: "✔️Flexibility for Speed<br>✔️Stability for Strength<br>✔️Blast From the Past" }
  ];
  let currentIndex = 2; // Pornim de la modelul Nike sport shoes

  function changeModel(step) {
    currentIndex += step;

    if (currentIndex >= models.length) {
      currentIndex = 0;
    } else if (currentIndex < 0) {
      currentIndex = models.length - 1;
    }

    updateModel();
  }

  function updateModel() {
    const model = models[currentIndex];
    const viewer = document.getElementById('modelViewer');
    const titleElement = document.getElementById('mainTitle');
    const subtitleElement = document.getElementById('subtitle');
    const featuresElement = document.getElementById('features');

    viewer.src = model.file;
    viewer.setAttribute('ios-src', model.iosFile); // Actualizează sursa pentru AR
    viewer.alt = model.subtitle;
    titleElement.href = model.url;
    titleElement.textContent = model.title;
    subtitleElement.textContent = model.subtitle;
    featuresElement.innerHTML = model.features;
  }

  // Inițializăm primul model
  updateModel();
</script>

</body>
</html>
