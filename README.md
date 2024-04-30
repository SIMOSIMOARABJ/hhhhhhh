<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>عيد ميلاد سعيد لأجمل أميرة</title>
    <style>
        body {
            background-color: #f5f5f5;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        #fireworksCanvas {
            position: absolute;
            top: 0;
            left: 0;
        }
        .container {
            text-align: center;
        }
        .message {
            font-size: 24px;
            margin-bottom: 20px;
        }
        .image-container {
            position: relative;
            display: inline-block;
        }
        .image-container img {
            width: 300px;
            height: auto;
            border-radius: 50%;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
        }
        .image-caption {
            position: absolute;
            bottom: -20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #fff;
            padding: 5px 10px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
        }
    </style>
</head>
<body>
    <canvas id="fireworksCanvas"></canvas>
    <div class="container">
        <h1 class="message">عيد ميلاد سعيد لأجمل أميرة</h1>
        <div class="image-container">
            <img src="heart.jpg" alt="حبيبتي">
            <div class="image-caption">أجمل أميرة</div>
        </div>
    </div>
    
    <script>
        const fireworksCanvas = document.getElementById('fireworksCanvas');
        const ctx = fireworksCanvas.getContext('2d');

        fireworksCanvas.width = window.innerWidth;
        fireworksCanvas.height = window.innerHeight;

        let animationId;

        function drawFirework(x, y, color, radius) {
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2);
            ctx.fillStyle = color;
            ctx.fill();
            ctx.closePath();
        }

        function animate() {
            animationId = requestAnimationFrame(animate);
            ctx.fillStyle = 'rgba(0, 0, 0, 0.1)';
            ctx.fillRect(0, 0, fireworksCanvas.width, fireworksCanvas.height);

            // تعريف الألعاب النارية هنا، على سبيل المثال:
            // drawFirework(x, y, color, radius);

            // مثال بسيط
            const fireworksX = Math.random() * fireworksCanvas.width;
            const fireworksY = Math.random() * fireworksCanvas.height;
            const fireworksColor = `hsl(${Math.random() * 360}, 100%, 50%)`;
            const fireworksRadius = Math.random() * 3;
            drawFirework(fireworksX, fireworksY, fireworksColor, fireworksRadius);
        }

        animate(); // يبدأ الألعاب النارية تلقائيًا عند تحميل الصفحة
    </script>
</body>
</html>
