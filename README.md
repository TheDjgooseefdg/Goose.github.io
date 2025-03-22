<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goose Unblocked Games</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            background: linear-gradient(45deg, lightblue, lightgreen);
            background-size: 400% 400%;
            animation: gradientAnimation 10s infinite alternate;
            color: lightblue;
        }
        @keyframes gradientAnimation {
            0% {
                background-position: 0% 0%;
                color: darkgreen;
            }
            100% {
                background-position: 100% 100%;
                color: lightblue;
            }
        }
        h1, p, .clock {
            transition: color 1s ease-in-out;
        }
        img {
            max-width: 200px;
            height: auto;
            display: block;
            margin: 0 auto 20px auto;
        }
        .clock-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }
        .clock {
            font-size: 18px;
            font-weight: bold;
        }
        .game-link {
            display: inline-block;
            margin-top: 20px;
            padding: 10px 20px;
            background-color: darkgreen;
            color: white;
            text-decoration: none;
            font-size: 18px;
            border-radius: 5px;
        }
    </style>
    <script>
        function updateClocks() {
            const timeZones = {
                "New York": "America/New_York",
                "London": "Europe/London",
                "Tokyo": "Asia/Tokyo",
                "Sydney": "Australia/Sydney"
            };
            
            const isDark = window.getComputedStyle(document.body).color === "rgb(0, 100, 0)";
            const textColor = isDark ? "lightblue" : "darkgreen";
            
            document.querySelectorAll(".clock").forEach(clock => {
                clock.style.color = textColor;
            });
            
            for (const [city, zone] of Object.entries(timeZones)) {
                const time = new Date().toLocaleTimeString("en-US", { timeZone: zone });
                document.getElementById(city).textContent = `${city}: ${time}`;
            }
        }
        
        setInterval(updateClocks, 1000);
    </script>
</head>
<body onload="updateClocks()">
    <div class="clock-container">
        <div class="clock" id="New York"></div>
        <div class="clock" id="London"></div>
        <div class="clock" id="Tokyo"></div>
        <div class="clock" id="Sydney"></div>
    </div>
    <img src="home_goose_on_a_transparent_background__by_zoostock_dcfnphr-fullview.png" alt="Goose">
    <h1>Welcome to Goose Unblocked Games</h1>
    <p>This is a simple HTML page.</p>
    
    <a href="game.html" class="game-link">Play Catch the Goose</a>
</body>
</html>
