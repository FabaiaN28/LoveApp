<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi amor, esta es para ti</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #ff758c, #ff7eb3);
            color: white;
            overflow-x: hidden;
            transition: background-color 0.5s;
        }
        h1, h2, p {
            text-align: center;
            animation: fadeIn 2s;
        }
        h1 {
            font-size: 3em;
            margin-top: 50px;
            color: #fff8f8;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.4);
        }
        .button {
            background-color: #ff5f7f;
            border: none;
            color: white;
            padding: 15px 32px;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 5px;
            transition: transform 0.3s, background-color 0.3s;
            margin-top: 20px;
        }
        .button:hover {
            transform: scale(1.1);
            background-color: #ff7eb3;
        }
        .album-container, .reasons-container, .calendar-container, .box-container, .game-container {
            display: none;
            text-align: center;
        }
        .photo-gallery img {
            width: 150px;
            height: 150px;
            margin: 10px;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .photo-gallery img:hover {
            transform: scale(1.1);
        }
        .reason {
            margin: 20px;
            padding: 15px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            display: inline-block;
        }
        .reason img {
            width: 50px;
            height: 50px;
            margin-right: 10px;
        }
        .modal, .calendar-modal, .box-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            justify-content: center;
            align-items: center;
            color: white;
        }
        .modal-content, .calendar-content, .box-content {
            background-color: #333;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            max-width: 400px;
            width: 90%;
        }
        .modal img, .calendar img {
            width: 100%;
            height: auto;
        }
        .modal .close, .calendar .close, .box .close {
            color: #fff;
            font-size: 2em;
            position: absolute;
            top: 10px;
            right: 10px;
            cursor: pointer;
        }
        .music-btn {
            position: fixed;
            bottom: 20px;
            left: 20px;
            background-color: #ff7eb3;
            border: none;
            padding: 10px 15px;
            color: white;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 5px;
        }
        .light-dark-btn {
            position: fixed;
            top: 20px;
            left: 20px;
            background-color: #333;
            color: white;
            border: none;
            padding: 10px;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 5px;
        }
        .light-dark-btn:hover {
            background-color: #555;
        }
        @keyframes fadeIn {
            0% {
                opacity: 0;
            }
            100% {
                opacity: 1;
            }
        }
        /* Modo oscuro */
        body.dark-mode {
            background: #333;
            color: #f1f1f1;
        }
        /* Modo claro */
        body.light-mode {
            background: #ff758c;
            color: #333;
        }
    </style>
</head>
<body>

    <!-- Página de inicio -->
    <h1>Mi amor, esta es para ti</h1>
    <p>Bienvenida a un lugar creado solo para ti, mi razón de sonreír todos los días.</p>
    <button class="button" id="discoverBtn">Descubre mi sorpresa</button>

    <!-- Modo claro/oscuro -->
    <button class="light-dark-btn" id="modeBtn">Modo Oscuro</button>

    <!-- Álbum de recuerdos -->
    <div class="album-container">
        <h2>Recuerdos Juntos</h2>
        <div class="photo-gallery">
            <img src="https://via.placeholder.com/150" alt="Imagen 1" onclick="openModal('Recuerdo 1')">
            <img src="https://via.placeholder.com/150" alt="Imagen 2" onclick="openModal('Recuerdo 2')">
            <img src="https://via.placeholder.com/150" alt="Imagen 3" onclick="openModal('Recuerdo 3')">
        </div>
    </div>

    <!-- Razones por las que te amo -->
    <div class="reasons-container">
        <h2>Razones por las que te amo</h2>
        <div class="reason">
            <img src="https://via.placeholder.com/50" alt="Razón 1">
            <p>Me haces sentir feliz incluso en los días más grises.</p>
        </div>
        <div class="reason">
            <img src="https://via.placeholder.com/50" alt="Razón 2">
            <p>Tu sonrisa ilumina mi mundo.</p>
        </div>
    </div>

    <!-- Calendario personalizado -->
    <div class="calendar-container">
        <h2>Calendario de momentos especiales</h2>
        <div class="calendar">
            <p>¡Haz clic en una fecha para ver un recuerdo!</p>
        </div>
    </div>

    <!-- Caja de sorpresas -->
    <div class="box-container">
        <h2>Caja de Sorpresas</h2>
        <button onclick="openBoxModal()">¡Abrir caja!</button>
    </div>

    <!-- Juego interactivo -->
    <div class="game-container">
        <h2>Juego sobre nuestra relación</h2>
        <p>¿Dónde fue nuestra primera cita?</p>
        <button onclick="alert('¡Correcto!')">En el parque</button>
        <button onclick="alert('¡Incorrecto!')">En la playa</button>
    </div>

    <!-- Modal para fotos -->
    <div class="modal" id="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <p id="modalMessage"></p>
        </div>
    </div>

    <!-- Modal para caja -->
    <div class="box-modal" id="boxModal">
        <div class="box-content">
            <span class="close" onclick="closeBoxModal()">&times;</span>
            <p>¡Te amo mucho!</p>
        </div>
    </div>

    <!-- Música de fondo -->
    <audio id="backgroundMusic" loop>
        <source src="https://www.bensound.com/bensound-music/bensound-lovely.mp3" type="audio/mp3">
    </audio>
    <button class="music-btn" onclick="toggleMusic()">Reproducir música</button>

    <script>
        // Modo oscuro y claro
        const modeBtn = document.getElementById('modeBtn');
        const body = document.body;
        modeBtn.addEventListener('click', () => {
            if (body.classList.contains('dark-mode')) {
                body.classList.remove('dark-mode');
                body.classList.add('light-mode');
                modeBtn.textContent = 'Modo Claro';
            } else {
                body.classList.remove('light-mode');
                body.classList.add('dark-mode');
                modeBtn.textContent = 'Modo Oscuro';
            }
        });

        // Mostrar la sorpresa
        document.getElementById('discoverBtn').addEventListener('click', () => {
            document.querySelector('.album-container').style.display = 'block';
            document.querySelector('.reasons-container').style.display = 'block';
            document.querySelector('.calendar-container').style.display = 'block';
            document.querySelector('.box-container').style.display = 'block';
            document.querySelector('.game-container').style.display = 'block';
        });

        // Modal para imágenes
        function openModal(message) {
            document.getElementById('modal').style.display = 'flex';
            document.getElementById('modalMessage').textContent = message;
        }

        function closeModal() {
            document.getElementById('modal').style.display = 'none';
        }

        // Caja de sorpresas
        function openBoxModal() {
            document.getElementById('boxModal').style.display = 'flex';
        }

        function closeBoxModal() {
            document.getElementById('boxModal').style.display = 'none';
        }

        // Música
        function toggleMusic() {
            const music = document.getElementById('backgroundMusic');
            if (music.paused) {
                music.play();
            } else {
                music.pause();
            }
        }
    </script>

</body>
</html>
