<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ask Tulona</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 50px;
      overflow: hidden; /* To prevent scrolling */
      background-color: #f1cc7b; /* Light orange background color */
    }

    #question {
      font-size: 50px;
      margin-bottom: 20px;
    }

    .option {
      font-size: 20px; /* Increased font size */
      padding: 15px 30px; /* Increased padding */
      cursor: pointer;
      position: absolute;
      background-color: #1c4c6b; /* Background color for Yes and No */
      color: #dad8d8; /* Text color for Yes and No */
      border-radius: 18px; /* Rounded corners */
      display: inline-block; /* Add this to allow setting a border */
      border: 1px solid #040c11; /* Border color for Yes and No */
      box-sizing: border-box; /* Include border in width and height */
    }

    #yesOption {
      left: 380px;
      top: 580px;
    }

    #noOption {
      left: 520px;
      top: 580px;
    }
  </style>
</head>
<body>

<div id="question">Are u free on 13 ?</div>

<div id="options">
  <div class="option" onclick="handleClick('yes')" id="yesOption">Yes</div>
  <div class="option" onmouseover="moveNoOption()" id="noOption">No</div>
</div>

<div id="gifContainer">
    <img src="huh.gif" alt="Please GIF">
</div>

<!-- <div id="dollImage">
    <img src="doll.jpg" alt="Doll Image">
</div> -->

<script>
  function moveNoOption() {
    const noOption = document.getElementById('noOption');
    const newX = Math.floor(Math.random() * window.innerWidth);
    const newY = Math.floor(Math.random() * window.innerHeight);

    noOption.style.left = newX + 'px';
    noOption.style.top = newY + 'px';
  }

  function handleClick(answer) {
    if (answer === 'no') {
      alert('Oops! You moved away, try again!');
    } else {
      window.location.href = 'index2.html';
    }
  }
</script>

</body>
</html>
