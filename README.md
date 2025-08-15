# Prank
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>💨 Пердеж-шоу</title>
<style>
  body {
    text-align: center;
    font-family: Arial, sans-serif;
    font-size: 2em;
    padding-top: 5%;
    transition: background 0.1s;
    overflow: hidden;
  }
  img {
    max-width: 80%;
    animation: shake 0.2s infinite;
  }
  @keyframes shake {
    0% { transform: translate(0px, 0px) rotate(0deg); }
    25% { transform: translate(5px, 5px) rotate(5deg); }
    50% { transform: translate(-5px, -5px) rotate(-5deg); }
    75% { transform: translate(5px, -5px) rotate(5deg); }
    100% { transform: translate(0px, 0px) rotate(0deg); }
  }
</style>
</head>
<body>
<h1 id="text">😏 Ну привет...</h1>
<img id="gif" src="https://media.tenor.com/B9NDOZuxzFMAAAAC/fart.gif" alt="puk">

<script>
  // Список звуков пердежа
  const farts = [
    "https://www.myinstants.com/media/sounds/fart-with-reverb.mp3",
    "https://www.myinstants.com/media/sounds/fart-meme.mp3",
    "https://www.myinstants.com/media/sounds/quick-fart.mp3",
    "https://www.myinstants.com/media/sounds/fart_2.mp3"
  ];

  function playRandomFart() {
    const audio = new Audio(farts[Math.floor(Math.random() * farts.length)]);
    audio.play();
  }

  // Запуск случайного пердежа каждые 1.5 секунды
  setInterval(playRandomFart, 1500);

  // Мигающий фон
  setInterval(() => {
    document.body.style.background = `rgb(${Math.random()*255},${Math.random()*255},${Math.random()*255})`;
  }, 100);

  // Меняющийся текст
  const texts = [
    "💨 ПЕРДЕЖ АТАКА!!!",
    "😂 Лови!",
    "💥 БА-БАХ!",
    "😈 Ты попался!",
    "🎉 Пук-фестиваль!",
    "🚀 Пердеж в космос!"
  ];
  let i = 0;
  setInterval(() => {
    document.getElementById("text").innerText = texts[i % texts.length];
    i++;
  }, 500);
</script>
</body>
</html>
