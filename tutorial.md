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
    <iframe src = "{{ site.baseurl }}/js/ViewerJS/#../../assets/Advisor Tutorial.pdf" width='100%' height='600px' allowfullscreen webkitallowfullscreen></iframe>
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