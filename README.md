<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Para mi Mimi 🩵</title>
<style>
body {
  background: linear-gradient(45deg, #ff4e50, #f9d423);
  font-family: Arial;
  text-align: center;
  color: white;
  padding-top: 40px;
  overflow: hidden;
}

h1 { font-size: 40px; }
h2 { font-size: 30px; }

button {
  padding: 15px 30px;
  font-size: 22px;
  border: none;
  border-radius: 30px;
  cursor: pointer;
  margin: 10px;
}

#si {
  background: #00ff99;
  color: black;
  box-shadow: 0 0 15px white;
}

#no {
  background: #ff0055;
  color: white;
  position: absolute;
}

img {
  width: 300px;
  border-radius: 20px;
  box-shadow: 0 0 20px white;
  margin-top: 20px;
}

.heart {
  position: fixed;
  color: pink;
  font-size: 25px;
  animation: float 6s infinite;
}

@keyframes float {
  0% { bottom: 0; opacity: 1; }
  100% { bottom: 100%; opacity: 0; }
}
</style>
</head>

<body>

<h1> He estado preparando esto,
y queria hacerte una pregunta...(demasiado importante para tito)</h1>
<p>Haz clic para descubrir tu sorpresa…</p>

<button onclick="mostrar()">Abrir sorpresa 🎁</button>

<div id="contenido" style="display:none;">
  <h2>¿Puedes ser mi Valentín este 14 de febrero? PORFAVOR</h2>
  <p>Compré esto para nuestra cita 🎬</p>

  <!-- CAMBIA entradas.jpg POR TU FOTO -->
  <img src="cine.jpg">

  <p>Prometo hacerte muy feliz ese día 💕</p>

  <div>
    <button id="si" onclick="alert('Sabía que dirías que sí 😍 Te amo, Mimi 💖')">Sí 💘</button>
    <button id="no">No 🙄</button>
  </div>
</div>

<script>
function mostrar() {
  document.getElementById("contenido").style.display = "block";
}

// Botón NO que huye
const no = document.getElementById("no");
no.addEventListener("mouseover", () => {
  let x = Math.random() * (window.innerWidth - 100);
  let y = Math.random() * (window.innerHeight - 100);
  no.style.left = x + "px";
  no.style.top = y + "px";
});

// corazones flotando
setInterval(() => {
  let heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "💖";
  heart.style.left = Math.random() * 100 + "vw";
  document.body.appendChild(heart);
  setTimeout(() => heart.remove(), 6000);
}, 500);
</script>

</body>
</html>
