# Sheesh
sheesh
<!DOCTYPE html>
<html>
<head>
  <title>Do You Love Me?</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
  <style>
    body {
      background-color: #f7f7f7;
      font-family: 'Open Sans', sans-serif;
    }
    .container {
      max-width: 600px;
      margin: 40px auto;
      padding: 20px;
      background-color: #fff;
      border: 1px solid #ddd;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    .question {
      font-size: 24px;
      font-weight: bold;
      margin-bottom: 20px;
    }
    .buttons {
      display: flex;
      justify-content: space-between;
      margin-top: 20px;
    }
    .button {
      background-color: #4CAF50;
      color: #fff;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .button:hover {
      background-color: #3e8e41;
    }
    #no-button {
      position: absolute;
      top: 121px;
      left: 135px;
    }
    #gif {
      width: 100px;
      height: 100px;
      margin: 20px auto;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1 class="question">Do You Love Me?</h1>
    <div class="buttons">
      <a href="#" class="button" onclick="checkAnswer()">Yes</a>
      <a href="#" id="no-button" class="button" onclick="noAnswer()">No</a>
    </div>
    <p id="result">Waiting for your answer...</p>
    <img id="gif" src="" alt="Cute heart GIF">
  </div>

  <script>
    let noCount = 0;
    let gifs = [
      "https://media.tenor.com/Y-hMRHdsPjUAAAAM/bunny-rabbit.gif",
      
    ];

    function checkAnswer() {
      document.getElementById("result").innerHTML = "'wag mo namang ipahalata na love na love mo ako";
    }
    function noAnswer() {
      noButtonTop = Math.floor(Math.random() * (window.innerHeight - 100)) + 50;
      noButtonLeft = Math.floor(Math.random() * (window.innerWidth - 100)) + 50;
      document.getElementById("no-button").style.top = noButtonTop + "px";
      document.getElementById("no-button").style.left = noButtonLeft + "px";

      let gifIndex = Math.floor(Math.random() * gifs.length);
      document.getElementById("gif").src = gifs[gifIndex];

      noCount++;
      let messages = [
        "sakit mo naman",
        "grabe ka na sa'kin",
        "sure na ba yan?",
        "sure na sure na?",
        "Hindi na talaga mababago?",
        "mag yes ka na kasi"
      ];
      document.getElementById("result").innerHTML = messages[noCount % messages.length];
    }
  </script>
</body>
</html>
