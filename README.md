
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi amor, esta es para ti</title>
    <style>
@import url('https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;400;700&display=swap');

:root {
    --bg-light: #ffe6f2;
    --bg-dark: #1a1a2e;
    --text-light: #000;
    --text-dark: #fff;
    --card-light: rgba(255, 255, 255, 0.8);
    --card-dark: rgba(255, 255, 255, 0.15);
}

body {
    font-family: 'Poppins', sans-serif;
    margin: 0;
    padding: 0;
    background: linear-gradient(135deg, #ff758c, #ff7eb3);
    color: white;
    overflow-x: hidden;
    transition: all 0.3s ease;
}

body.dark-mode {
    background: var(--bg-dark);
    color: var(--text-dark);
}

h1, h2, p {
    text-align: center;
    animation: fadeIn 2s;
}

h1 {
    font-family: 'Pacifico', cursive;
    font-size: 3em;
    margin-top: 50px;
    color: #fff8f8;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.4);
}

.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 50px;
}

.card {
    background: var(--card-light);
    border-radius: 15px;
    padding: 20px;
    width: 300px;
    margin: 20px;
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    backdrop-filter: blur(10px);
}

body.dark-mode .card {
    background: var(--card-dark);
}

.card:hover {
    transform: translateY(-10px);
}

.button {
    background-color: #ff5f7f;
    border: none;
    color: white;
    padding: 15px 32px;
    font-size: 1.2em;
    cursor: pointer;
    border-radius: 10px;
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
    background: var(--bg-dark);
    color: var(--text-dark);
}

/* Modo claro */
body.light-mode {
    background: var(--bg-light);
    color: var(--text-light);
}

.toggle-mode {
    position: fixed;
    top: 20px;
    right: 20px;
    background: #ff5f7f;
    color: white;
    border: none;
    padding: 10px 20px;
    cursor: pointer;
    border-radius: 10px;
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

<!-- Juego interactivo mejorado -->
<div class="game-container">
    <h2>¡Un juego sobre nosotros!</h2>
    <p>¿Cuánto recuerdas sobre nuestra relación? Responde las preguntas con cariño. <3</p>
    
    <div id="question1">
        <p><strong>Pregunta 1:</strong> ¿Dónde fue nuestra primera cita?</p>
        <button onclick="checkAnswer('question1', 'Parque')">En el parque</button>
        <button onclick="checkAnswer('question1', 'Restaurante')">En el restaurante</button>
        <button onclick="checkAnswer('question1', 'Cine')">En el cine</button>
        <button onclick="giveHint('question1')">Pista</button>
        <div id="hint1" style="display:none; color: green;">Es un lugar al aire libre donde pasamos mucho tiempo.</div>
    </div>

    <div id="question2" style="display:none;">
        <p><strong>Pregunta 2:</strong> ¿Qué canción bailamos en nuestra primera cita?</p>
        <button onclick="checkAnswer('question2', 'Perfect de Ed Sheeran')">Perfect de Ed Sheeran</button>
        <button onclick="checkAnswer('question2', 'Shape of You')">Shape of You</button>
        <button onclick="checkAnswer('question2', 'La Vie en Rose')">La Vie en Rose</button>
        <button onclick="giveHint('question2')">Pista</button>
        <div id="hint2" style="display:none; color: green;">Es una canción romántica de Ed Sheeran.</div>
    </div>

    <div id="question3" style="display:none;">
        <p><strong>Pregunta 3:</strong> ¿Cuál es el lugar que soñamos visitar juntos?</p>
        <button onclick="checkAnswer('question3', 'París')">París</button>
        <button onclick="checkAnswer('question3', 'Tokio')">Tokio</button>
        <button onclick="checkAnswer('question3', 'Roma')">Roma</button>
        <button onclick="giveHint('question3')">Pista</button>
        <div id="hint3" style="display:none; color: green;">Es la ciudad del amor.</div>
    </div>

    <div id="question4" style="display:none;">
        <p><strong>Pregunta 4:</strong> ¿Qué animal te recuerda a mí cuando te cuento historias divertidas?</p>
        <button onclick="checkAnswer('question4', 'Un perro')">Un perro</button>
        <button onclick="checkAnswer('question4', 'Un gato')">Un gato</button>
        <button onclick="checkAnswer('question4', 'Un elefante')">Un elefante</button>
        <button onclick="giveHint('question4')">Pista</button>
        <div id="hint4" style="display:none; color: green;">Es un animal amigable que siempre está feliz.</div>
    </div>

    <div id="endGame" style="display:none;">
        <h3>¡Felicidades, has completado el juego!</h3>
        <p>Ahora sabes cuánto nos conocemos. <3</p>
        <button onclick="showSurprise()">¡Abre tu sorpresa!</button>
    </div>
    
    <div id="surprise" style="display:none;">
        <h2>Tu sorpresa:</h2>
        <p>Te amo mucho, mi vida. Cada día a tu lado es un regalo. 💖</p>
        <img id="surpriseImage" src="https://via.placeholder.com/300" alt="Imagen sorpresa" />
    </div>
</div>

<script>
    // Función para verificar la respuesta
    function checkAnswer(questionId, answer) {
        const correctAnswers = {
            'question1': 'Parque',
            'question2': 'Perfect de Ed Sheeran',
            'question3': 'París',
            'question4': 'Un perro'
        };

        const nextQuestion = {
            'question1': 'question2',
            'question2': 'question3',
            'question3': 'question4',
            'question4': 'endGame'
        };

        const hintId = `hint${questionId.charAt(questionId.length - 1)}`;
        
        if (answer === correctAnswers[questionId]) {
            alert('¡Respuesta correcta! <3');
            document.getElementById(questionId).style.display = 'none';
            document.getElementById(nextQuestion[questionId]).style.display = 'block';
        } else {
            alert('Respuesta incorrecta, inténtalo de nuevo.');
        }
    }

    // Función para mostrar las pistas
    function giveHint(questionId) {
        const hint = document.getElementById(`hint${questionId.charAt(questionId.length - 1)}`);
        hint.style.display = 'block';
    }

    // Función para mostrar la sorpresa final
    function showSurprise() {
        document.getElementById('surprise').style.display = 'block';
        document.getElementById('surpriseImage').src = 'https://via.placeholder.com/600x400';  // Aquí puedes poner la imagen personalizada que desees
    }
</script>


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
 
