<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulario de Peticiones de Turno</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 700px;
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
        select, input, button {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        select:focus, input:focus {
            border-color: #007bff;
            outline: none;
        }
        button {
            background-color: #007bff;
            color: white;
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
        <h1>Formulario de Peticiones de Turno</h1>
        <form id="peticionesForm">
            <!-- Seleccionar la zona de preferencia -->
            <label>Seleccionar la zona de preferencia</label>
            <select id="zona1" required>
                <option value="" disabled selected>Seleccione una zona</option>
                <option>ALB</option>
                <option>SM1</option>
                <option>VZA</option>
                <option>SM2</option>
                <option>CSU</option>
                <option>NTO</option>
            </select>
            <select id="zona2" required>
                <option value="" disabled selected>Seleccione una zona</option>
                <option>ALB</option>
                <option>SM1</option>
                <option>VZA</option>
                <option>SM2</option>
                <option>CSU</option>
                <option>NTO</option>
            </select>
            <select id="zona3" required>
                <option value="" disabled selected>Seleccione una zona</option>
                <option>ALB</option>
                <option>SM1</option>
                <option>VZA</option>
                <option>SM2</option>
                <option>CSU</option>
                <option>NTO</option>
            </select>
            <select id="zona4" required>
                <option value="" disabled selected>Seleccione una zona</option>
                <option>ALB</option>
                <option>SM1</option>
                <option>VZA</option>
                <option>SM2</option>
                <option>CSU</option>
                <option>NTO</option>
            </select>
            <select id="zona5" required>
                <option value="" disabled selected>Seleccione una zona</option>
                <option>ALB</option>
                <option>SM1</option>
                <option>VZA</option>
                <option>SM2</option>
                <option>CSU</option>
                <option>NTO</option>
            </select>
            <select id="zona6" required>
                <option value="" disabled selected>Seleccione una zona</option>
                <option>ALB</option>
                <option>SM1</option>
                <option>VZA</option>
                <option>SM2</option>
                <option>CSU</option>
                <option>NTO</option>
            </select>

            <!-- Turno preferido de mayor a menor -->
            <label>Turno preferido de mayor a menor</label>
            <select id="turno1" required>
                <option value="" disabled selected>Seleccione un turno</option>
                <option>Turno 1</option>
                <option>Turno 2</option>
                <option>Turno 3</option>
                <option>Turno 4</option>
            </select>
            <select id="turno2" required>
                <option value="" disabled selected>Seleccione un turno</option>
                <option>Turno 1</option>
                <option>Turno 2</option>
                <option>Turno 3</option>
                <option>Turno 4</option>
            </select>
            <select id="turno3" required>
                <option value="" disabled selected>Seleccione un turno</option>
                <option>Turno 1</option>
                <option>Turno 2</option>
                <option>Turno 3</option>
                <option>Turno 4</option>
            </select>
            <select id="turno4" required>
                <option value="" disabled selected>Seleccione un turno</option>
                <option>Turno 1</option>
                <option>Turno 2</option>
                <option>Turno 3</option>
                <option>Turno 4</option>
            </select>

            <!-- Motivo del turno -->
            <label for="motivoTurno">Motivo del turno</label>
            <input type="text" id="motivoTurno" name="motivoTurno" required>

            <!-- Seleccionar la secuencia preferida -->
            <label>Seleccionar la secuencia preferida</label>
            <select id="secuencia1" required>
                <option value="" disabled selected>Seleccione una secuencia</option>
                <option>Secuencia 1</option>
                <option>Secuencia 2</option>
                <option>Secuencia 3</option>
                <option>Secuencia 4</option>
                <option>Secuencia 5</option>
                <option>Secuencia 6</option>
                <option>Secuencia 7</option>
                <option>Secuencia 8</option>
                <option>Secuencia 9</option>
                <option>Secuencia A</option>
                <option>Secuencia B</option>
            </select>

            <!-- Donde reside -->
            <label for="residencia">Donde reside</label>
            <input type="text" id="residencia" name="residencia" required>

            <!-- Dificultad para caminar -->
            <label>¿Dificultad para caminar o estar de pie?</label>
            <select id="dificultad" required>
                <option value="" disabled selected>Seleccione una opción</option>
                <option>Sí</option>
                <option>No</option>
            </select>

            <!-- Cuenta con vehículo -->
            <label>¿Cuenta con vehículo?</label>
            <select id="vehiculo" required>
                <option value="" disabled selected>Seleccione una opción</option>
                <option>Sí</option>
                <option>No</option>
            </select>

            <!-- Botón de enviar -->
            <button type="submit">Enviar</button>
        </form>
        <div class="confirmation" id="confirmationMessage">
            ¡Formulario enviado con éxito!
        </div>
    </div>
    <script>
        const form = document.getElementById('peticionesForm');
        const confirmationMessage = document.getElementById('confirmationMessage');

        form.addEventListener('submit', function(event) {
            event.preventDefault();
            confirmationMessage.style.display = 'block';
            form.reset();
        });
    </script>
</body>
</html>
