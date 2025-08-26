<!DOCTYPE html>
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
</html>
