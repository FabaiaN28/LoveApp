<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Una página web interactiva llena de amor para mi novia, con fotos, música, juegos y más.">
    <meta name="keywords" content="amor, pareja, galería de fotos, música, juego, test de compatibilidad, cartas de amor">
    <title>Mi Amor Para Ti, Alexa</title>
    <style>
        /* Estilos generales */
        body {
            font-family: "Arial", sans-serif; /* Cambia la fuente a una más moderna */
            background-color: #F8F8F8; /* Un fondo más suave */
            color: #333;
            margin: 0;
            line-height: 1.6;
            display: flex;
            flex-direction: column;
            min-height: 100vh; /* Asegura que el footer se pegue al fondo */
        }
        
        header {
            background-color: #FF69B4; /* Un color rosa suave para el encabezado */
            color: white;
            padding: 20px;
            text-align: center;
        }
        
        main {
            padding: 20px;
            flex: 1; /* El contenido principal ocupa el espacio disponible */
        }
        
        footer {
            background-color: #333;
            color: white;
            padding: 10px;
            text-align: center;
        }
        
        /* Estilos para la galería de fotos */
        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        
        .gallery img {
            width: 200px;
            height: 200px;
            margin: 10px;
            border-radius: 5px;
            object-fit: cover; /* Para que las fotos se vean completas en el contenedor */
        }
        
        /* Estilos para el reproductor de música */
        .music-player {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .music-player audio {
            width: 100%;
            margin-bottom: 10px;
        }
        
        /* Estilos para el juego */
        .game {
            text-align: center;
        }
        
        .game button {
            padding: 10px 20px;
            background-color: #FF69B4;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        
        /* Estilos para el test de compatibilidad */
        .compatibility-test {
            text-align: center;
        }
        
        .compatibility-test input {
            margin: 10px;
        }
        
        .compatibility-test button {
            padding: 10px 20px;
            background-color: #FF69B4;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        
        /* Estilos para las cartas de amor */
        .love-letters {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .love-letters textarea {
            width: 80%;
            height: 200px;
            margin-bottom: 10px;
        }
        
        .love-letters button {
            padding: 10px 20px;
            background-color: #FF69B4;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>Mi Amor Para Ti, Alexa</h1>
    </header>
    <main>
        <section id="photos">
            <h2>Galería de Fotos</h2>
            <div class="gallery">
                <img src="foto1.jpg" alt="Foto 1">
                <img src="foto2.jpg" alt="Foto 2">
                <img src="foto3.jpg" alt="Foto 3">
                </div>
        </section>
        <section id="music">
            <h2>Música</h2>
            <div class="music-player">
                <audio controls>
                    <source src="musica.mp3" type="audio/mpeg">
                    Tu navegador no soporta la reproducción de audio.
                </audio>
            </div>
        </section>
        <section id="game">
            <h2>Juego</h2>
            <div class="game">
                <button>Jugar</button>
            </div>
        </section>
        <section id="compatibility">
            <h2>Test de Compatibilidad</h2>
            <div class="compatibility-test">
                <input type="text" placeholder="Tu nombre">
                <input type="text" placeholder="Su nombre">
                <button>Calcular</button>
            </div>
        </section>
        <section id="love-letters">
            <h2>Cartas de Amor</h2>
            <div class="love-letters">
                <textarea placeholder="Escribe tu carta de amor aquí..."></textarea>
                <button>Enviar</button>
            </div>
        </section>
    </main>
    <footer>
        <p>Hecho con amor para Alexa</p>
    </footer>
</body>
</html>
