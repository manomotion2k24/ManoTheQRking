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
        align-items: flex-start; /* Aliniat la stânga */
        margin-left: 20px; /* Asigură-te că este aliniat corespunzător în conținut */
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
  // Codul JavaScript rămâne neschimbat
</script>

</body>
</html>
