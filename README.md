 <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dikra eyniyaaa 💕</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    overflow:hidden;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(-45deg,#ff4d88,#ff7eb3,#ff9ecf,#ff5fa2);
    background-size:400% 400%;
    animation:bg 10s ease infinite;
    font-family:Arial,sans-serif;
}

@keyframes bg{
0%{background-position:0% 50%;}
50%{background-position:100% 50%;}
100%{background-position:0% 50%;}
}

.card{
    text-align:center;
    background:rgba(255,255,255,.15);
    backdrop-filter:blur(12px);
    padding:40px;
    border-radius:25px;
    color:white;
    box-shadow:0 0 30px rgba(255,255,255,.4);
    animation:zoom 2s infinite alternate;
    z-index:10;
}

.card h1{
    font-size:45px;
    margin-bottom:15px;
    text-shadow:0 0 15px white;
}

.card p{
    font-size:28px;
    color:#ffe6f0;
}

@keyframes zoom{
from{transform:scale(1);}
to{transform:scale(1.05);}
}

.heart{
    position:absolute;
    color:#fff;
    animation:fall linear infinite;
    user-select:none;
}

@keyframes fall{
0%{
transform:translateY(-100px) scale(.6);
opacity:0;
}
20%{
opacity:1;
}
100%{
transform:translateY(110vh) scale(1.4);
opacity:0;
}
}
</style>

</head>
<body>

<div class="card">
<h1>💖 Dikra eyniyaaa 💖</h1>
<p>💕 I'm Sorry 💕</p>
</div>

<script>
function createHeart(){

const heart=document.createElement("div");
heart.classList.add("heart");

const hearts=["❤️","💖","💕","💗","💓","💞","💘"];

heart.innerHTML=hearts[Math.floor(Math.random()*hearts.length)];

heart.style.left=Math.random()*100+"vw";
heart.style.fontSize=(20+Math.random()*40)+"px";
heart.style.animationDuration=(4+Math.random()*6)+"s";

document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},10000);

}

setInterval(createHeart,180);
</script>

</body>
</html>