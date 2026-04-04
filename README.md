<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Yash ❤️ Gayatri</title>

<style>
body {
  margin: 0;
  overflow: hidden;
  font-family: 'Poppins', sans-serif;
  color: white;
  text-align: center;
}

/* Background Animation */
body {
  background: linear-gradient(-45deg, #ff4e50, #ff6a88, #fc913a, #f9d423);
  background-size: 400% 400%;
  animation: gradient 12s ease infinite;
}

@keyframes gradient {
  0% {background-position: 0% 50%;}
  50% {background-position: 100% 50%;}
  100% {background-position: 0% 50%;}
}

/* Slides */
.slide {
  display: none;
  height: 100vh;
  width: 100%;
  padding: 40px;
  box-sizing: border-box;
  animation: fade 1s;
}

@keyframes fade {
  from {opacity: 0;}
  to {opacity: 1;}
}

.text {
  font-size: 30px;
  line-height: 1.7;
}

.title {
  font-size: 45px;
  margin-bottom: 20px;
}

/* Images */
img {
  max-width: 300px;
  border-radius: 20px;
  margin-top: 20px;
  box-shadow: 0 0 20px black;
}

/* Falling Hearts */
.heart {
  position: fixed;
  top: -10px;
  color: pink;
  font-size: 20px;
  animation: fall linear infinite;
}

@keyframes fall {
  to {
    transform: translateY(100vh);
  }
}
</style>
</head>

<body>

<!-- MUSIC (Tere Bina) -->
<iframe width="0" height="0"
src="https://www.youtube.com/embed/9JDSGhhiOwI?autoplay=1&loop=1&playlist=9JDSGhhiOwI"
frameborder="0" allow="autoplay"></iframe>

<!-- SLIDES -->

<div class="slide"><div class="title">💌 My LOML 💋</div><div class="text">This is only for youu 🤌</div></div>

<div class="slide"><div class="text">This is our story… ❤️‍🩹</div></div>

<div class="slide"><div class="text">5 September… jab aapko main pasand aayi 🥹</div></div>

<div class="slide"><div class="text">15 October… baatein shuru hui 🫠</div></div>

<div class="slide"><div class="text">1 November… maine haan bola ❤️<br>I love you 💋</div></div>

<div class="slide"><div class="text">Tuition… chupke pyaar 🥺</div></div>

<div class="slide"><div class="text">First hug 🫂… first kiss 💋</div></div>

<div class="slide"><div class="text">Late night talks… boards support 🩷</div></div>

<div class="slide"><div class="text">Mandir… prayers… memories 🥰</div></div>

<div class="slide"><div class="text">1 year complete 😭🫶</div></div>

<div class="slide"><div class="text">Phir galtiyan hui… sab tootne laga 😔</div></div>

<div class="slide"><div class="text">Main aapko khona nahi chahti 😭</div></div>

<div class="slide"><div class="text">Please mujhe mat chhodo Yashu… 🥺💔</div></div>

<div class="slide"><div class="text">Sorry… Sorry… Sorry… 😭</div></div>

<!-- FIRST PIC -->
<div class="slide">
<div class="text">Mujhe maaf kar do… 🥺</div>
<img src="first.jpg">
</div>

<!-- COUPLE PIC -->
<div class="slide">
<div class="text">Yashu… I love you so much ❤️</div>
<img src="couple.jpg">
</div>

<!-- FINAL -->
<div class="slide">
<div class="title">PLEASE FORGIVE ME YASHU 🥺💔</div>
<img src="couple.jpg">
</div>

<!-- SCRIPT -->
<script>
let i = 0;
let slides = document.getElementsByClassName("slide");

function showSlides() {
  for (let j = 0; j < slides.length; j++) {
    slides[j].style.display = "none";
  }
  i++;
  if (i > slides.length) { i = 1; }
  slides[i-1].style.display = "block";
  setTimeout(showSlides, 3000);
}
showSlides();

/* Hearts generator */
setInterval(() => {
  let heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "💖";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.animationDuration = (2 + Math.random() * 3) + "s";
  document.body.appendChild(heart);

  setTimeout(() => {
    heart.remove();
  }, 5000);
}, 300);
</script>

</body>
</html>
