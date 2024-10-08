<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Vighnesh Games</title>

    <!-- Favicon for the logo -->
    <link rel="icon" href="C:/Users/Sachin/Downloads/imageedit_1_9183713021.png">

    <style>
        /* Ensures the body and iframe take up full screen size */
        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            display: flex;
            overflow: hidden;
            background-color: #00ff00; /* Brighter light green */
        }

        /* Container for iframe and buttons */
        .container {
            display: flex;
            flex-grow: 1;
            width: 100%;
        }

        /* Styling for the iframe to occupy 3/4th of the page */
        .game-container {
            width: 75%;
            height: 68.5vh;
            padding: 2%;
            position: relative;
        }

        iframe {
            width: 100%;
            height: 100%;
            border: none;
        }

        /* Full screen button positioned at the bottom */
        .fullscreen-button {
            position: absolute;
            bottom: -30px; /* Reduced gap */
            left: 50%;
            transform: translateX(-50%);
            width: 70%; /* Button width set to 70% */
            padding: 10px 20px;
            font-size: 16px;
            background-color: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }

        .fullscreen-button:hover {
            background-color: #0056b3;
        }

        /* Right-side panel for buttons */
        .buttons-container {
            width: 25%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 1%;
            background-color: #008000;
        }

        /* Container for each button and image */
        .button-wrapper {
            text-align: center;
            margin: 10px 0;
        }

        /* Image size set to 80px */
        .button-wrapper img {
            width: 80px;
            height: 80px;
            border-radius: 15px;
            pointer-events: none;
            display: block;  /* Ensures block-level display */
            margin: 0 auto 10px;  /* Centers the image and adds some space below */
        }

        /* Button styling */
        .button-wrapper button {
            width: 100px; /* Adjusted button size to match image */
            padding: 10px;
            margin-top: 5px;
            font-size: 16px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }

        .button-wrapper button:hover {
            background-color: #45a049;
        }

        /* Created by text */
        .created-by {
            position: absolute;
            bottom: -10px; /* Reduced gap */
            left: 50%;
            transform: translateX(-50%);
            font-size: 18px; /* Text size increased */
            color: #333;
        }

        /* Footer for logo and copyright */
        .footer {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            background-color: black; /* Footer background set to black */
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 10px 0;
        }

        .footer img {
            width: 50px;
            height: 50px;
            margin-right: 10px;
        }

        .footer-text {
            font-size: 16px;
            color: white; /* Text color set to white */
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Game iframe occupying 3/4th of the page -->
        <div class="game-container">
            <iframe id="gameIframe" src="https://game-previews.gdevelop.io/1728191774306-309285/index.html" allowfullscreen></iframe>
            <button class="fullscreen-button" onclick="enterFullscreen()">Enter Full Screen</button>
        </div>

        <!-- Button container occupying 1/4th of the page -->
        <div class="buttons-container">

            <!-- Button with image 1 -->
            <div class="button-wrapper">
                <img src="file:///C:/Users/Sachin/Downloads/SCDF.JPG" alt="Game 1">
                <button onclick="loadGame('https://game-previews.gdevelop.io/1728191774306-309285/index.html')">PLAY GAME 1</button>
            </div>

            <!-- Button with image 2 -->
            <div class="button-wrapper">
                <img src="file:///C:/Users/Sachin/Downloads/CaptureW.JPG" alt="Game 2">
                <button onclick="loadGame('https://game-previews.gdevelop.io/1728208191705-594208/index.html')">PLAY GAME 2</button>
            </div>

            <!-- Button with image 3 -->
            <div class="button-wrapper">
                <img src="file:///C:/Users/Sachin/Downloads/CaptureW.JPG" alt="Game 3">
                <button onclick="loadGame('https://game-previews.gdevelop.io/1728226434384-588034/index.html')">PLAY GAME 3</button>
            </div>

        </div>
    </div>

    <!-- Footer for logo and copyright -->
    <div class="footer">
        <img src="file:///C:/Users/Sachin/Downloads/imageedit_1_9183713021.png" alt="Vighnesh Games Logo">
        <span class="footer-text">� 2024 Vighnesh Games</span>
    </div>

    <script>
        // Function to load a new game in the iframe
        function loadGame(gameUrl) {
            document.getElementById('gameIframe').src = gameUrl;
        }

        // Function to enter fullscreen
        function enterFullscreen() {
            var iframe = document.getElementById('gameIframe');
            if (iframe.requestFullscreen) {
                iframe.requestFullscreen();
            } else if (iframe.mozRequestFullScreen) { // Firefox
                iframe.mozRequestFullScreen();
            } else if (iframe.webkitRequestFullscreen) { // Chrome, Safari and Opera
                iframe.webkitRequestFullscreen();
            } else if (iframe.msRequestFullscreen) { // IE/Edge
                iframe.msRequestFullscreen();
            }
        }
    </script>

</body>
</html>
