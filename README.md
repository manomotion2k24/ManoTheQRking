<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Demo Modele 3D</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
    <style>
      body {
        margin: 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        min-height: 100vh;
        background-color: #f0f0f0;
      }
      model-viewer {
        width: 90vw; /* Ajustează lățimea după necesități */
        height: 45vh; /* Ajustează înălțimea după necesități */
        margin-bottom: 2vh;
      }
    </style>
</head>
<body>

<model-viewer src="Avatar1.glb" ios-src="Avatar1.usdz" ar camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="Primul model 3D"></model-viewer>

<model-viewer src="Avatar2.glb" ios-src="Avatar2.usdz" ar camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="Al doilea model 3D"></model-viewer>

</body>
</html>
