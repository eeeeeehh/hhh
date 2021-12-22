
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
    
body {background-color: #222;}
    
p {
    text-align: center;
    font-size: 70px;
    margin-top:50px;
    font-family: fantasy;
    color:antiquewhite;
}

 h2 {
    text-align: center; 
    color: antiquewhite;
    margin-top:200px;
    font-size: 40px; 
    font-weight: normal;
    font-family: fantasy;

}
    
</style>
</head>
<body>
    
<h2>До конца экзамена осталось</h2>
<p id="demo"></p>

<script>
    
var countDownDate = new Date("Jan 12, 2022 13:00").getTime();

var x = setInterval(function() {

    var now = new Date().getTime();
    
    var distance = countDownDate - now;
   
    var days = Math.floor(distance / (1000 * 60 * 60 * 24));
    var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    var seconds = Math.floor((distance % (1000 * 60)) / 1000);
   
    document.getElementById("demo").innerHTML = days + " день " + hours + " часа "
    + minutes + " минуты " + seconds + " секунды ";
    
    if (distance < 0) {
        clearInterval(x);
        document.getElementById("demo").innerHTML = "а все уже";
    }
}, 1000);
    
                     </script>
