---
layout: page
title: Advisor Tutorial
permalink: /tutorial/
---

<p class="visible-mobile">This page is best viewed on a larger screen</p>

<section id="advisor-checkin">
<p>Before continuing to the tutorial, please check in first by providing some basic information:</p>
{% include advisor-checkin.html %}
</section>

<article id="tutorial" class="hidden">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/V9RgzTnp1t0?modestbranding=1&rel=0" frameborder="0" allow="accelerometer; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</article>

<script>

checkCheckedIn();


function checkCheckedIn () {
    var checkin = $("#advisor-checkin");
    var tutorial = $("#tutorial");
    if (window.location.hash === "#checked-in") {
        checkin.addClass("hidden");
        tutorial.removeClass("hidden");
    } else {
        checkin.removeClass("hidden");
        tutorial.addClass("hidden");
    }
}

$(window).on("hashchange", function(){
    checkCheckedIn();
});

</script>
