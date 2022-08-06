---
layout: "landing_page"
sitemap:
  exclude: true  
---

<center>
<iframe width="840" height="474" src="https://www.youtube-nocookie.com/embed/nCzk4wDv8Zc?rel=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<h1>HURRY this all goes away...</h1>
<h2>
11th/12th August<br />
</h2>
<h1><span id="demo"></span></h1>

<a href="https://timetothrivechallenge.com/projectnext?source=ildpromise&a=1899" target="_blank">
  <img src="/i/Buttons/pnandbonuses.png" alt="Project Next with Bonus Bundle button">
</a>

<img src='/i/pn/2022/bonuspage.png' alt='Header image offering additional bonuses for Project Next'>


<a href="https://timetothrivechallenge.com/projectnext?source=ildpromise&a=1899" target="_blank">
  <img src="/i/Buttons/pnbuynow.png" alt="Project Next with Bonus Bundle button">
</a>

<br><br>
<sub>I am an independent Mastermind.com TM Affiliate, not an employee. I receive referral payments from Mastermind.com TM. The opinions expressed here are my own and are not official statements of Mastermind.com TM or its parent company, Mastermind.com LLC.</sub>

</center>

<!-- Display the countdown timer in an element -->


<script type="text/javascript" src="https://moment.github.io/luxon/global/luxon.min.js"></script>
<script type="text/javascript">
    // Set the date we're counting down to (in UTC)
    var end = luxon.DateTime.fromISO("2022-08-12T23:59:59-07:00");

    var second = 1000;
    var minute = 60 * second;
    var hour = 60 * minute;
    var day = 24 * hour;

    // Get todays date and time
    var date = new Date();
    var now = luxon.DateTime.local();
    var diff = end.diff(now);

    // Update the count down every 1 second
    var x = setInterval(function() {

        // Time calculations for days, hours, minutes and seconds
        var days = Math.floor(diff / day);
        var hours = Math.floor((diff % day) / hour);
        var minutes = Math.floor((diff % hour) / minute);
        var seconds = Math.floor((diff % minute) / second);

        // Display the result in the element with id="demo"
        document.getElementById("demo").innerHTML = days + " days, " + hours + " hours, "
        + minutes + " mins, " + seconds + "  ";

        // If the count down is finished, write some text 
        if (diff < 0) {
            clearInterval(x);
            document.getElementById("demo").innerHTML = "OFFER IS NOW CLOSED";
        }

        diff = diff - second;

    }, second);
</script>