<!DOCTYPE html>
<html>
<head>
  <title>Row Counter</title>
  <style>
    body {
      background-image:url("C:\Users\Joshika Reddy\OneDrive\Pictures\bgimage.jpg.png");
      background-size: cover;
      background-position: center;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
      margin: 0;
    }
    .container {
      text-align: center;
      background-color :darkgray;
      padding: 30px 50px;
      border-radius: 10px;
      box-shadow :brown;
    }
    h1 {
      font-size: 2em;
      margin-bottom: 10px;
    }
    h2 {
      font-size: 3em;
      margin: 10px 0;
    }
    .btn {
      border: none;
      color: white;
      padding: 10px 25px;
      font-size: 16px;
      border-radius: 5px;
      margin: 5px;
      cursor: pointer;
      transition: 0.2s;
    }
    .btn:hover {
      transform: scale(1.05);
    }
    .red {
      background-color :red;
    }
    .green {
      background-color :green;
    }
    #save-el {
      font-weight: bold;
      margin-top: 15px;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Row Counter</h1>
    <h2 id="count-el">0</h2>
    <button id="increment-btn" class="btn red">INCREMENT</button>
    <button id="save-btn" class="btn green">SAVE</button>
    <p id="save-el">Previous entries: </p>
  </div>
  <script>
    let countEl = document.getElementById("count-el");
    let saveEl = document.getElementById("save-el");
    let count = 0;
    document.getElementById("increment-btn").addEventListener("click", function() {
      count += 1;
      countEl.textContent = count;
    });
    document.getElementById("save-btn").addEventListener("click", function() {
      saveEl.textContent += count + " - ";
      count = 0;
      countEl.textContent = count;
    });
  </script>
</body>
</html>
