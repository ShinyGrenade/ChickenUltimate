<!DOCTYPE html>
The reason chickens cannot fly high becaues they don't have faith in their wing or maybe they are born to be eaten.

<embed src="Chi.mp3" loop="true" autostart="true" hidden="true">

<html>
  <head>
  <h3>Money: <span id="money">0</span>  MPS: <span id="moneyPerSecond">0</span><br /> <img src="https://stickershop.line-scdn.net/stickershop/v1/product/1082755/LINEStorePC/main.png;compress=true?__=20161019" onclick="moneyClick()">Hack</img src="https://stickershop.line-scdn.net/stickershop/v1/product/1082755/LINEStorePC/main.png;compress=true?__=20161019"></h3>
  </head>
  <body>
  <h3> Hacker Earnings</h3>
  <p>Click Upgrade: <span id="clickUpgradeCost">50</span> <button onclick="buyClickUpgrade()">Buy Click Upgrade</button>
  <p><button onclick="buyBeginner()">Buy Beginner</button> Cost: <span id="beginnerCost">10</span></p>
  </body>
</html>

<embed src="Chi.mp3" loop="true" autostart="true" hidden="true">


<script>
var money = 0;
var beginner = 0;
var mpc = 1;
var moneyPerSecond = 0;
var clicks = 0;

function moneyClick(){
money += mpc;
clicks += 1;
document.getElementById("money").innerHTML = prettify(money);
}

function mps(){
  money += moneyPerSecond;
  document.getElementById('money').innerHTML = prettify(money);
  document.getElementById('moneyPerSecond').innerHTML = prettify(moneyPerSecond);
}

function buyClickUpgrade(){
  var clickUpgradeCost = Math.floor(50 * Math.pow(1.0, mpc));
  if (money >= clickUpgradeCost){
    mpc++;
    money -= clickUpgradeCost;
    document.getElementById('clickUpgradeCost').innerHTML = clickUpgradeCost;
  }
  var nextCost = Math.floor(100 * Math.pow(1.2, mpc));
  document.getElementById('clickUpgradeCost').innerHTML = nextCost;
}

function buyBeginner(){
  var beginnerCost = Math.floor(10 * Math.pow(1.1, beginner));
  if (money >= beginnerCost){
    beginner += 0.1;
    moneyPerSecond += 0.1;
    money -= beginnerCost;
    document.getElementById('money').innerHTML = prettify(money);
    document.getElementById('moneyPerSecond').innerHTML = prettify(moneyPerSecond);
  }
  var nextCost = Math.floor(10 * Math.pow(3.2, beginner));
  document.getElementById('beginnerCost').innerHTML = prettify(nextCost);
}

window.setInterval(mps, 1000);


function prettify(input){
  var output = Math.round(input * 1000000)/ 1000000;
  return output;

}

var hundredClicks = 100;

function clicks(){
  if(click == hundredClicks){
    alert("Congrats on 100 clicks");
  }
}

window.setInterval(clicks, 1);


</script>
