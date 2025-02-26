<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #222;
            color: white;
            font-family: Arial, sans-serif;
            flex-direction: column;
        }
        #clock {
            font-size: 50px;
            font-weight: bold;
            background: black;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px white;
        }
    </style>
</head>
<body>

    <h1>Digital Clock</h1>
    <div id="clock"></div>

    <script>
        function updateClock() {
            const now = new Date();
            let hours = now.getHours();
            let minutes = now.getMinutes();
            let seconds = now.getSeconds();

            // Add leading zeros
            hours = hours < 10 ? "0" + hours : hours;
            minutes = minutes < 10 ? "0" + minutes : minutes;
            seconds = seconds < 10 ? "0" + seconds : seconds;

            document.getElementById("clock").innerText = hours + ":" + minutes + ":" + seconds;
        }

        // Update clock every second
        setInterval(updateClock, 1000);
        updateClock(); // Initial call to show clock immediately
    </script>

</body>
</html>
