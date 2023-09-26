#   🦈 [simple_pop-up](https://noisk8.github.io/simple_pop-up/) 🦈
~~~
<!DOCTYPE html> <!-- Declaración del tipo de documento HTML -->
<html lang="en"> <!-- Apertura del elemento HTML con el atributo 'lang' para el idioma (inglés) -->
<head>
    <meta charset="UTF-8"> <!-- Declaración de la codificación de caracteres UTF-8 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Configuración de la escala inicial para dispositivos móviles -->
    <title>Pop-up de Podcast</title> <!-- Título de la página en la pestaña del navegador -->
    <style>
        /* Estilos CSS dentro de la etiqueta 'style' */

        /* Estilos para el fondo oscuro */
        .overlay { /* Selector de clase CSS */
            display: none; /* No mostrar el elemento inicialmente */
            position: fixed; /* Posición fija en la ventana del navegador */
            top: 0; /* En la parte superior */
            left: 0; /* En la parte izquierda */
            width: 100%; /* Ancho del 100% de la ventana */
            height: 100%; /* Altura del 100% de la ventana */
            background-color: rgba(0, 0, 0, 0.7); /* Color de fondo negro con transparencia */
            z-index: 1; /* Capa en la parte superior */
        }

        /* Estilos para la tarjeta pop-up */
        .popup { /* Selector de clase CSS */
            display: none; /* No mostrar el elemento inicialmente */
            position: fixed; /* Posición fija en la ventana del navegador */
            top: 50%; /* En el centro verticalmente */
            left: 50%; /* En el centro horizontalmente */
            transform: translate(-50%, -50%); /* Centrar la tarjeta */
            background-image: url('tu-imagen-de-fondo-con-transparencia.png'); /* Imagen de fondo con transparencia */
            background-size: cover; /* Ajustar la imagen de fondo al tamaño de la tarjeta */
            background-repeat: no-repeat; /* No repetir la imagen de fondo */
            background-position: center; /* Centrar la imagen de fondo */
            padding: 20px; /* Espaciado interior */
            z-index: 2; /* Capa en la parte superior */
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.3); /* Sombra */
            width: 90%; /* Ancho del 90% de la ventana */
            max-width: 400px; /* Ancho máximo */
            text-align: center; /* Texto centrado */
            color: #fff; /* Color de texto blanco */
        }

        /* ... (otros estilos) ... */

        /* Hacer que la tarjeta pop-up sea responsive */
        @media (max-width: 768px) { /* Estilos para dispositivos con ancho máximo de 768px */
            .popup { /* Selector de clase CSS */
                width: 90%; /* Ancho del 90% de la ventana */
            }
        }
    </style>
</head>
<body>
    <!-- Cuerpo del documento HTML -->
    <!-- Fondo oscuro y tarjeta pop-up -->
    <div class="overlay" id="overlay"></div> <!-- Div para el fondo oscuro -->
    <div class="popup" id="popup"> <!-- Div para la tarjeta pop-up -->
        <span class="close" onclick="closePopup()">&times;</span> <!-- Botón de cierre (X) -->
        <h2>Promoción de Podcast</h2> <!-- Título -->
        <!-- Espacio para la imagen con transparencia -->
        <img src="tu-imagen-con-transparencia.png" alt="Imagen del Podcast" style="max-width: 100%; margin: 10px 0;">
        <p>¡Descubre nuestro nuevo podcast! Escucha episodios emocionantes sobre temas interesantes.</p> <!-- Párrafo -->
        <!-- Botón decorado con transparencia -->
        <a href="https://tu-podcast.com" target="_blank" class="btn">Visitar el Podcast</a>
    </div>

    <!-- Script JavaScript para la funcionalidad del pop-up -->
    <script>
        // Función para mostrar el pop-up automáticamente después de 5 segundos
        setTimeout(function() {
            document.getElementById('overlay').style.display = 'block'; // Mostrar el fondo oscuro
            document.getElementById('popup').style.display = 'block'; // Mostrar la tarjeta pop-up
        }, 5000); // Esperar 5000 milisegundos (5 segundos)

        // Función para cerrar el pop-up
        function closePopup() {
            document.getElementById('overlay').style.display = 'none'; // Ocultar el fondo oscuro
            document.getElementById('popup').style.display = 'none'; // Ocultar la tarjeta pop-up
        }
    </script>
</body>
</html>

~~~
