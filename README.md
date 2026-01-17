<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Rock Paper Scissors</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 50px;
    }

    .button-container {
      display: flex;
      justify-content: center;
      gap: 20px;
    }

    button {
      border: none;
      background: none;
      cursor: pointer;
    }

    button img {
      width: 150px;   /* Change image size here */
      height: auto;
      border-radius: 10px;
    }

    #result {
      margin-top: 30px;
      font-size: 32px;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <h1>Choose Wisely</h1>

  <div class="button-container">
    <button onclick="playGame()">
      <img src="https://i.imgur.com/bb0Ffh4.png" alt="Button 1">
    </button>

    <button onclick="playGame()">
      <img src="https://i.imgur.com/q18m5se.png" alt="Button 2">
    </button>

    <button onclick="playGame()">
      <img src="https://i.imgur.com/RLCjO2e.png" alt="Button 3">
    </button>
  </div>

  <div id="result"></div>

  <script>
    function playGame() {
      // Generates 0, 1, or 2
      const randomNumber = Math.floor(Math.random() * 3);

      const resultText = document.getElementById("result");

      if (randomNumber === 0) {
        resultText.textContent = "You Win";
      } else {
        resultText.textContent = "You Lose";
      }
    }
  </script>

</body>
</html>
