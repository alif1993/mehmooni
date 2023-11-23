<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Countdown Mehmooni</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            padding: 50px;
        }
        h1 {
            color: #333;
        }
        #countdown {
            font-size: 2em;
            color: #ff4500;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Exciting Mehmooni will be over in</h1>
    <div id="countdown"></div>

    <script>
        // Set the date we're counting down to (replace with your specific date and time)
        const countDownDate = new Date("Nov 22, 2023 23:00:00").getTime();

        // Update the countdown every 1 second
        const x = setInterval(function() {
            const now = new Date().getTime();
            const distance = countDownDate - now;

            // Calculate hours, minutes, and seconds
            const hours = Math.floor(distance / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            // Display the countdown
            document.getElementById("countdown").innerHTML = `${hours}h ${minutes}m ${seconds}s `;

            // If the countdown is over, display a message
            if (distance < 0) {
                clearInterval(x);
                document.getElementById("countdown").innerHTML = "EXPIRED";
            }
        }, 1000);
    </script>
</body>
</html>
