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
            font-family: 'Arial', sans-serif; /* Cambia la fuente a una más moderna */
            background-color: #f8f8f8; /* Un fondo más suave */
            color: #333;
            margin: 0;
            line-height: 1.6;
            display: flex;
            flex-direction: column;
            min-height: 100vh; /* Asegura que el footer se pegue al fondo */
        }

        /* Encabezado */
        header {
            background-color: #e91e63; /* Rosa más vibrante */
            color: white;
            padding: 20px;
            text-align: center;
        }

        header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        nav li {
            display: inline-block;
            margin: 0 15px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            padding: 8px 12px; /* Añade padding para mejor clickeabilidad */
            border-radius: 5px; /* Bordes redondeados */
            transition: background-color 0.3s; /* Transición suave */
        }

        nav a:hover {
            background-color: rgba(255, 255, 255, 0.2); /* Rosa más claro al pasar el ratón */
        }

        /* Contenido principal */
        main {
            padding: 20px;
            flex: 1; /* El contenido principal ocupa el espacio disponible */
        }

        section {
            margin-bottom: 30px;
            background-color: white; /* Fondo blanco para las secciones */
            padding: 20px;
            border-radius: 8px; /* Bordes redondeados */
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); /* Sombra ligera */
        }

        section h2 {
            color: #e91e63;
            font-size: 2em;
            margin-bottom: 15px;
            text-align: center;
        }

        /* Galería */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Diseño de galería responsivo */
            gap: 15px;
        }

        .gallery img {
            width: 100%;
            height: auto;
            border-radius: 8px;
            transition: transform 0.3s;
            object-fit: cover; /* Para que las imágenes cubran el contenedor */
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        /* Timeline */
        .timeline {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .timeline-item {
            background-color: #f5f5f5;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .timeline-item h3 {
            margin-bottom: 10px;
            color: #e91e63;
        }

        /* Footer */
        footer {
            background-color: #e91e63;
            color: white;
            text-align: center;
            padding: 15px;
            margin-top: 20px; /* Espacio arriba del footer */
        }

        /* Estilos para dispositivos móviles */
        @media (max-width: 768px) {
            nav li {
                display: block; /* Navegación en vertical */
                margin: 10px 0;
            }

            .gallery {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); /* Galería más compacta */
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>Mi Amor Para Ti</h1>
        <nav>
            <ul>
                <li><a href="#gallery">Galería</a></li>
                <li><a href="#timeline">Nuestra Historia</a></li>
                <li><a href="#test">Test de Compatibilidad</a></li>
                <li><a href="#music">Música</a></li>
                <li><a href="#game">Juego</a></li>
                <li><a href="#calendar">Calendario</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="gallery">
            <h2>Nuestros Mejores Momentos</h2>
            <div class="gallery">
                <img src="foto1.jpg" alt="Momento especial 1">
                <img src="foto2.jpg" alt="Momento especial 2">
                <img src="foto3.jpg" alt="Momento especial 3">
                </div>
        </section>

        <section id="timeline">
            <h2>Nuestra Historia</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <h3>Primer Encuentro</h3>
                    <p>El 14 de febrero de 2024, nuestra historia comenzó...</p>
                </div>
                <div class="timeline-item">
                    <h3>Primer Viaje Juntos</h3>
                    <p>El 20 de agosto de 2024, viajamos a la playa por primera vez.</p>
                </div>
                </div>
        </section>

        <section id="test">
            <h2>Test de Compatibilidad</h2>
            <p>¡Vamos a descubrir cuánto nos conocemos!</p>
            <button onclick="alert('Responde a todas las preguntas con amor :)')">Comenzar Test</button>
        </section>

        <section id="music">
            <h2>Nuestra Canción</h2>
            <audio controls>
                <source src="nuestra-cancion.mp3" type="audio/mp3">
                Tu navegador no soporta el elemento de audio.
            </audio>
        </section>

        <section id="game">
            <h2>Un Juego para Nosotros</h2>
            <button onclick="alert('¡Haz clic y diviértete!')">Jugar</button>
        </section>

        <section id="calendar">
            <h2>Calendario de Fechas Especiales</h2>
            <p>Aquí puedes ver y agregar recordatorios de nuestros momentos especiales.</p>
            <button onclick="alert('Añadir evento especial')">Añadir Evento</button>
        </section>
    </main>

    <footer>
        <p>Creado con ❤️ para ti, Alexa.</p>
    </footer>

</body>
</html>
