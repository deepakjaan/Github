<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Bacha</title>
    <style>
        body {
            background: linear-gradient(120deg, #ff9a9e, #fad0c4);
            text-align: center;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
            color: white;
        }
        .container {
            margin-top: 50px;
            display: none;
        }
        h1 {
            font-size: 60px;
            text-shadow: 2px 2px 20px rgba(255, 0, 102, 0.8);
            animation: glow 1.5s infinite alternate;
        }
        @keyframes glow {
            from {
                text-shadow: 2px 2px 10px rgba(255, 0, 102, 0.6);
            }
            to {
                text-shadow: 2px 2px 25px rgba(255, 0, 102, 1);
            }
        }
        .love-message {
            font-size: 30px;
            font-weight: bold;
            animation: fadeIn 3s ease-in-out;
        }
        .gift-box {
            width: 150px;
            height: 150px;
            background: red;
            position: relative;
            margin: 100px auto;
            cursor: pointer;
        }
        .gift-box:before {
            content: "";
            width: 100%;
            height: 50px;
            background: gold;
            position: absolute;
            top: -25px;
            left: 0;
        }
        .gift-box.open {
            display: none;
        }
        .image-container img {
            width: 350px;
            border-radius: 20px;
            box-shadow: 0 0 25px rgba(255, 0, 255, 0.8);
            animation: zoomIn 3s ease-in-out;
        }
        @keyframes zoomIn {
            0% { transform: scale(0.5); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
    </style>
</head>
<body>
    <div class="gift-box" onclick="openGift()"></div>
    <div class="container" id="birthdayContainer">
        <h1>🎉 Happy Birthday Bacha! 🎂</h1>
        <div class="image-container">
            <img src="YOUR_IMAGE_URL" alt="Birthday Image">
        </div>
        <p class="love-message">I Love You Bacha ❤️</p>
        <audio autoplay>
            <source src="YOUR_SONG_URL" type="audio/mpeg">
        </audio>
    </div>
    <script>
        function openGift() {
            document.querySelector(".gift-box").classList.add("open");
            document.getElementById("birthdayContainer").style.display = "block";
        }
    </script>
</body>
</html>
