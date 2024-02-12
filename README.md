<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.3">
    <title>3D Model View</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
    <style>
        body {
            perspective: 1000px;
        }
        #iosMessage, #androidMessage {
            display: none;
            animation: rotateX360 30s linear infinite;
            transform-style: preserve-3d;
            font-weight: bold;
            text-shadow: 1px 1px 2px #000;
        }
        @keyframes rotateX360 {
            from {
                transform: rotateX(0deg);
            }
            to {
                transform: rotateX(360deg);
            }
        }
        .ar-instruction {
            text-align: center;
            font-size: 16px;
            margin-top: 10px;
        }
    </style>
</head>
<body>

<p id="iosMessage">Model 3D</p>
<p id="iosMessage">Deschide în Safari dacă ești pe Apple</p>
<p id="androidMessage">Model 3D</p>

<p><a href="https://vimeo.com/user74836700">Înapoi la pagina produsului</a></p>

<model-viewer src="Avatar4.glb" ios-src="Avatar4.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="4" alt="A 3D model of an avatar"></model-viewer>
<p class="ar-instruction">Apasă pe acest buton pentru a vedea produsul în camera ta ↑</p>

<!-- Adaugă aici orice alte <model-viewer> și <p class="ar-instruction"> pentru modelele tale 3D suplimentare -->

<script>
    // Functie pentru a verifica daca utilizatorul este pe un dispozitiv iOS sau Android
    function showMessageBasedOnOS() {
        var ua = navigator.userAgent || navigator.vendor || window.opera;
        if (/iPad|iPhone|iPod/.test(ua) && !window.MSStream) {
            document.getElementById('iosMessage').style.display = 'block';
        } else if (/android/i.test(ua)) {
            document.getElementById('androidMessage').style.display = 'block';
        }
    }
    showMessageBasedOnOS();
</script>

</body>
</html>
