# Friend-
<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Secret Question 💌</title>
<style>
body {
  margin:0;
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  background:linear-gradient(135deg,#ffe6f0,#fff5f9);
  font-family:Arial, sans-serif;
  overflow:hidden;
}

.card{
  background:white;
  padding:30px;
  border-radius:25px;
  text-align:center;
  width:90%;
  max-width:340px;
  box-shadow:0 15px 40px rgba(0,0,0,0.15);
  position:relative;
}

h2{
  color:#ff4f8b;
}

button{
  padding:12px 20px;
  border:none;
  border-radius:25px;
  font-size:16px;
  cursor:pointer;
  margin:10px;
  transition:0.3s;
}

#yes{
  background:#ff4f8b;
  color:white;
}

#no{
  background:#ddd;
  position:absolute;
}

.popup{
  display:none;
  margin-top:20px;
  font-size:18px;
  color:#ff4f8b;
}

.heart{
  position:absolute;
  color:#ff4f8b;
  animation:float 3s linear infinite;
}

@keyframes float{
  0%{transform:translateY(0);}
  100%{transform:translateY(-100vh);}
}
</style>
</head>

<body>

<div class="card">
  <h2>Hey Shopao 😌<br>Will you be my Valentine?</h2>

  <button id="yes">Yes 😳</button>
  <button id="no">No 🙈</button>

  <div class="popup" id="popup">
    Ayyy grabe siya 😆💖<br>
    Hindi na friend yan ahhh 👀✨
  </div>
</div>

<script>
const noBtn = document.getElementById("no");
const yesBtn = document.getElementById("yes");
const popup = document.getElementById("popup");

noBtn.addEventListener("mouseover", ()=>{
  const x = Math.random()*250;
  const y = Math.random()*250;
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
});

yesBtn.addEventListener("click", ()=>{
  popup.style.display="block";
  yesBtn.style.display="none";
  noBtn.style.display="none";
  createHearts();
});

function createHearts(){
  setInterval(()=>{
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML="💖";
    heart.style.left=Math.random()*100+"vw";
    heart.style.bottom="0px";
    heart.style.fontSize=(Math.random()*20+15)+"px";
    document.body.appendChild(heart);

    setTimeout(()=>{heart.remove();},3000);
  },300);
}
</script>

</body>
</html>
