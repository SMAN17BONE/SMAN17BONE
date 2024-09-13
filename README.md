<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>link fisika</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 10px;
            height:99999em;
            background-color: white;
        }
        canvas {
            border: 1px solid crimson;
            width: 100%;
            height: auto;
        }
        button {
          font-size: 20px;
          color: crimson;
          padding: 10px;
          margin:20px;
          text-decoration: none;
        }
        header h1 {
          color: crimson;
        }
        footer>h1 {
          color:crimson;
        }
    </style>
</head>
<body>
    <h1>ai_fisika.com</h1>
    <button id="startTest">
      <strong>
        tombol gacor
      </strong>
      </button>
    <canvas id="testCanvas"></canvas>

    <script>
        document.getElementById('startTest').addEventListener('click', function() {
            var canvas = document.getElementById('testCanvas');
            var ctx = canvas.getContext('2d');

            // Set canvas size to full viewport
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;

            function draw() {
                var width = canvas.width;
                var height = canvas.height;
                
                ctx.clearRect(0, 0, width, height);

                // Draw multiple overlapping rectangles
                ctx.fillStyle = 'rgba(0, 0, 255, 0.3)';
                for (var i = 1; i < 900000; i++) {
                    var x = Math.random() * width;
                    var y = Math.random() * height;
                    var size = Math.random() * 5000 + 100; // size between 10 and 60
                    ctx.fillRect(x, y, size, size);
                }

                // Request a new animation frame
                requestAnimationFrame(draw);
            }

            draw();
        });
    </script>
        <header>
        <h1> </h1>
    </header>
    <footer>
      <h1>
        tekan untuk memunculkan jawaban.
      </h1>
    </footer>
</body>
</html>
