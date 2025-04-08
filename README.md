<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Age Calculator</title>
  <style>
    body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: #f0f0f0;
}

.container {
  background: white;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
  text-align: center;
}

input[type="date"] {
  padding: 10px;
  margin-top: 10px;
  margin-bottom: 15px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  padding: 10px 20px;
  background-color: #0077cc;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #005fa3;
}
  </style>
</head>
<body>
  <div class="container">
    <h1>Age Calculator</h1>
    <label for="birthdate">Enter your birthdate:</label>
    <input type="date" id="birthdate">
    <button onclick="calculateAge()">Calculate Age</button>
    <p id="result"></p>
  </div>
</body>
</html>
