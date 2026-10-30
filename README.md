# Pkb9999<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PNB9999 Trading</title>
<style>
body{background:#0b1220;color:white;font-family:Arial;padding:15px}
.card{background:#17243a;padding:15px;border-radius:12px;margin-bottom:15px}
.price{color:#00e5a0;font-size:26px;font-weight:bold}
button{flex:1;padding:12px;border:none;border-radius:8px;color:white;font-weight:bold}
.buy{background:#00a878} .sell{background:#e53546}
.row{display:flex;gap:10px;margin-top:10px}
</style>
</head>
<body>
<h1 style="color:#00e5a0;text-align:center">PNB9999 Trading</h1>

<div class="card">
<h3>मेरा बैलेंस</h3>
<div class="price" id="bal">₹100000</div>
</div>

<div class="card">
<h3>RELIANCE</h3>
<div class="price" id="price">₹1450</div>
<div class="row">
<button class="buy" onclick="buy()">BUY</button>
<button class="sell" onclick="sell()">SELL</button>
</div>
</div>

<script>
let balance = 100000;
let price = 1450;
function buy(){
 if(balance>=price){
  balance-=price;
  document.getElementById('bal').innerText='₹'+balance;
  alert('Buy Ho Gaya!');
 }
}
function sell(){
 balance+=price;
 document.getElementById('bal').innerText='₹'+balance;
 alert('Sell Ho Gaya!');
}
// Live price hilane ke liye
setInterval(()=>{
 price = (1450 + (Math.random()-0.5)*10).toFixed(2);
 document.getElementById('price').innerText='₹'+price;
},2000);
</script>
</body>
</html>
