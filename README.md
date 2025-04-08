<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Age Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      display: flex;
      height: 100vh;
      justify-content: center;
      align-items: center;
    }
    .container {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      text-align: center;
      width: 300px;
    }
    input[type="date"] {
      padding: 8px;
      width: 100%;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
    }
    button {
      padding: 10px 20px;
      background: #4CAF50;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
    }
    button:hover {
      background: #45a049;
    }
    #result {
      margin-top: 15px;
      font-size: 18px;
      color: #333;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Age Calculator</h2>
    <input type="date" id="birthdate">
    <button onclick="calculateAge()">Calculate</button>
    <p id="result"></p>
  </div>

  <script>
    function calculateAge() {
      const birthdate = new Date(document.getElementById("birthdate").value);
      const today = new Date();

      if (!birthdate || birthdate > today) {
        document.getElementById("result").innerText = "Please enter a valid birthdate.";
        return;
      }

      let age = today.getFullYear() - birthdate.getFullYear();
      const m = today.getMonth() - birthdate.getMonth();

      if (m < 0 || (m === 0 && today.getDate() < birthdate.getDate())) {
        age--;
      }

      document.getElementById("result").innerText = `You are ${age} years old.`;
    }
  </script>
</body>
</html>
