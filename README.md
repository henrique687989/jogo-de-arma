<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jogo de Tiro</title>
    <style>
        canvas {
            border: 1px solid black;
            display: block;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <canvas id="gameCanvas" width="800" height="600"></canvas>

    <script>
        // Obtenha o contexto do canvas
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');

        // Definir a nave do jogador
        const player = {
            x: canvas.width / 2,
            y: canvas.height - 30,
            width: 50,
            height: 50,
            color: 'blue',
            speed: 5
        };

        // Função para desenhar a nave do jogador
        function drawPlayer() {
            ctx.fillStyle = player.color;
            ctx.fillRect(player.x, player.y, player.width, player.height);
        }

        // Função para atualizar a posição do jogador
        function updatePlayerPosition() {
            // Adicionar código para mover o jogador com as teclas de seta ou WASD
        }

        // Função principal do jogo
        function main() {
            // Limpar o canvas
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            // Atualizar e desenhar o jogador
            updatePlayerPosition();
            drawPlayer();

            // Chamar a função principal novamente
            requestAnimationFrame(main);
        }

        // Começar o jogo
        main();
    </script>
</body>
</html>
