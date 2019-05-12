---
layout: "landing_page"

---

<center>

<h1>
BONUS offer expires<br>
13th May midnight PST &nbsp;&nbsp;||&nbsp;&nbsp; 14th May 8am BST<br>
<span id="demo"></span>
</h1>

<img src="/i/Mainlogo1500x500.jpg" alt="Inspiring Life Design logo" width="0" height="0">

<sub>This page contains affiliate links</sub><br><br>

{% include vimeo.html vimeoid="335513065" %}

<a href="https://cl518.isrefer.com/go/kbborder/a1899" target="_blank">
  <img src="/i/Buttons/kbb-buy-now.png" alt="KBB buy now button">
</a>

<img src='/i/2019/kbb/bonus-page-header.png' alt='Header image offering additional bonuses for the Knowledge Business Blueprint by Tony Robbins, Dean Graziosi and Russell Brunson'>

<a href="https://cl518.isrefer.com/go/kbborder/a1899" target="_blank">
  <img src="/i/Buttons/kbb-buy-now.png" alt="KBB buy now button">
</a>

</center>

<!-- Display the countdown timer in an element -->


<script type="text/javascript" src="https://moment.github.io/luxon/global/luxon.min.js"></script>
<script type="text/javascript">
    // Set the date we're counting down to (in UTC)
    var end = luxon.DateTime.fromISO("2019-05-13T23:59:59-07:00");

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
        document.getElementById("demo").innerHTML = days + "d " + hours + "h "
        + minutes + "m " + seconds + "s ";

        // If the count down is finished, write some text 
        if (diff < 0) {
            clearInterval(x);
            document.getElementById("demo").innerHTML = "OFFER IS NOW CLOSED";
        }

        diff = diff - second;

    }, second);
</script>






