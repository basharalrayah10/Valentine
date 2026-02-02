<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<title>For Hiba 💖</title>  
  
<style>  
  body {  
    margin: 0;  
    height: 100vh;  
    font-family: "Arial Rounded MT Bold", Arial, sans-serif;  
    background: radial-gradient(circle, #ffd1e8, #ff9acb);  
    display: flex;  
    flex-direction: column;  
    align-items: center;  
    justify-content: center;  
    overflow: hidden;  
  }  
  
  h1 {  
    color: #ff2f92;  
    text-align: center;  
    z-index: 3;  
    text-shadow: 0 0 10px white;  
  }  
  
  /* Hello Kitty background */  
  .kitty {  
    position: absolute;  
    width: 420px;  
    opacity: 0.6;  
    z-index: 1;  
  }  
  
  .buttons {  
    position: relative;  
    width: 340px;  
    height: 220px;  
    z-index: 3;  
  }  
  
  button {  
    border: none;  
    border-radius: 40px;  
    padding: 14px 30px;  
    font-size: 18px;  
    cursor: pointer;  
    transition: all 0.2s ease;  
  }  
  
  #yes {  
    background: #ff4da6;  
    color: white;  
  }  
  
  #no {  
    background: #777;  
    color: white;  
    position: absolute;  
    left: 180px;  
    top: 100px;  
  }  
  
  /* Sparkles */  
  .sparkle {  
    position: absolute;  
    width: 6px;  
    height: 6px;  
    background: white;  
    border-radius: 50%;  
    animation: float 4s infinite ease-in-out;  
    opacity: 0.8;  
  }  
  
  @keyframes float {  
    0% { transform: translateY(0); opacity: 0.8; }  
    100% { transform: translateY(-120px); opacity: 0; }  
  }  
</style>  
</head>  
  
<body>  
  
<h1>Hiba 💕<br>Will you be my Valentine?</h1>  
  
<img  
  class="kitty"  
  src="https://upload.wikimedia.org/wikipedia/en/0/05/Hello_Kitty_character_portrait.png"  
  alt="Hello Kitty"  
/>  
  
<div class="buttons">  
  <button id="yes" onclick="yesClicked()">Yes 💖</button>  
  <button id="no" onmouseover="moveNo()">No 🙈</button>  
</div>  
  
<!-- 🎵 AUDIO (replace file name with yours) -->  
<audio autoplay loop>  
  <source src="clueless-whisper-instrumental.mp3" type="audio/mpeg">  
</audio>  
  
<script>  
  // Make sparkles  
  for (let i = 0; i < 40; i++) {  
    const s = document.createElement("div");  
    s.className = "sparkle";  
    s.style.left = Math.random() * 100 + "vw";  
    s.style.top = Math.random() * 100 + "vh";  
    s.style.animationDuration = 2 + Math.random() * 3 + "s";  
    document.body.appendChild(s);  
  }  
  
  // Yes button slowly grows over time  
  setInterval(() => {  
    const yes = document.getElementById("yes");  
    const size = parseInt(getComputedStyle(yes).fontSize);  
    yes.style.fontSize = size + 1 + "px";  
  }, 1200);  
  
  function moveNo() {  
    const no = document.getElementById("no");  
    const yes = document.getElementById("yes");  
  
    const x = Math.random() * 260;  
    const y = Math.random() * 160;  
  
    no.style.left = x + "px";  
    no.style.top = y + "px";  
  
    const size = parseInt(getComputedStyle(yes).fontSize);  
    yes.style.fontSize = size + 3 + "px";  
  }  
  
  function yesClicked() {  
    document.body.innerHTML = `  
      <h1 style="color:#ff2f92; text-align:center;">  
        Yayyy Hiba! 💘🐱✨<br>  
        It’s a date 💖  
      </h1>  
    `;  
  }  
</script>  
  
</body>  
</html>  
