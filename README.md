<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Papa! 🎂</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        .container {
            text-align: center;
            z-index: 10;
            position: relative;
        }

        .birthday-text {
            font-size: 4rem;
            font-weight: bold;
            color: #fff;
            text-shadow: 3px 3px 6px rgba(0,0,0,0.5);
            margin-bottom: 2rem;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from {
                text-shadow: 3px 3px 6px rgba(0,0,0,0.5), 0 0 20px #ff6b6b;
            }
            to {
                text-shadow: 3px 3px 6px rgba(0,0,0,0.5), 0 0 30px #ff6b6b, 0 0 40px #ff6b6b;
            }
        }

        .cake {
            position: relative;
            width: 200px;
            height: 200px;
            margin: 0 auto 2rem;
            animation: bounce 2s ease-in-out infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-20px);
            }
            60% {
                transform: translateY(-10px);
            }
        }

        .cake-base {
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 160px;
            height: 80px;
            background: linear-gradient(45deg, #8B4513, #A0522D);
            border-radius: 10px 10px 0 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }

        .cake-layer {
            position: absolute;
            bottom: 80px;
            left: 50%;
            transform: translateX(-50%);
            width: 140px;
            height: 60px;
            background: linear-gradient(45deg, #FFB6C1, #FFC0CB);
            border-radius: 10px 10px 0 0;
            box-shadow: 0 3px 10px rgba(0,0,0,0.2);
        }

        .cake-top {
            position: absolute;
            bottom: 140px;
            left: 50%;
            transform: translateX(-50%);
            width: 120px;
            height: 40px;
            background: linear-gradient(45deg, #FF69B4, #FF1493);
            border-radius: 10px 10px 0 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.2);
        }

        .candle {
            position: absolute;
            bottom: 180px;
            left: 50%;
            transform: translateX(-50%);
            width: 8px;
            height: 30px;
            background: linear-gradient(to bottom, #FFD700, #FFA500);
            border-radius: 4px;
        }

        .flame {
            position: absolute;
            bottom: 210px;
            left: 50%;
            transform: translateX(-50%);
            width: 12px;
            height: 20px;
            background: radial-gradient(circle, #FFD700, #FF6B35, #FF4500);
            border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
            animation: flicker 0.5s ease-in-out infinite alternate;
        }

        @keyframes flicker {
            0% {
                transform: translateX(-50%) scale(1);
                opacity: 1;
            }
            100% {
                transform: translateX(-50%) scale(1.1);
                opacity: 0.8;
            }
        }

        .sprinkles {
            position: absolute;
            width: 4px;
            height: 4px;
            background: #FFD700;
            border-radius: 50%;
            animation: sprinkle 3s linear infinite;
        }

        .sprinkle1 { top: 20px; left: 30px; animation-delay: 0s; }
        .sprinkle2 { top: 40px; right: 25px; animation-delay: 0.5s; }
        .sprinkle3 { top: 60px; left: 20px; animation-delay: 1s; }
        .sprinkle4 { top: 80px; right: 40px; animation-delay: 1.5s; }
        .sprinkle5 { top: 100px; left: 50px; animation-delay: 2s; }

        @keyframes sprinkle {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(360deg);
                opacity: 0;
            }
        }

        .message {
            font-size: 1.5rem;
            color: #fff;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            margin-top: 2rem;
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .floating-hearts {
            position: absolute;
            font-size: 2rem;
            color: #ff6b6b;
            animation: float 6s ease-in-out infinite;
        }

        .heart1 { top: 10%; left: 10%; animation-delay: 0s; }
        .heart2 { top: 20%; right: 15%; animation-delay: 1s; }
        .heart3 { top: 60%; left: 5%; animation-delay: 2s; }
        .heart4 { top: 80%; right: 10%; animation-delay: 3s; }
        .heart5 { top: 40%; left: 80%; animation-delay: 4s; }

        @keyframes float {
            0%, 100% {
                transform: translateY(0px) rotate(0deg);
            }
            50% {
                transform: translateY(-20px) rotate(180deg);
            }
        }

        .sparkles {
            position: absolute;
            width: 3px;
            height: 3px;
            background: #FFD700;
            border-radius: 50%;
            animation: sparkle 2s linear infinite;
        }

        .sparkle1 { top: 15%; left: 20%; animation-delay: 0s; }
        .sparkle2 { top: 25%; right: 25%; animation-delay: 0.3s; }
        .sparkle3 { top: 45%; left: 15%; animation-delay: 0.6s; }
        .sparkle4 { top: 65%; right: 20%; animation-delay: 0.9s; }
        .sparkle5 { top: 85%; left: 25%; animation-delay: 1.2s; }

        @keyframes sparkle {
            0%, 100% {
                opacity: 0;
                transform: scale(0);
            }
            50% {
                opacity: 1;
                transform: scale(1);
            }
        }

        .love-text {
            font-size: 1.2rem;
            color: #FFD700;
            margin-top: 1rem;
            font-style: italic;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% {
                opacity: 0.7;
            }
            50% {
                opacity: 1;
            }
        }

        @media (max-width: 768px) {
            .birthday-text {
                font-size: 2.5rem;
            }
            .cake {
                width: 150px;
                height: 150px;
            }
            .message {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
    <div class="floating-hearts heart1">❤️</div>
    <div class="floating-hearts heart2">💖</div>
    <div class="floating-hearts heart3">💝</div>
    <div class="floating-hearts heart4">💕</div>
    <div class="floating-hearts heart5">💗</div>

    <div class="sparkles sparkle1"></div>
    <div class="sparkles sparkle2"></div>
    <div class="sparkles sparkle3"></div>
    <div class="sparkles sparkle4"></div>
    <div class="sparkles sparkle5"></div>

    <div class="container">
        <h1 class="birthday-text">Happy Birthday Papa! 🎂</h1>
        
        <div class="cake">
            <div class="cake-base"></div>
            <div class="cake-layer"></div>
            <div class="cake-top"></div>
            <div class="candle"></div>
            <div class="flame"></div>
            <div class="sprinkles sprinkle1"></div>
            <div class="sprinkles sprinkle2"></div>
            <div class="sprinkles sprinkle3"></div>
            <div class="sprinkles sprinkle4"></div>
            <div class="sprinkles sprinkle5"></div>
        </div>

        <div class="message">
            Wishing you a day filled with joy, laughter, and love! 🎉
        </div>
        
        <div class="love-text">
            With all my love and gratitude ❤️
        </div>
    </div>

    <script>
        // Add some interactive sparkles on click
        document.addEventListener('click', function(e) {
            const sparkle = document.createElement('div');
            sparkle.className = 'sparkles';
            sparkle.style.left = e.clientX + 'px';
            sparkle.style.top = e.clientY + 'px';
            sparkle.style.position = 'fixed';
            sparkle.style.animation = 'sparkle 1s linear forwards';
            document.body.appendChild(sparkle);
            
            setTimeout(() => {
                document.body.removeChild(sparkle);
            }, 1000);
        });

        // Add some floating balloons
        function createBalloon() {
            const balloon = document.createElement('div');
            balloon.innerHTML = '🎈';
            balloon.style.position = 'fixed';
            balloon.style.fontSize = '2rem';
            balloon.style.left = Math.random() * window.innerWidth + 'px';
            balloon.style.top = window.innerHeight + 'px';
            balloon.style.animation = 'float 8s linear forwards';
            balloon.style.zIndex = '5';
            document.body.appendChild(balloon);
            
            setTimeout(() => {
                if (document.body.contains(balloon)) {
                    document.body.removeChild(balloon);
                }
            }, 8000);
        }

        // Create balloons periodically
        setInterval(createBalloon, 3000);
    </script>
</body>
</html>
