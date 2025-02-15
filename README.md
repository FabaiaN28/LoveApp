
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Aplicación Web</title>
    <style>
        /* Estilos CSS */
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }
        header {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
        }
        main {
            padding: 20px;
        }
        #miBoton {
            padding: 10px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>Mi Aplicación Web</h1>
    </header>
    <main>
        <p>¡Bienvenido a mi aplicación web!</p>
        <button id="miBoton">Haz clic aquí</button>
    </main>
    <script>
        // Funciones JavaScript
        const miBoton = document.getElementById('miBoton');
        miBoton.addEventListener('click', () => {
            alert('¡Hola desde JavaScript!');
        });
    </script>
</body>
</html>
