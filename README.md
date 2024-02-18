<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Descoperă Produsele Noastre</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
    <style>
      body {
        margin: 0;
        padding: 0;
        font-family: Arial, sans-serif;
      }
      model-viewer {
        width: 100%;
        height: 400px; /* Ajustat la 400px pentru o vizualizare mai bună */
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
    </style>
</head>
<body>

<div class="content">
    <h2 style="text-align: center;"><a href="#" target="_blank">Descoperă Produsele Noastre</a></h2>
    <div class="model-and-navigation">
      <h3 id="productTitle">Scaun tapițat</h3>
      <model-viewer id="modelViewer" src="scaun.glb" ios-src="scaun.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="Produsul nostru">
        <button slot="ar-button" class="ar-button">👋 Activează modul AR</button>
      </model-viewer>
      <div class="navigation">
          <button class="nav-button" onclick="changeModel(-1)">⇦ prev</button>
          <button class="nav-button" onclick="changeModel(1)">next ⇨</button>
      </div>
    </div>
    <div class="features" id="productFeatures">
      <p>
          ✔️Produsul nu este montat<br>
          ✔️Asamblarea este rapida si usoara<br>
          ✔️otel acoperit cu pulbere
      </p>
    </div>
    <p><a href="https://manomotion2k24.github.io/Pizza/" class="bold-link" target="_blank">Pizza Quattro Formaggie</a></p>
    <p><a href="https://manomotion2k24.github.io/My-Beloved-Girl/" class="bold-link" target="_blank">Rama Foto Familie</a></p>
    <p><a href="https://manomotion2k24.github.io/cactus/" class="bold-link" target="_blank">Cactus Opuntia Albispina</a></p>
</div>

<script>
  const models = [
    {file: "guler2.glb", title: "Cumpara acum Guler masaj", link: "https://unizdrav.ro/produse/4021/guler-de-masaj-pentru-gat-si-umeri-unizdrav", subtitle: "Guler de masaj pentru gât și umeri", features: "✔️Pornirea și oprirea căldurii, ✔️Schimbarea rotației capetelor de masaj, ✔️3 niveluri de intensitate, ✔️Oprire automată"},
    {file: "scaun.glb", title: "Cumpara acum Scaun sufragerie stofă", link: "https://acaju.ro/products/scaun-tapitat-k365-rosu-52x57x90-cm?gad_source=1", subtitle: "Scaun tapițat", features: "✔️Produsul nu este montat, ✔️Asamblarea este rapida si usoara, ✔️otel acoperit cu pulbere"},
    {file: "Avatar4.glb", title: "", link: "", subtitle: "", features: ""}
  ];
  let currentIndex = 1;

  const viewer = document.getElementById('modelViewer');
  const productTitle = document.getElementById('productTitle');
  const productFeatures = document.getElementById('productFeatures');

  function changeModel(step) {
    currentIndex += step;

    if (currentIndex >= models.length) {
      currentIndex = 0;
    } else if (currentIndex < 0) {
      currentIndex = models.length - 1;
    }

    const model = models[currentIndex];
    viewer.src = model.file;
    viewer.alt = model.subtitle;
    productTitle.innerHTML = `<a href="${model.link}" target="_blank">${model.title}</a>`;
    productFeatures.innerHTML = `<p>${model.features.replace(/, /g, "<br>")}</p>`;
  }

  // Inițializare la încărcare
  window.onload = () => changeModel(0);
</script>

</body>
</html>
