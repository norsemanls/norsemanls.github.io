---
layout: page
title: Contact Us
permalink: /contact/
---

{% include contact-form.html %}


<script>
    $(document).ready(function() {
        if(window.location.hash === "#thanks") {
            sweetThanks();
            removeHash();
        }
    });

    function removeHash () {
        history.pushState("", document.title, window.location.pathname + window.location.search);
    }

    function sweetThanks() {
        swal(
            "Thanks for your message",
            "We'll get back to you as soon as we can.",
            "success"
        );
    }
</script>

