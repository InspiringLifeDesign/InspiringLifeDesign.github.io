---
layout: "landing_page"

---

<br><br><br>
<h1>
<center>

Countdown to Facebook Live pre-event chat!<br>
Starts<br>
11pm BST/12am CEST<br>
Tuesday 30th April 2019
<p id="demo"></p>

</center>
</h1>


<center>
<img src='/i/2019/kbb/live-training.png' alt='Tony Robbins, Dean Graziosi and Russell Brunson will reveal their best kept impact and income secrets'>
</center>


<!-- Display the countdown timer in an element -->


<script>
// Set the date we're counting down to
var countDownDate = new Date("April 30, 2019 23:00:00").getTime();

// Update the count down every 1 second
var x = setInterval(function() {

  // Get todays date and time
  var now = new Date().getTime();

  // Find the distance between now and the count down date
  var distance = countDownDate - now;

  // Time calculations for days, hours, minutes and seconds
  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);

  // Display the result in the element with id="demo"
  document.getElementById("demo").innerHTML = minutes + "m " + seconds + "s ";

  // If the count down is finished, write some text 
  if (distance < 0) {
    clearInterval(x);
    document.getElementById("demo").innerHTML = "OFFER IS NOW CLOSED";
  }
}, 1000);
</script>






