<!DOCTYPE html>
<html>
<head>
<title>LoveApp</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body {
  font-family: sans-serif;
  background-color: #f0f0f0;
  margin: 0;
  padding: 0;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

.heart {
  width: 100px;
  height: 100px;
  background-color: red;
  transform: rotate(-45deg);
  position: relative;
}

.heart::before,
.heart::after {
  content: "";
  width: 100px;
  height: 100px;
  background-color: red;
  border-radius: 50%;
  position: absolute;
  top: -50px;
  left: 0;
}

.heart::after {
  left: 50px;
}

h1 {
  color: #333;
  margin-top: 20px;
}

p {
  color: #666;
  text-align: center;
  margin-top: 10px;
}
</style>
</head>
<body>
<div class="container">
  <div class="heart"></div>
  <h1>LoveApp</h1>
  <p>¡Comparte el amor con el mundo!</p>
</div>
</body>
</html>
