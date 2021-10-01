---
layout: "landing_page"

---

<center>
<h1>
October Team Cup
</h1>
<h3>
Team Cup Time Remaining:
<p id="countdown"></p>
</h3>
<table class="table table-colored">
  <thead>
    <tr>
      <th style="text-align: left">Team Member</th>
      <th style="text-align: center">Success Club Goal</th>
      <th style="text-align: center">Current Success Club points</th>
      <th style="text-aligh: center">Success Club points still needed</th>
      <th style="text-aligh: center">Start Rank</th>      
      <th style="text-aligh: center">Goal Rank</th>
      <th style="text-aligh: center">End Rank</th>
      <th style="text-aligh: center">Cup Points</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left">Alex</td>
      <td style="text-align: center">10</td>
      <td style="text-align: center">0</td>
      <td style="text-align: center">10</td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center">0</td>
    </tr>
    <tr>
      <td style="text-align: left">Christina</td>
      <td style="text-align: center"></td>
      <td style="text-align: center">0</td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center">0</td>
    </tr>
    <tr>
      <td style="text-align: left">Corinna</td>
      <td style="text-align: center">10</td>
      <td style="text-align: center">0</td>
      <td style="text-align: center">10</td>
      <td style="text-align: center">Emerald</td>
      <td style="text-align: center">Emerald</td>
      <td style="text-align: center"></td>
      <td style="text-align: center">0</td>      
    </tr>
    <tr>
      <td style="text-align: left">Cynthia</td>
      <td style="text-align: center">10</td>
      <td style="text-align: center">0</td>
      <td style="text-align: center">10</td>    
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center">0</td>        
    </tr>
    <tr>
      <td style="text-align: left">Keri</td>
      <td style="text-align: center"></td>
      <td style="text-align: center">0</td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center">0</td>      
    </tr>
    <tr>
      <td style="text-align: left">TOTAL</td>
      <td style="text-align: center"></td>
      <td style="text-align: center">0</td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center"></td>
      <td style="text-align: center">0</td>      
    </tr>
  </tbody>
</table>
</center>
<h4>How We Earn Cup Points:</h4>
<h5>
1 Cup Point: 1 Success Club point<br />
3 Cup Points: Rank advancement<br />
3 Cup Points: Rank advancement of a PS coach<br />
</h5>


<table width="1000" style="margin: 5px 5px 5px 5px;">
<tr>
<td>
<img src="/i/beachbody/topten.jpg">
</td>
<td>
<h4>Try a different Power Hour each day:</h4>
{% include youtubewithtime.html videoid="zKO7933aaDY" %}
<br />
{% include youtubewithtime.html videoid="D19cu6P64uY" %}
<br />
{% include youtubewithtime.html videoid="WrOgLmH4sRY" timeid="246" %}
<br />
{% include youtubewithtime.html videoid="fXlQt0TfRYE" timeid="146" %}
</td>
</tr>
<tr>
<td>
</td>
<td>

</td>
</tr>
</table>




<!-- Display the countdown timer in an element -->


<script>
// Set the date we're counting down to
var countDownDate = new Date("Nov 1, 2021 6:59:00").getTime();

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
