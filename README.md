
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Special Mission 🎓</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;800&family=Poppins:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box}

:root{
  --bg:#101024;
  --purple:#a56be8;
  --gold:#ffca67;
  --white:#fffaf4;
  --dark:#211b36;
}

body{
  min-height:100vh;
  background:
  radial-gradient(circle at 15% 15%,#49316c,transparent 35%),
  radial-gradient(circle at 85% 85%,#4b285f,transparent 35%),
  var(--bg);
  color:white;
  font-family:Poppins,sans-serif;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:20px;
  overflow-x:hidden;
}

body:before{
  content:"";
  position:fixed;
  inset:0;
  background-image:radial-gradient(#ffffff25 1px,transparent 1px);
  background-size:35px 35px;
  pointer-events:none;
}

.app{
  width:100%;
  max-width:480px;
  position:relative;
  z-index:2;
}

.header{
  display:flex;
  align-items:center;
  justify-content:space-between;
  margin-bottom:18px;
}

.brand{
  font-weight:800;
  font-size:13px;
  letter-spacing:1px;
  color:var(--gold);
}

.steps{display:flex;gap:8px}

.step{
  width:32px;
  height:32px;
  border:1px solid #ffffff55;
  border-radius:50%;
  display:grid;
  place-items:center;
  font-size:12px;
}

.step.active{
  background:var(--gold);
  color:#20182e;
  border-color:var(--gold);
  font-weight:800;
}

.track{
  height:5px;
  background:#ffffff25;
  border-radius:20px;
  margin-bottom:17px;
  overflow:hidden;
}

.fill{
  height:100%;
  width:0%;
  background:linear-gradient(90deg,var(--purple),var(--gold));
  transition:.5s;
}

.card{
  background:linear-gradient(145deg,#fffdf8,#f7e9dc);
  color:var(--dark);
  padding:35px 25px;
  border-radius:27px;
  min-height:540px;
  position:relative;
  overflow:hidden;
  box-shadow:0 30px 80px #0008;
  animation:enter .55s ease;
}

.card:before{
  content:"";
  position:absolute;
  width:220px;
  height:220px;
  border-radius:50%;
  background:#f8dba955;
  top:-140px;
  right:-80px;
}

.card:after{
  content:"";
  position:absolute;
  width:180px;
  height:180px;
  border-radius:50%;
  background:#d6b4ee33;
  bottom:-130px;
  left:-70px;
}

.content{
  position:relative;
  z-index:1;
  text-align:center;
}

@keyframes enter{
  from{opacity:0;transform:translateY(25px) scale(.97)}
  to{opacity:1;transform:translateY(0) scale(1)}
}

.tag{
  display:inline-block;
  padding:8px 15px;
  background:#eee1f8;
  color:#8c4eb4;
  border-radius:30px;
  font-size:11px;
  font-weight:800;
  letter-spacing:2px;
  margin-bottom:22px;
}

.art{
  font-size:75px;
  margin:5px 0 20px;
  filter:drop-shadow(0 8px 8px #0002);
}

h1{
  font-family:'Playfair Display',serif;
  font-size:35px;
  line-height:1.2;
  margin-bottom:15px;
}

.purple{color:#9854c5}

.description{
  color:#777080;
  font-size:14px;
  line-height:1.9;
  margin-bottom:25px;
}

.highlight{
  background:linear-gradient(transparent 60%,#ffdb8b 60%);
  font-weight:800;
}

.main-btn{
  width:100%;
  padding:17px;
  border:0;
  border-radius:14px;
  background:linear-gradient(120deg,#ffca67,#f5a72d);
  color:#2c2140;
  font-size:15px;
  font-weight:800;
  font-family:inherit;
  cursor:pointer;
  box-shadow:0 6px 0 #c9852d;
  transition:.2s;
}

.main-btn:hover{transform:translateY(-3px)}

.main-btn:active{transform:translateY(3px)}

.small{
  font-size:11px;
  color:#a49ba8;
  margin-top:20px;
}

.question{
  font-family:'Playfair Display',serif;
  font-size:24px;
  line-height:1.5;
  margin:15px 0 25px;
}

.tape{
  background:#f4cf83;
  padding:12px 18px;
  display:inline-block;
  transform:rotate(-2deg);
  box-shadow:0 5px 12px #0002;
  font-weight:800;
  margin-bottom:25px;
}

.options{
  display:grid;
  gap:12px;
}

.option{
  width:100%;
  padding:15px;
  background:#fffdfa;
  border:1.5px solid #e5d4cf;
  border-radius:16px;
  display:flex;
  align-items:center;
  gap:13px;
  text-align:left;
  font-family:inherit;
  font-size:13px;
  font-weight:700;
  color:#342a43;
  cursor:pointer;
  transition:.2s;
}

.option:hover{
  background:#f4e8fb;
  border-color:#a56be8;
  transform:translateX(5px);
}

.option .ico{font-size:24px}

.feedback{
  display:none;
  margin-top:17px;
  padding:12px;
  border-radius:12px;
  background:#eee2f7;
  color:#74439a;
  font-size:13px;
  font-weight:700;
}

.footer{
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-top:25px;
  font-size:12px;
  font-weight:700;
  color:#51435e;
}

.final{
  font-family:'Playfair Display',serif;
  font-size:clamp(40px,10vw,57px);
  color:#974bc1;
  text-shadow:2px 3px #f0d1ff;
  margin:15px 0;
}

.final-box{
  background:#f0dcff;
  color:#74409b;
  padding:14px;
  border-radius:13px;
  font-weight:800;
  margin:20px 0;
  transform:rotate(-2deg);
}

.confetti{
  position:fixed;
  top:-30px;
  z-index:10;
  pointer-events:none;
  animation:fall linear forwards;
}

@keyframes fall{
  to{transform:translateY(110vh) rotate(800deg);opacity:0}
}

@media(max-width:400px){
  .card{padding:30px 20px;min-height:510px}
  h1{font-size:30px}
  .question{font-size:21px}
}
</style>
</head>

<body>

<div class="app">

<header class="header">
  <div class="brand">✦ A SPECIAL SURPRISE</div>
  <div class="steps">
    <div class="step active" id="s1">1</div>
    <div class="step" id="s2">2</div>
    <div class="step" id="s3">3</div>
  </div>
</header>

<div class="track">
  <div class="fill" id="fill"></div>
</div>

<div class="card" id="card">

<div class="content">

  <div class="tag">🔎 CONFIDENTIAL INFORMATION</div>

  <div class="art">🕵️‍♀️🎓</div>

  <h1>We Have <span class="purple">Some News!</span></h1>

  <p class="description">
    Our investigation team discovered something interesting...
    <br><br>
    Apparently, someone has officially earned a diploma!
    <br><br>
    But we need to confirm one thing...
  </p>

  <div class="question">
    What kind of diploma did you get? 👀
  </div>

  <button class="main-btn" onclick="reveal()">
    REVEAL THE SECRET ✨
  </button>

  <div class="small">
    TOP SECRET • AUTHORIZED PERSONNEL ONLY
  </div>

</div>
</div>
</div>

<script>

const questions=[
{
 q:"An employee arrives 5 minutes late. What's your first reaction?",
 a:[
  ["😡","Where have you been?!"],
  ["☕","Let's discuss your attendance"],
  ["💸","I'll deduct it from your salary"]
 ],
 response:[
  "Someone woke up on the wrong side of HR 😂",
  "Coffee first, investigation second ☕",
  "The payroll department is already waiting 💸"
 ]
},
{
 q:"An employee asks for a salary increase. What do you say?",
 a:[
  ["📩","We'll get back to you"],
  ["😂","Have you tried being rich?"],
  ["📋","Please submit an official request"]
 ],
 response:[
  "The most famous HR sentence ever 😂",
  "Financial advice by HR professionals 💀",
  "Paperwork never ends!"
 ]
},
{
 q:"What's the most important HR superpower?",
 a:[
  ["🧠","Reading people's minds"],
  ["☕","Surviving endless meetings"],
  ["🗣️","Saying 'As per our discussion'"]
 ],
 response:[
  "Especially during interviews! 🧠",
  "Coffee deserves an employee of the month award",
  "A true HR classic 😂"
 ]
},
{
 q:"What's your first decision as an HR specialist?",
 a:[
  ["🏖️","Give everyone a vacation"],
  ["💰","Increase everyone's salary"],
  ["👑","Promote myself immediately"]
 ],
 response:[
  "Employee happiness comes first! ❤️",
  "The finance department disagrees 😂",
  "CEO of HR in 3 seconds!"
 ]
}
];

let current=0;

function updateSteps(n){
 for(let i=1;i<=3;i++){
  document.getElementById('s'+i).classList.toggle('active',i<=n);
 }
}

function updateProgress(v){
 document.getElementById('fill').style.width=v+'%';
}

function render(html){
 const card=document.getElementById('card');
 card.style.animation='none';
 void card.offsetWidth;
 card.style.animation='enter .55s ease';
 card.innerHTML=`<div class="content">${html}</div>`;
}

function reveal(){
 updateSteps(2);
 updateProgress(15);

 render(`
  <div class="tag">🎯 MYSTERY SOLVED!</div>
  <div class="art">💼👩‍💼</div>
  <h1>It's <span class="purple">HR!</span></h1>
  <p class="description">
    HUMAN RESOURCES DIPLOMA
    <br><br>
    So you're officially qualified to manage people,
    solve problems, and survive endless meetings!
    😂
  </p>
  <div class="final-box">HR SPECIALIST IN THE MAKING ✨</div>
  <button class="main-btn" onclick="startQuiz()">
    LET THE HR TEST BEGIN →
  </button>
 `);
}

function startQuiz(){
 current=0;
 showQuestion();
}

function showQuestion(){
 const q=questions[current];
 updateSteps(2);
 updateProgress(15+(current/questions.length)*65);

 render(`
  <div class="tape">🔎 HR INVESTIGATION</div>
  <div class="art">${['⏰','💰','🧠','👑'][current]}</div>
  <div class="tag">QUESTION ${current+1} / ${questions.length}</div>
  <div class="question">${q.q}</div>

  <div class="options">
   ${q.a.map((a,i)=>`
    <button class="option" onclick="choose(${i})">
     <span class="ico">${a[0]}</span>
     <span>${a[1]}</span>
    </button>
   `).join('')}
  </div>

  <div class="feedback" id="feedback"></div>

  <div class="footer">
   <span>💼 HR DEPARTMENT</span>
   <span>${current+1} OF ${questions.length} ↗</span>
  </div>
 `);
}

function choose(i){
 const q=questions[current];
 const feedback=document.getElementById('feedback');
 feedback.style.display='block';
 feedback.innerHTML=q.response[i]+'<br><br>Next question coming up...';

 document.querySelectorAll('.option').forEach(b=>b.disabled=true);

 setTimeout(()=>{
  current++;
  if(current<questions.length){
   showQuestion();
  }else{
   celebrate();
  }
 },1100);
}

function celebrate(){
 updateSteps(3);
 updateProgress(100);

 render(`
  <div class="tag">🏆 MISSION COMPLETED</div>
  <div class="art">👑🎓💐</div>

  <div class="final">MABROOOOOOK!</div>

  <h1>You Did It! ❤️</h1>

  <p class="description">
   Congratulations on your
   <span class="purple"><b>HR Diploma!</b></span>
   <br><br>
   From now on, you don't just judge people...
   <br>
   You officially have a diploma to do it! 😂
  </p>

  <div class="final-box">
   HR SPECIALIST LOADING... 100% ✅
  </div>

  <p class="description">
   Wishing you more success, happiness
   and amazing opportunities.
   <br><br>
   YOU DESERVE IT! 💜
  </p>

  <button class="main-btn" onclick="party()">
   CELEBRATE AGAIN 🎉
  </button>
 `);

 party();
}

function party(){
 const emojis=['🎉','🎊','✨','💜','🎓','💛','🌟','🥳'];

 for(let i=0;i<90;i++){
  const el=document.createElement('div');
  el.className='confetti';
  el.innerText=emojis[Math.floor(Math.random()*emojis.length)];
  el.style.left=Math.random()*100+'vw';
  el.style.fontSize=(15+Math.random()*20)+'px';
  el.style.animationDuration=(2+Math.random()*4)+'s';
  el.style.animationDelay=Math.random()*1.5+'s';

  document.body.appendChild(el);
  setTimeout(()=>el.remove(),7000);
 }
}

</script>

</body>
</html>

