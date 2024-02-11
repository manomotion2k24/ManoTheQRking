<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AR Web Demo</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
    <style>
        body { margin: 0; }
        model-viewer {
            width: 100vw;
            height: 100vh;
        }
        .ar-button {
            display: none;
        }
        model-viewer[ar-status="not-presenting"] .ar-button {
            display: block;
            position: absolute;
            bottom: 10%;
            left: 50%;
            transform: translateX(-50%);
            padding: 10px 20px;
            font-size: 18px;
            background-color: #0008;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>

<model-viewer src="avatar1.glb" ar ios-src="avatar1.usdz" camera-controls environment-image="neutral" auto-rotate shadow-intensity="1" alt="A 3D model of an avatar">
    <button slot="ar-button" class="ar-button">View in your space</button>
</model-viewer>

<script>
    // Personalizează comportamentul butonului AR dacă este necesar
</script>

</body>
</html>
