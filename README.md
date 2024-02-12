<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.3">
    <title>3D Model View</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
</head>
<body>

<!-- Aici adăugăm un paragraf cu un ID pentru a putea fi ascuns sau afișat de script -->
<p id="iosMessage" style="display: none;">Deschide în Safari dacă ești pe Apple</p>

<p><a href="https://vimeo.com/user74836700">Înapoi la pagina produsului</a></p>

<model-viewer src="Avatar1.glb" ios-src="Avatar1.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="A 3D model of an avatar"></model-viewer>

<model-viewer src="Avatar2.glb" ios-src="Avatar2.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="2" alt="An 3D model of a second avatar"></model-viewer>

<model-viewer src="Avatar3.glb" ios-src="Avatar3.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="3" alt="Ann 3D model of a second avatar"></model-viewer>
<script>
    // Functie pentru a verifica daca utilizatorul este pe un dispozitiv iOS
    function checkIfIOS() {
        var iDevices = [
            'iPad Simulator',
            'iPhone Simulator',
            'iPod Simulator',
            'iPad',
            'iPhone',
            'iPod'
        ];

        if (!!navigator.platform) {
            while (iDevices.length) {
                if (navigator.platform === iDevices.pop()){ return true; }
            }
        }

        return false;
    }

    // Dacă este iOS, afișăm mesajul
    if(checkIfIOS()) {
        document.getElementById('iosMessage').style.display = 'block';
    }
</script>

</body>
</html>
