# aulagit
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Coração Animado</title>
    <style>
        body {
            background-color: black;
            margin: 0;
            overflow: hidden;
            text-align: center;
        }

        h1 {
            justfy-contend:center
            text-aling:center;
            font-family: Arial, sans-serif;
            font-size: 60px;
            margin: 20px 0;
          margin-left:20px;
            background: linear-gradient(270deg, red, orange, yellow, green, blue, indigo, violet);
            background-size: 800% 800%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient 5s ease infinite;
        }

        @keyframes gradient {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }

        canvas {
            display: block;
            margin: auto;
        }
    </style>
</head>
<body>
    
    <canvas id="canvas" width="800" height="600"></canvas>

    <script>
        const canvas = document.getElementById('canvas');
        const ctx = canvas.getContext('2d');

        const cores = ["blue", "skyblue", "pink", "lightblue", "turquoise", "purple", "indigo", "red", "yellow"];

        function desenharCoracao(cor) {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            ctx.fillStyle = cor;

            ctx.beginPath();
            ctx.moveTo(400, 300);
            ctx.bezierCurveTo(400, 200, 600, 200, 600, 300);
            ctx.bezierCurveTo(600, 400, 500, 450, 400, 550);
            ctx.bezierCurveTo(300, 450, 200, 400, 200, 300);
            ctx.bezierCurveTo(200, 200, 400, 200, 400, 300);
            ctx.fill();

            ctx.fillStyle = "white";
            ctx.font = "bold 34px Arial";
            ctx.textAlign = "center";
            ctx.fillText("I love you", 400, 580);
        }

        function batimento() {
            const cor = cores[Math.floor(Math.random() * cores.length)];
            desenharCoracao(cor);
        }

        setInterval(batimento, 350);
  
  
  
    </script>
  
  <br>
  <h1>I love you &#10084;&#65039;
</h1>
</body>
</html>

