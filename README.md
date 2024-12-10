<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulario de Reporte de Problemas</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f3f4f6;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 500px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .container h1 {
            text-align: center;
            color: #333;
        }
        label {
            font-weight: bold;
            color: #555;
            display: block;
            margin-bottom: 5px;
        }
        input, select, button {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        input:focus, select:focus {
            border-color: #007bff;
            outline: none;
        }
        button {
            background-color: #007bff;
            color: #fff;
            font-size: 16px;
            cursor: pointer;
            border: none;
        }
        button:hover {
            background-color: #0056b3;
        }
        .confirmation {
            display: none;
            color: green;
            font-weight: bold;
            text-align: center;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Reporte de Problemas</h1>
        <form id="reporteForm">
            <!-- Número de tarjeta -->
            <label for="numeroTarjeta">Número de tarjeta</label>
            <input type="text" id="numeroTarjeta" name="numeroTarjeta" placeholder="Ingrese el número de la tarjeta" required>

            <!-- Problema o situación -->
            <label for="problema">Problema o situación</label>
            <select id="problema" name="problema" required>
                <option value="" disabled selected>Seleccione una opción</option>
                <option value="recargaFallida">Recarga fallida</option>
                <option value="noEntregoVuelto">No entregó vuelto</option>
            </select>

            <!-- Hora aproximada y fecha -->
            <label for="horaFecha">Hora y fecha de la situación</label>
            <input type="datetime-local" id="horaFecha" name="horaFecha" required>

            <!-- Estación de la situación -->
            <label for="estacion">Estación de la situación</label>
            <input type="text" id="estacion" name="estacion" placeholder="Ingrese el nombre de la estación" required>

            <!-- Billete insertado -->
            <label for="billete">Billete insertado</label>
            <select id="billete" name="billete" required>
                <option value="" disabled selected>Seleccione un billete</option>
                <option value="1">$1</option>
                <option value="5">$5</option>
                <option value="10">$10</option>
            </select>

            <!-- Número del equipo -->
            <label for="numeroEquipo">Número del equipo</label>
            <input type="text" id="numeroEquipo" name="numeroEquipo" placeholder="Ingrese el número del equipo" required>

            <!-- Botón de enviar -->
            <button type="submit">Enviar</button>
        </form>
        <div class="confirmation" id="confirmationMessage">
            ¡El formulario fue enviado con éxito!
        </div>
    </div>

    <script>
        // Manejo del evento submit del formulario
        const form = document.getElementById('reporteForm');
        const confirmationMessage = document.getElementById('confirmationMessage');

        form.addEventListener('submit', function(event) {
            event.preventDefault(); // Evita el envío tradicional del formulario
            confirmationMessage.style.display = 'block'; // Muestra el mensaje de confirmación
            form.reset(); // Resetea los campos del formulario
        });
    </script>
</body>
</html>
