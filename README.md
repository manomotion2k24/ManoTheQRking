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
            animation: rotateAnimation 6s linear infinite; /* Durata totală ajustată pentru a permite întoarcerea la 0 grade */
            transform-style: preserve-3d;
            font-weight: bold;
            text-shadow: 3px 3px 4px #000;
        }
        @keyframes rotateYInfinitely {
            from {
                transform: rotateY(0);
            }
            to {
                transform: rotateY(360deg);
            }
        }
        .bounce {
            display: inline-block;
            animation: bounce 1s infinite;
        }
        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-5px);
            }
        }
    </style>
</head>
<body>

<p id="iosMessage">Model 3D</p>
<p id="androidMessage">Model 3D</p>

<p><a href="https://vimeo.com/user74836700">Înapoi la pagina produsului</a></p>

<model-viewer src="Avatar4.glb" ios-src="Avatar4.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="4" alt="A 3D model of an avatar"></model-viewer>

<p id="arInstructionAndroid" style="display:none;">Apasă pe acest buton pentru a vedea <span class="bounce">↑</span> produsul în camera ta.</p>
<p id="arInstructionIOS" style="display:none;">Apasă pe acest buton pentru a vedea <span class="bounce">↑</span> produsul în camera ta.</p>

<script>
    function showMessageBasedOnOS() {
        var ua = navigator.userAgent || navigator.vendor || window.opera;
        if (/iPad|iPhone|iPod/.test(ua) && !window.MSStream) {
            document.getElementById('iosMessage').style.display = 'block';
            document.getElementById('arInstructionIOS').style.display = 'block';
            document.getElementById('androidMessage').style.display = 'none';
        } else if (/android/i.test(ua)) {
            document.getElementById('androidMessage').style.display = 'block';
            document.getElementById('arInstructionAndroid').style.display = 'block';
            document.getElementById('iosMessage').style.display = 'none';
        }
    }
    showMessageBasedOnOS();
</script>

</body>
</html>
