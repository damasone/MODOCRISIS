<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modo Crisis - FractaLab</title>
    <link href="https://fonts.googleapis.com/css2?family=Work+Sans:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: #1A1A1A;
            color: #FFFFFF;
            font-family: 'Work Sans', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
        }
        .crisis-container {
            max-width: 800px;
            text-align: center;
        }
        .step {
            display: none;
        }
        .step.active {
            display: block;
        }
        h1 {
            font-size: 36px;
            font-weight: 700;
            margin-bottom: 20px;
            color: #DD2035;
        }
        p {
            font-size: 18px;
            line-height: 1.6;
            margin-bottom: 25px;
        }
        textarea, input, select {
            width: 100%;
            padding: 12px;
            font-size: 16px;
            border: 1px solid #FFFFFF;
            background-color: #2D2D2D;
            color: #FFFFFF;
            margin-bottom: 20px;
            font-family: 'Work Sans', sans-serif;
        }
        textarea {
            height: 120px;
            resize: none;
        }
        button {
            background-color: #DD2035;
            color: #FFFFFF;
            border: none;
            padding: 12px 24px;
            font-size: 16px;
            font-weight: 700;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #B01A2C;
        }
        .highlight {
            color: #DD2035;
            font-weight: 700;
        }
        .warning {
            color: #DD2035;
            font-size: 20px;
            font-weight: 700;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="crisis-container">
        <div class="step active" id="step1">
            <h1>Modo Crisis</h1>
            <p>¿Cómo te sientes en este momento? No pienses mucho, solo escribe.</p>
            <input type="text" id="situation" placeholder="Ejemplo: Estoy al límite...">
            <button onclick="nextStep(2)">Siguiente</button>
        </div>
        
        <div class="step" id="step2">
            <h1>¿Cuánta energía te queda?</h1>
            <p>Del 1 al 10, ¿cuánta fuerza tienes ahora mismo?</p>
            <select id="energy">
                <option value="1-3">Muy poca (1-3)</option>
                <option value="4-6">Media (4-6)</option>
                <option value="7-10">Mucha (7-10)</option>
            </select>
            <button onclick="nextStep(3)">Siguiente</button>
        </div>
        
        <div class="step" id="step3">
            <h1>Detente un momento</h1>
            <p id="breath-text">Respira hondo: inhala 4 segundos, exhala 8. Repite cinco veces.</p>
            <button onclick="nextStep(4)">Siguiente</button>
        </div>
        
        <div class="step" id="step4">
            <h1>¿Qué necesitas ahora?</h1>
            <p>Elige lo que más se acerque a lo que sientes:</p>
            <select id="need">
                <option value="escuchar">Alguien que me escuche</option>
                <option value="espacio">Un momento de calma</option>
                <option value="accion">Hacer algo para cambiar esto</option>
            </select>
            <button onclick="nextStep(5)">Siguiente</button>
        </div>

        <div class="step" id="step5">
            <h1>Tu próximo paso</h1>
            <p id="advice-text">Pequeños pasos crean grandes cambios.</p>
            <button onclick="reset()">Volver a empezar</button>
        </div>
    </div>
    
    <script>
        function nextStep(stepNumber) {
            document.querySelectorAll('.step').forEach(step => step.classList.remove('active'));
            document.getElementById('step' + stepNumber).classList.add('active');
            
            if (stepNumber === 3) {
                let energy = document.getElementById('energy').value;
                let breathText = "Respira hondo: inhala 4 segundos, exhala 8. Repite cinco veces.";
                if (energy === "1-3") {
                    breathText = "Tu cuerpo está tenso. Prueba a moverte un poco después de respirar.";
                } else if (energy === "7-10") {
                    breathText = "Tienes energía dentro de ti. Usa esto para moverte.";
                }
                document.getElementById('breath-text').innerText = breathText;
            }

            if (stepNumber === 5) {
                let need = document.getElementById('need').value;
                let adviceText = "Cada paso cuenta, incluso el más pequeño.";
                if (need === "escuchar") {
                    adviceText = "Habla con alguien en quien confíes, no guardes esto solo.";
                } else if (need === "espacio") {
                    adviceText = "Tómate un momento, cierra los ojos y respira. No tienes que decidir nada ahora.";
                } else if (need === "accion") {
                    adviceText = "Haz algo pequeño ahora: mueve tu cuerpo, bebe agua, sal a caminar.";
                }
                document.getElementById('advice-text').innerText = adviceText;
            }
        }
        
        function reset() {
            document.querySelectorAll('.step').forEach(step => step.classList.remove('active'));
            document.getElementById('step1').classList.add('active');
        }
    </script>
</body>
</html>
