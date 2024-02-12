<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.4">
    <title>3D Model View</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
    <style>
        body {
            perspective: 1000px;
        }
        #iosMessage, #androidMessage {
            display: none;
            animation: rotateX180 10s linear infinite;
            transform-style: preserve-3d;
            font-weight: bold;
            text-shadow: 3px 3px 4px #000;
        }
        @keyframes rotateX180 {
            from {
                transform: rotateX(0deg);
            }
            to {
                transform: rotateX(180deg);
            }
        }
        .ar-instruction {
            text-align: center;
            font-size: 16px;
            margin-top: 10px;
        }
        .ar-instruction-ios {
            display: none;
        }
    </style>
</head>
<body>

<p id="iosMessage">Deschide în Safari dacă ești pe Apple <br> Model 3D</p>
<p id="androidMessage">Apasati pe butonul din coltul drept al imaginii pentru a vedea in spatiul dumneavoastra</p>

<p><a href="https://vimeo.com/user74836700">Înapoi la pagina produsului</a></p>

<model-viewer src="Avatar4.glb" ios-src="Avatar4.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="4" alt="A 3D model of an avatar"></model-viewer>
<p class="ar-instruction">Apasă pe acest buton pentru a vedea produsul în camera ta ↑</p>
<p class="ar-instruction-ios">Apasă pe acest buton pentru a vedea ↑ produsul în camera ta</p>

<script>
    // Functie pentru a verifica daca utilizatorul este pe un dispozitiv iOS sau Android
    function showMessageBasedOnOS() {
        var ua = navigator.userAgent || navigator.vendor || window.opera;
        if (/iPad|iPhone|iPod/.test(ua) && !window.MSStream) {
            document.getElementById('iosMessage').style.display = 'block';
            var iosInstructions = document.getElementsByClassName('ar-instruction-ios');
            for (var i = 0; i < iosInstructions.length; i++) {
                iosInstructions[i].style.display = 'block';
            }
            var androidInstructions = document.getElementsByClassName('ar-instruction');
            for (var i = 0; i < androidInstructions.length; i++) {
                androidInstructions[i].style.display = 'none';
            }
        } else if (/android/i.test(ua)) {
            document.getElementById('androidMessage').style.display = 'block';
        }
    }
    showMessageBasedOnOS();
</script>

</body>
</html>
