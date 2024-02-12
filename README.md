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
            animation: rotate360 3s linear infinite;
            transform: rotateX(20deg) rotateY(10deg);
            font-weight: bold;
            text-shadow: 1px 1px 2px #000;
        }
        @keyframes rotate360 {
            from {
                transform: rotateX(20deg) rotateY(10deg);
            }
            to {
                transform: rotateX(360deg) rotateY(360deg);
            }
        }
    </style>
</head>
<body>

<p id="iosMessage">Deschide în Safari dacă ești pe Apple</p>
<p id="androidMessage">Apasati pe butonul din coltul drept al imaginii pentru a vedea in spatiul dumneavoastra</p>

<p><a href="https://vimeo.com/user74836700">Înapoi la pagina produsului</a></p>

<model-viewer src="Avatar1.glb" ios-src="Avatar1.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="A 3D model of an avatar"></model-viewer>
<!-- Adaugă aici celelalte <model-viewer> pentru modelele tale 3D -->

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
