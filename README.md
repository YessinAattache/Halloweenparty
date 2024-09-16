<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Halloween Party</title>
    <style>
        body {
            background-color: #000; /* Black background for Halloween feel */
            color: #fff; /* White text */
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            overflow: hidden;
        }
        h1 {
            text-align: center;
            font-size: 4em;
            margin-top: 20px;
        }
        .floating-image {
            position: absolute;
            animation: float 10s infinite;
            width: 200px; /* Adjust the size of the image */
        }
        @keyframes float {
            0% { transform: translate(0, 0); }
            50% { transform: translate(100px, 50px); }
            100% { transform: translate(0, 0); }
        }
        #rsvp-button {
            display: block;
            margin: 50px auto;
            padding: 15px 30px;
            font-size: 1.5em;
            background-color: #ff4500; /* Halloween orange */
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
            text-align: center;
        }
        #rsvp-button:hover {
            background-color: #ff6347; /* Slightly lighter orange on hover */
        }
    </style>
</head>
<body>
    <h1>Halloween Party</h1>
    <img src="https://github.com/YessinAattache/Halloweenparty/blob/main/IMG_7400.JPG" alt="Floating Cat" class="floating-image">
    <a id="rsvp-button" href="https://docs.google.com/forms/d/e/1FAIpQLScFB9FSckUz2MF5YOpCQ2S9gHQMfTimJs7QKGtBaGeWCZArJQ/viewform?usp=sf_link" target="_blank">RSVP Here</a>

    <script>
        // JavaScript to make the image float around the screen
        const img = document.querySelector('.floating-image');
        function randomPosition() {
            const x = Math.floor(Math.random() * window.innerWidth) - img.width;
            const y = Math.floor(Math.random() * window.innerHeight) - img.height;
            img.style.transform = `translate(${x}px, ${y}px)`;
        }
        setInterval(randomPosition, 3000); // Move the image every 3 seconds
    </script>
</body>
</html>
