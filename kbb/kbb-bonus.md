---
layout: "landing_page"

---

<h1>
<center>

This BONUS offer expires May 13th, 2019 at 11:59pm PST
<p id="demo"></p>

</center>
</h1>

<center>
<img src='/i/2019/kbb/bonus-page-header.png' alt='Header image offering additional bonuses for the Knowledge Business Blueprint by Tony Robbins, Dean Graziosi and Russell Brunson'>

<br>

<a href="https://cl518.isrefer.com/go/kbborder/a1899" target="_blank">
  <img src="/i/Buttons/kbb-buy-now.png" alt="KBB buy now button">
</a>

</center>
<br>


<!-- Display the countdown timer in an element -->


<script>
// Set the date we're counting down to
var countDownDate = new Date("May 13, 2019 04:59:00").getTime();

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
  document.getElementById("demo").innerHTML = days + "d " + hours + "h "
  + minutes + "m " + seconds + "s ";

  // If the count down is finished, write some text 
  if (distance < 0) {
    clearInterval(x);
    document.getElementById("demo").innerHTML = "OFFER IS NOW CLOSED";
  }
}, 1000);
</script>






