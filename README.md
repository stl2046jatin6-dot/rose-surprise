<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For My Billu ❤️</title>

<style>

body{
margin:0;
font-family:'Segoe UI',sans-serif;
background:black;
color:white;
overflow:hidden;
text-align:center;
}

canvas{
position:fixed;
top:0;
left:0;
z-index:-1;
}

.page{
display:none;
padding:40px;
max-width:700px;
margin:auto;
}

.active{
display:block;
animation:fade 1s;
}

@keyframes fade{
from{opacity:0;transform:translateY(20px);}
to{opacity:1;transform:translateY(0);}
}

button{
padding:14px 28px;
font-size:18px;
border:none;
border-radius:30px;
background:linear-gradient(45deg,#ff4d6d,#ff8fab);
color:white;
cursor:pointer;
box-shadow:0 0 20px rgba(255,0,90,0.6);
transition:0.3s;
margin-top:20px;
}

button:hover{
transform:scale(1.1);
box-shadow:0 0 30px rgba(255,0,120,1);
}

h1{
color:#ff9db5;
}

.heart{
position:fixed;
font-size:20px;
animation:fall 6s linear infinite;
}

@keyframes fall{
0%{transform:translateY(-10vh);}
100%{transform:translateY(110vh);}
}

</style>
</head>

<body>

<audio autoplay loop>
<source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_8c7d9c27c4.mp3">
</audio>

<canvas id="stars"></canvas>

<div id="p1" class="page active">
<h1 id="typing"></h1>
<button onclick="next('p2')">Enter My Heart 💌</button>
</div>

<div id="p2" class="page">
<h1>The Day Everything Changed</h1>
<p>
The day you came into my life woh mere liye sabse beautiful din tha.
Us din se meri life thodi si alag ho gayi.
You are my precious gem 💎
</p>
<button onclick="next('p3')">Continue</button>
</div>

<div id="p3" class="page">
<h1>How You Make Me Feel</h1>
<p>
Jab se main tumse baat karne laga hu na,
aisa lagta hai jaise kisi apne se baat kar raha hu.
Dil ko ek ajeeb si sukoon milti hai.
</p>
<button onclick="next('p4')">Continue</button>
</div>

<div id="p4" class="page">
<h1>Our Story</h1>
<p>
Kabhi kabhi hamari ladai bhi ho jati hai,
lekin phir bhi pata nahi kyun
hum phir se ek dusre ke paas aa jate hain.
Maybe some connections are written by Allah 🤲
</p>
<button onclick="next('p5')">Continue</button>
</div>

<div id="p5" class="page">
<h1>Billu My Princess 🎀</h1>
<p>
Agar tum saath ho na toh life thodi si easy lagti hai.
</p>
<button onclick="next('p6')">Continue</button>
</div>

<div id="p6" class="page">
<h1>Will You Be Mine? ❤️</h1>
<button onclick="next('p7')">YES ❤️</button>
<button onclick="next('p7')">ALWAYS ❤️</button>
</div>

<div id="p7" class="page">
<h1>I Knew You Would Say Yes 😌</h1>
<p>Love You So Much ❤️</p>
</div>

<script>

function next(id){
document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
document.getElementById(id).classList.add('active');
}

const text="For My Special One — My Billu ❤️";
let i=0;

function typing(){
if(i<text.length){
document.getElementById("typing").innerHTML+=text.charAt(i);
i++;
setTimeout(typing,70);
}
}
typing();

function hearts(){
let heart=document.createElement("div");
heart.className="heart";
heart.innerHTML="❤️";
heart.style.left=Math.random()*100+"vw";
heart.style.fontSize=Math.random()*20+20+"px";
document.body.appendChild(heart);
setTimeout(()=>heart.remove(),6000);
}
setInterval(hearts,400);

const canvas=document.getElementById("stars");
const ctx=canvas.getContext("2d");

canvas.width=window.innerWidth;
canvas.height=window.innerHeight;

let stars=[];

for(let i=0;i<200;i++){
stars.push({
x:Math.random()*canvas.width,
y:Math.random()*canvas.height,
size:Math.random()*2
});
}

function drawStars(){
ctx.clearRect(0,0,canvas.width,canvas.height);
ctx.fillStyle="white";

stars.forEach(s=>{
ctx.beginPath();
ctx.arc(s.x,s.y,s.size,0,Math.PI*2);
ctx.fill();
});
}

function animateStars(){
stars.forEach(s=>{
s.y+=0.3;
if(s.y>canvas.height)s.y=0;
});
drawStars();
requestAnimationFrame(animateStars);
}

animateStars();

</script>

</body>
</html>
