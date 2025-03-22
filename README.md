<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Catch the Goose</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: lightblue;
        }
        #game-container {
            position: relative;
            width: 600px;
            height: 400px;
            margin: 20px auto;
            background-color: white;
            border: 2px solid black;
        }
        #goose {
            position: absolute;
            width: 50px;
            height: auto;
            cursor: pointer;
        }
        .score {
            font-size: 24px;
            font-weight: bold;
        }
    </style>
    <script>
        let score = 0;
        function moveGoose() {
            const goose = document.getElementById("goose");
            const gameContainer = document.getElementById("game-container");
            const maxX = gameContainer.clientWidth - goose.clientWidth;
            const maxY = gameContainer.clientHeight - goose.clientHeight;
            
            const randomX = Math.floor(Math.random() * maxX);
            const randomY = Math.floor(Math.random() * maxY);
            
            goose.style.left = `${randomX}px`;
            goose.style.top = `${randomY}px`;
        }
        
        function catchGoose() {
            score++;
            document.getElementById("score").textContent = `Score: ${score}`;
            moveGoose();
        }

        function openGameInNewTab() {
            window.open('CatchTheGoose.html', '_blank');
        }
        
        window.onload = function() {
            moveGoose();
        };
    </script>
</head>
<body>
    <h1>Catch the Goose!</h1>
    <p class="score" id="score">Score: 0</p>
    <div id="game-container">
        <img id="goose" src="home_goose_on_a_transparent_background__by_zoostock_dcfnphr-fullview.png" alt="Goose" onclick="catchGoose()">
    </div>
    <br>
    <button onclick="openGameInNewTab()">Catch the Goose</button>
    <br>
    <a href="index.html">Back to Home</a>
</body>
</html>
