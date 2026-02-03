index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Astha ❤️ Parth</title>

<style>
body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(135deg, #ffd1dc, #ff4d6d);
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Comic Sans MS', cursive;
}

.card {
  background: #fff0f5;
  padding: 22px;
  border-radius: 25px;
  text-align: center;
  width: 340px;
  position: relative;
  z-index: 2;
  box-shadow: 0 15px 40px rgba(0,0,0,0.3);
}

h1 {
  color: #ff3366;
}

p {
  color: #ff4d6d;
  font-size: 17px;
}

img {
  width: 100%;
  border-radius: 18px;
  margin: 8px 0;
}

button {
  padding: 12px 25px;
  margin: 8px;
  border: none;
  border-radius: 20px;
  font-size: 16px;
  cursor: pointer;
  position: relative;
}

.yes {
  background: #ff4d6d;
  color: white;
}

.no {
  background: #ffd1dc;
  color: #ff3366;
  position: absolute;
}

/* Floating hearts */
.heart {
  position: absolute;
  font-size: 20px;
  animation: float 6s linear infinite;
}

@keyframes float {
  0% {
    transform: translateY(100vh) scale(0.6);
    opacity: 1;
  }
  100% {
    transform: translateY(-10vh) scale(1.3);
    opacity: 0;
  }
}
</style>
</head>

<body>

<!-- Background Music -->
<audio autoplay loop>
  <source src="until-i-found-you.mp3" type="audio/mpeg">
</audio>

<div class="card">
  <h1>Astha 💖 Parth</h1>

  <img src="image1.jpg">
  <img src="image2.jpg">

  <p>
    From the moment I met you,<br>
    my heart chose you 💞<br><br>
    Parth… will you be my Valentine? 🌹✨
  </p>

  <button class="yes" onclick="yesClicked()">Yes 💍💖</button>
  <button class="no" id="noBtn">No 🙈</button>

  <div id="result"></div>
</div>

<script>
function yesClicked() {
  document.getElementById("result").innerHTML =
    "YAYYY 🥰💘 I found my forever… Happy Valentine’s Parth 🌹❤️";
}

// Runaway No button
const noBtn = document.getElementById("noBtn");

noBtn.addEventListener("mouseover", () => {
  const x = Math.random() * 200 - 100;
  const y = Math.random() * 150 - 75;

  noBtn.style.transform = `translate(${x}px, ${y}px)`;
});

// Floating hearts
setInterval(() => {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = ["💖","💘","💝","❤️"][Math.floor(Math.random()*4)];
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = Math.random() * 20 + 15 + "px";
  document.body.appendChild(heart);

  setTimeout(() => heart.remove(), 6000);
}, 350);
</script>

</body>
</html>
