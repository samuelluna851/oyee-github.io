
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Te Amo Perla 💕</title>
<style>
  body {
    margin: 0;
    padding: 0;
    background: #111;
    overflow: hidden;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .word {
    position: absolute;
    font-size: 20px;
    color: #ff69b4;
    user-select: none;
    transition: transform 0.3s, font-size 0.3s;
    cursor: pointer;
  }

  .word:hover {
    font-size: 40px;
    transform: scale(1.5);
  }
</style>
</head>
<body>
<script>
  const words = ["te amo Perla"];
  const numWords = 30;

  for(let i=0; i<numWords; i++){
    const div = document.createElement('div');
    div.className = 'word';
    div.innerText = words[0];
    document.body.appendChild(div);

    // Posición inicial random
    div.style.left = Math.random() * window.innerWidth + 'px';
    div.style.top = -50 - Math.random() * 200 + 'px';

    // Animación de caída
    let speed = 1 + Math.random() * 3;
    function fall() {
      let top = parseFloat(div.style.top);
      if(top > window.innerHeight){
        div.style.top = -50 + 'px';
        div.style.left = Math.random() * window.innerWidth + 'px';
      } else {
        div.style.top = top + speed + 'px';
      }
      requestAnimationFrame(fall);
    }
    fall();
  }
</script>
</body>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Te Amo PERLIS 🫶🏻💕</title>
<style>
  body {
    margin: 0;
    padding: 0;
    height: 100vh;
    background: #ffe6f0;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Arial', sans-serif;
    color: #ff0066;
    font-size: 2rem;
  }

  .heart {
    position: absolute;
    animation: fall linear infinite, sway ease-in-out infinite;
    user-select: none;
    pointer-events: none;
  }

  @keyframes fall {
    0% { transform: translateY(-50px) rotate(0deg); opacity: 1; }
    100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
  }

  @keyframes sway {
    0% { transform: translateX(0px); }
    50% { transform: translateX(20px); }
    100% { transform: translateX(0px); }
  }

  .center-text {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    font-size: 3rem;
    text-align: center;
    color: #ff0066;
  }
</style>
</head>
<body>
<div class="center-text">TE AMO PERLIS 🫶🏻💕</div>

<script>
  const colors = ['#ff0066', '#ff66b2', '#ffccff', '#ff99cc', '#ff3399', '#ff6666'];

  function createHeart() {
    const heart = document.createElement('div');
    heart.className = 'heart';
    heart.textContent = '💖';
    heart.style.left = Math.random() * window.innerWidth + 'px';
    heart.style.fontSize = (20 + Math.random() * 40) + 'px';
    heart.style.color = colors[Math.floor(Math.random() * colors.length)];
    heart.style.animationDuration = ${3 + Math.random() * 4}s, ${2 + Math.random() * 2}s;
    heart.style.opacity = Math.random() * 0.8 + 0.2;
    document.body.appendChild(heart);

    setTimeout(() => {
      heart.remove();
    }, 7000);
  }

  setInterval(createHeart, 150);
</script>
</body>
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lluvia de Amor</title>
<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    body {
        background: linear-gradient(135deg, #ff9a9e, #fad0c4);
        overflow: hidden;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: 'Arial', sans-serif;
        color: white;
        text-shadow: 2px 2px 8px rgba(0,0,0,0.5);
    }
    h1 {
        position: absolute;
        top: 40%;
        font-size: 3rem;
        text-align: center;
    }
    .heart {
        position: absolute;
        top: -50px;
        font-size: 24px;
        color: #ff3366;
        animation: fall linear forwards;
    }
    @keyframes fall {
        to {
            transform: translateY(110vh) rotate(360deg);
            opacity: 0;
        }
    }
</style>
</head>
<body>
    <h1>💖 Lluvia de Amor 💖</h1>
    <script>
        const body = document.body;

        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '❤️';

            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = (Math.random() * 3 + 2) + 's'; // Velocidad
            heart.style.fontSize = (Math.random() * 20 + 20) + 'px'; // Tamaño

            body.appendChild(heart);

            setTimeout(() => {
                heart.remove();
            }, 5000);
        }

        setInterval(createHeart, 200);
    </script>
</body>
</html>
</html>
</html>
