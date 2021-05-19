---
layout: "landing_page"

---

<center>
<h1>
Diamonds In Disney Hustle Page
</h1>
<h3>
<p id="countdown"></p>
</h3>
<h4>
Coaches still needed:  9<br />
Coaches needed breakdown:  2 Emerald, 3 further coaches<br />
</h4>
</center>

<table width="1000" style="margin: 5px 5px 5px 5px;">
<tr>
<td>
<img src="/i/beachbody/topten.jpg">
</td>
<td>
<h4>Try a different Power Hour each day:</h4>
{% include youtubewithtime.html videoid="WrOgLmH4sRY" timeid="246" %}
<br />
{% include youtubewithtime.html videoid="fXlQt0TfRYE" timeid="146" %}
</td>
</tr>
<tr>
<td>
<h4>Useful Links:</h4>
</td>
<td>

</td>
</tr>
</table>

Get the party happening on my Instagram profile page (feed, profile, highlights)



<!-- Display the countdown timer in an element -->


<script>
// Set the date we're counting down to
var countDownDate = new Date("Jun 9, 2021 23:55:00").getTime();

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

  // Display the result in the element with id="countdown"
  document.getElementById("countdown").innerHTML = days + " days " + hours + "h " + minutes + "m " + seconds + "s";

  // If the count down is finished, write some text 
  if (distance < 0) {
    clearInterval(x);
    document.getElementById("countdown").innerHTML = "IT'S HAPPENING!";
  }
}, 1000);
</script>
