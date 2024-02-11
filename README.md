Deschide link-ul in Safari daca ai Iphone
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D Model View</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
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
            width: 60%; /* Ajustează acest procentaj în funcție de dimensiunea dorită */
            height: 80%; /* Ajustează acest procentaj în funcție de dimensiunea dorită */
        }
    </style>
</head>
<body>

<model-viewer src="Avatar1.glb" ios-src="Avatar1.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="A 3D model of an avatar"></model-viewer>

</body>
</html>
