<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RC Car Controller</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
        }
        .controls {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            margin-top: 20px;
        }
        .btn {
            padding: 15px 30px;
            font-size: 20px;
            cursor: pointer;
        }
        .speed-slider {
            width: 80%;
        }
    </style>
</head>
<body>
    <h1>RC Car Controller</h1>
    <div class="controls">
        <button class="btn" onclick="sendCommand('forward')">⬆ Forward</button>
        <div>
            <button class="btn" onclick="sendCommand('left')">⬅ Left</button>
            <button class="btn" onclick="sendCommand('stop')">⏹ Stop</button>
            <button class="btn" onclick="sendCommand('right')">➡ Right</button>
        </div>
        <button class="btn" onclick="sendCommand('backward')">⬇ Backward</button>
        <input type="range" class="speed-slider" min="0" max="100" value="50" oninput="sendSpeed(this.value)">
        <p>Speed: <span id="speedValue">50</span>%</p>
    </div><script>
    function sendCommand(command) {
        console.log("Command sent:", command);
        // Send this command to your RC car via Bluetooth/Wi-Fi
    }
    function sendSpeed(speed) {
        document.getElementById('speedValue').innerText = speed;
        console.log("Speed set to:", speed);
        // Send speed data to the RC car
    }
</script>

</body>
</html>
