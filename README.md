<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D Model Viewer</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer@latest"></script>
    <style>
      body {
        margin: 0;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        background: linear-gradient(145deg, rgba(255,255,255,1) 0%, rgba(229,229,229,1) 100%);
      }

      model-viewer {
        width: 100%; /* Ensure model-viewer takes full width */
        height: 100%; /* Ensure model-viewer takes full height */
        --poster-color: transparent;
      }

      /* Style the AR button */
      model-viewer::part(ar-button) {
        position: fixed; /* Fix the button relative to the viewport */
        top: 16px; /* Position the button 16px from the top of the viewport */
        right: 16px; /* Position the button 16px from the right of the viewport */
        z-index: 10; /* Ensure the button is above other page elements */
      }
    </style>
</head>
<body>
    <model-viewer src="Avatar1.glb" ios-src="Avatar1.usdz" alt="A 3D model of an avatar" ar ar-modes="webxr scene-viewer quick-look" environment-image="neutral" auto-rotate camera-controls></model-viewer>
</body>
</html>
