---
title: bsoist's linkblog
description: anything I find interesting enough to share
author: bsoist
layout: page
---
<address>I've obsessed about how I share links for a long time, but I have finally settled on a system I built that [works for me][1]. You can find the [RSS feed over here][2].</address>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script>
    $(function(){
        $("#includedContent").load("http://links.bsoi.st/links.html");
    });
</script>
<div id="includedContent"></div>


[1]: https://github.com/bsoist/ShortenLinks
[2]: /subscribe/
