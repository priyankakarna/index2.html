
<!DOCTYPE html>
<html>
<head>
 <title></title>
 <link rel="stylesheet" type="text/css" href="style.css">
 <link href="https://fonts.googleapis.com/css?family=Acme" rel="stylesheet">
</head>
<body>

<div class="container">
 <h1>JS LUDO</h1>

 <div class="dice">
  <p>Player 1</p>
  <img src="images/dice1.png" id="check1">
 </div>
 <div class="dice">
  <p>Player 1</p>
  <img src="images/dice6.png" id="check2">
 </div>

 <div>
  <button onclick="ludogame()"> Click ME</button>
 </div>
</div>


<script>

 ludogame = () => { 
 const play1 = Math.floor(Math.random() * 6) + 1; 
 const play1dice = `images/dice${play1}.png`;
 document.getElementById('check1').setAttribute('src', play1dice);

 const play2 = Math.floor(Math.random() * 6) + 1; 
 const play2dice = `images/dice${play2}.png`;
 document.getElementById('check2').setAttribute('src', play2dice);

 if(play1 > play2) 
  { document.querySelector('h1').innerHTML="Player 1 won :)";
 } else if(play1 < play2) {
   document.querySelector('h1').innerHTML="Player 2 won :)";
 } else{ document.querySelector('h1').innerHTML="DRAW "; }
}

</script>
</body>
</html>







