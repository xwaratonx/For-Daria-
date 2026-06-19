# For-Daria-
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Для Дарьи ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Marck+Script&family=Montserrat:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Montserrat',sans-serif;
}

body{
background:#120708;
overflow-x:hidden;
color:white;
min-height:100vh;
}

.screen{
display:none;
min-height:100vh;
padding:25px;
justify-content:center;
align-items:center;
flex-direction:column;
text-align:center;
position:relative;
}

.active{
display:flex;
}

.bg{
position:absolute;
inset:0;
background:url('photo3.jpg') center center/cover;
filter:blur(12px);
opacity:.2;
z-index:-2;
}

.overlay{
position:absolute;
inset:0;
background:linear-gradient(
180deg,
rgba(0,0,0,.4),
rgba(70,0,0,.65)
);
z-index:-1;
}

.title{
font-family:'Marck Script',cursive;
font-size:58px;
color:#d62c45;
margin-bottom:15px;
text-shadow:0 0 20px rgba(255,0,80,.4);
}

.subtitle{
max-width:600px;
line-height:1.8;
font-size:20px;
margin-bottom:25px;
}

.main-photo{
width:320px;
max-width:90%;
border-radius:25px;
box-shadow:0 0 30px rgba(255,0,0,.25);
margin-bottom:25px;
}

.buttons{
display:flex;
gap:15px;
flex-wrap:wrap;
justify-content:center;
}

.btn{
border:none;
padding:15px 30px;
border-radius:15px;
font-size:18px;
cursor:pointer;
transition:.3s;
}

.yes{
background:#d62c45;
color:white;
}

.yes:hover{
transform:scale(1.05);
}

.no{
background:#2f1d1d;
color:white;
position:relative;
}

.card{
background:rgba(255,255,255,.08);
backdrop-filter:blur(10px);
padding:25px;
border-radius:20px;
max-width:500px;
width:100%;
}

input[type=date]{
width:100%;
padding:15px;
font-size:18px;
border-radius:12px;
border:none;
margin-top:15px;
margin-bottom:25px;
}

.time-option{
display:block;
margin:12px 0;
padding:15px;
border-radius:15px;
background:rgba(255,255,255,.08);
cursor:pointer;
}

.time-option input{
margin-right:10px;
}

.small{
display:block;
opacity:.7;
font-size:14px;
margin-top:5px;
}

.foods{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:12px;
margin-top:20px;
margin-bottom:25px;
}

.food{
background:rgba(255,255,255,.08);
padding:15px;
border-radius:15px;
}

.food input{
margin-right:8px;
}

.final-photo{
width:280px;
border-radius:25px;
margin-top:20px;
box-shadow:0 0 30px rgba(255,0,0,.2);
}

.happy{
font-size:64px;
font-weight:700;
color:#ff4d67;
margin-bottom:20px;
}

.result{
margin-top:20px;
line-height:2;
font-size:18px;
}

.heart{
position:fixed;
font-size:20px;
pointer-events:none;
animation:fall linear forwards;
}

@keyframes fall{
from{
transform:translateY(-50px);
opacity:1;
}
to{
transform:translateY(110vh);
opacity:0;
}
}

@keyframes pop{
0%{transform:scale(.5);}
100%{transform:scale(1);}
}

.celebrate{
font-size:70px;
animation:pop .5s ease;
}

</style>
</head>

<body>

<div class="bg"></div>
<div class="overlay"></div>

<!-- Экран 1 -->

<section id="screen1" class="screen active">

<h1 class="title">Моя любимая Дарья ❤️</h1>

<img src="photo1.jpg" class="main-photo">

<p class="subtitle">
Несмотря на то, что мы уже вместе,
<br><br>
я всё равно хочу пригласить тебя на свидание.
<br><br>
Пойдёшь со мной?
</p>

<div class="buttons">
<button class="btn yes" onclick="startDate()">
Конечно да ❤️
</button>

<button id="noBtn" class="btn no">
Нет
</button>
</div>

</section>

<!-- Экран 2 -->

<section id="screen2" class="screen">

<div class="card">

<h2 class="title" style="font-size:45px;">
Когда идём на свидание?
</h2>

<input type="date" id="date">

<h3 style="margin-bottom:15px;">Во сколько?</h3>

<label class="time-option">
<input type="radio" name="time" value="19:00">
19:00
<span class="small">Не рановато? 😏</span>
</label>

<label class="time-option">
<input type="radio" name="time" value="21:00">
21:00
<span class="small">Отличное время ❤️</span>
</label>

<label class="time-option">
<input type="radio" name="time" value="23:00">
23:00
<span class="small">Решила тусить? 😂</span>
</label>

<br>

<button class="btn yes" onclick="nextFoods()">
Дальше →
</button>

</div>

</section>

<!-- Экран 3 -->

<section id="screen3" class="screen">

<div class="card">

<h2 class="title" style="font-size:45px;">
Что будем есть? ❤️
</h2>

<div class="foods">

<label class="food"><input type="checkbox" value="Пицца 🍕">Пицца 🍕</label>

<label class="food"><input type="checkbox" value="Роллы 🍣">Роллы 🍣</label>

<label class="food"><input type="checkbox" value="Хинкали 🥟">Хинкали 🥟</label>

<label class="food"><input type="checkbox" value="Рыба 🐟">Рыба 🐟</label>

<label class="food"><input type="checkbox" value="Вино 🍷">Вино 🍷</label>

<label class="food"><input type="checkbox" value="Сок 🧃">Сок 🧃</label>

</div>

<button class="btn yes" onclick="finishDate()">
Завершить ❤️
</button>

</div>

</section>

<!-- Экран 4 -->

<section id="screen4" class="screen">

<div class="happy">
Я СЧАСТЛИВ ❤️
</div>

<p class="subtitle">
Я действительно счастлив, что ты не сказала нет.
<br><br>
Я очень рад, что мы проведём этот вечер вместе.
<br><br>
Жди меня, я уже начинаю готовиться и ждать нашего свидания.
</p>

<div class="result" id="result"></div>

<img src="photo2.jpg" class="final-photo">

</section>

<script>

const noBtn = document.getElementById("noBtn");

const texts = [
"Нет",
"Точно нет?",
"Подумай ещё 😏",
"Я же стараюсь ❤️",
"Ну Дарьяяя 🥺",
"Не туда жмёшь 😂",
"Последний шанс 😁",
"Всё равно не дам нажать 😎"
];

let index = 0;

function moveButton(){

index++;

if(index >= texts.length){
index = 0;
}

noBtn.innerText = texts[index];

const x = Math.random() * (window.innerWidth - 150);
const y = Math.random() * (window.innerHeight - 100);

noBtn.style.position = "fixed";
noBtn.style.left = x + "px";
noBtn.style.top = y + "px";
}

noBtn.addEventListener("mouseenter", moveButton);
noBtn.addEventListener("click", moveButton);
noBtn.addEventListener("touchstart", moveButton);

function createHeart(){

const heart = document.createElement("div");

heart.className = "heart";
heart.innerHTML = "❤️";

heart.style.left = Math.random()*100+"vw";

heart.style.animationDuration =
(4 + Math.random()*5) + "s";

document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},9000);

}

setInterval(createHeart,300);

function switchScreen(id){

document.querySelectorAll(".screen")
.forEach(s=>s.classList.remove("active"));

document.getElementById(id)
.classList.add("active");

}

function startDate(){

document.getElementById("screen1").innerHTML =
'<div class="celebrate">Урааааа! ❤️</div>';

for(let i=0;i<40;i++){
setTimeout(createHeart,i*50);
}

setTimeout(()=>{
switchScreen("screen2");
},1500);

}

function nextFoods(){

const date =
document.getElementById("date").value;

const time =
document.querySelector('input[name="time"]:checked');

if(!date || !time){
alert("Выбери дату и время ❤️");
return;
}

switchScreen("screen3");
}

function finishDate(){

const date =
document.getElementById("date").value;

const time =
document.querySelector('input[name="time"]:checked').value;

const foods =
Array.from(
document.querySelectorAll(
'.food input:checked'
)
).map(x=>x.value);

document.getElementById("result").innerHTML =
`
📅 <b>Дата:</b> ${date}<br>
🕘 <b>Время:</b> ${time}<br>
🍽️ <b>Выбрано:</b><br>
${foods.join("<br>")}
`;

switchScreen("screen4");

}

</script>

</body>
</html>
