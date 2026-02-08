<!DOCTYPE html>
<html>
<head>
<title>Rose Day Surprise</title>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #111;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  text-align: center;
}

/* Pages */
.page {
  display: none;
}

.active {
  display: block;
}

/* Button */
button {
  padding: 12px 25px;
  font-size: 18px;
  border: none;
  border-radius: 25px;
  background: deeppink;
  color: white;
  cursor: pointer;
  margin-top: 20px;
}

button:hover {
  background: hotpink;
}

/* Rose */
.rose {
  position: relative;
  width: 120px;
  height: 120px;
  margin: 20px auto;
  animation: bloom 3s ease-out forwards;
}

.petal {
  position: absolute;
  width: 60px;
  height: 90px;
  background: pink;
  border-radius: 60px 60px 0 0;
  transform-origin: bottom center;
  opacity: 0;
  animation: open 2.5s ease forwards;
}

.petal:nth-child(1){transform:rotate(0deg);animation-delay:0.2s;}
.petal:nth-child(2){transform:rotate(45deg);animation-delay:0.4s;}
.petal:nth-child(3){transform:rotate(90deg);animation-delay:0.6s;}
.petal:nth-child(4){transform:rotate(135deg);animation-delay:0.8s;}
.petal:nth-child(5){transform:rotate(180deg);animation-delay:1s;}
.petal:nth-child(6){transform:rotate(225deg);animation-delay:1.2s;}
.petal:nth-child(7){transform:rotate(270deg);animation-delay:1.4s;}
.petal:nth-child(8){transform:rotate(315deg);animation-delay:1.6s;}

.center {
  position: absolute;
  width: 40px;
  height: 40px;
  background: deeppink;
  border-radius: 50%;
  top: 40px;
  left: 40px;
}

@keyframes open {
  from {opacity:0; transform:scale(0);}
  to {opacity:1; transform:scale(1);}
}

@keyframes bloom {
  from {transform:scale(0.3);}
  to {transform:scale(1);}
}
</style>
</head>

<body>

<!-- PAGE 1 -->
<div id="page1" class="page active">
  <h1>Sorry… late ayinanduku ❤️</h1>
  <p>Please click below</p>
  <button onclick="showPage2()">Pallavi</button>
</div>

<!-- PAGE 2 -->
<div id="page2" class="page">
  <h1>🌸 Happy Rose Day Bangaram 🌸</h1>

  <div class="rose">
    <div class="petal"></div>
    <div class="petal"></div>
    <div class="petal"></div>
    <div class="petal"></div>
    <div class="petal"></div>
    <div class="petal"></div>
    <div class="petal"></div>
    <div class="petal"></div>
    <div class="center"></div>
  </div>
</div>

<script>
function showPage2() {
  document.getElementById("page1").classList.remove("active");
  document.getElementById("page2").classList.add("active");
}
</script>

</body>
</html>
