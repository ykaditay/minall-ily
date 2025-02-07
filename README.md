<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Minall 🌙✨</title>
    <style>
        body {
            text-align: center;
            background: url('https://i.postimg.cc/q78zK681/IMG-5402.jpg') no-repeat center center/cover;
            color: white;
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            transition: background 1s ease-in-out;
        }
        .container {
            background: rgba(0, 0, 0, 0.6);
            padding: 20px;
            border-radius: 15px;
            max-width: 600px;
        }
        h1 {
            font-size: 2.5em;
        }
        p {
            font-size: 1.2em;
            margin-top: 15px;
        }
        .ring {
            font-size: 4em;
            animation: ring-animation 2s infinite alternate;
        }
        @keyframes ring-animation {
            0% { transform: scale(1); }
            100% { transform: scale(1.2); }
        }
        .button {
            background: red;
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 10px;
            font-size: 1.2em;
            cursor: pointer;
            margin-top: 20px;
            transition: 0.3s;
        }
        .button:hover {
            background: pink;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Minall, My Shining Star 🌙✨</h1>
        <p>"Like the moon and stars light up the night sky, you brighten my world with your love and presence. On this special day, I just want to say... Will you always be my guiding light? 💖"</p>
        <div class="ring">💍</div>
        <button class="button" onclick="showLove()">Will You Be Mine? 💕</button>
        <p id="message" style="display:none; font-size: 1.5em; margin-top: 20px;">I Love You Forever, Minall! ❤️</p>
    </div>
    <audio id="background-music" loop>
        <source src="https://files.catbox.moe/78gyj8.mp3" type="audio/mpeg">
    </audio>
    <script>
        function showLove() {
            document.getElementById('message').style.display = 'block';
        }

        // Slideshow effect for background images
        let images = [
            'https://i.postimg.cc/q78zK681/IMG-5402.jpg',
            'https://i.postimg.cc/pL5926yb/IMG-5403.jpg',
            'https://i.postimg.cc/d0MhDjT7/IMG-5409.jpg',
            'https://i.postimg.cc/rFxm3tHM/IMG-0458.avif',
            'https://i.postimg.cc/gj69w8hJ/IMG-5401.jpg',
            'https://i.postimg.cc/667TVPL7/IMG-5960.jpg',
            'https://i.postimg.cc/Sj0BcRLG/IMG-5961.jpg',
            'https://i.postimg.cc/pVgrsBqs/IMG-6733.jpg',
            'https://i.postimg.cc/RZmFBZrf/IMG-6734.jpg',
            'https://i.postimg.cc/XJrN8ZFM/IMG-7650.jpg',
            'https://i.postimg.cc/gJ1zBYqx/IMG-9595.avif'
        ];
        
        let index = 0;
        function changeBackground() {
            document.body.style.backgroundImage = `url('${images[index]}')`;
            index = (index + 1) % images.length;
        }
        setInterval(changeBackground, 5000); // Change every 5 seconds

        // Ensure music plays on user interaction
        document.addEventListener('DOMContentLoaded', function () {
            let audio = document.getElementById('background-music');
            audio.play().catch(() => {
                document.body.addEventListener('click', function () {
                    audio.play();
                }, { once: true });
            });
        });
    </script>
</body>
</html>
