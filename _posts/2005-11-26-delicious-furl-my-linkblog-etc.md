---
title: del.icio.us, furl, my linkblog etc.
author: bsoist
layout: post
permalink: /2005/11/26/delicious-furl-my-linkblog-etc/
dsq_thread_id:
  - 47841221
categories:
  - Fun
tags:
  - delicious
  - Fun
  - furl
  - geek
  - Links
  - tech
---
I&#8217;ve been fooling around with how to post links to my linkblog and del.icio.us for a while now. I posted about this three times in July ([14<sup>th</sup>][1], [23<sup>rd</sup>][2], [31<sup>st</sup>][3]) while I was playing with the best setup for me.Since then, I have toyed with a few different tools for managing this. In September, I developed a solution that I liked. I wrote a toolbar button which, when clicked, would take the info from the page I was on and post to my linkblog using a combination of builtin [WordPress][4] code and my own code from 7/14 and then post to [deli.icio.us][5] and redirect me to [deli.icio.us][5] &#8220;done&#8221; message. Aside from the occassional unescaped character, it worked beautifully for a while, and I liked it.Recently, I noticed that the links were not posting to my blog (I know some of you don&#8217;t understand why I even want this &#8211; that&#8217;s okay). After messing with it for a few minutes I decided to just do things another way. I wrote another toolbar button that would post to my linkblog using builtin [WordPress][4] functionality and popup (in a tab, of course) the [del.icio.us][5] post form with the tags populated. I copy the tags, submit to [del.icio.us][5], paste my tags into [WordPress][4], and submit. Quick and easy enough for me.If you use [FireFox][6] and WordPress, you can drag this link &#8212; [Post Link][7] to your toolbar.Now, edit the code as follows &#8211; replace DELICIOUSUSERNAME with your del.ici.us username and replace WORDPRESSURL with your wordpress blog URL.

 [1]: http://bsoist.geexfiles.com/index.php/2005/07/14/my-link-blog/#more-81
 [2]: http://bsoist.geexfiles.com/index.php/2005/07/23/link-managers/
 [3]: http://bsoist.geexfiles.com/index.php/2005/07/31/more-about-links/#more-91
 [4]: http://wordpress.org/
 [5]: http://deli.icio.us/
 [6]: http://getfirefox.com/
 [7]: javascript:Q=document.selection?document.selection.createRange().text:document.getSelection();var%20ext=prompt(%22Comments?%22,%22%22);var%20tags=prompt(%22Tags?%22,%22%22);window.open('http://del.icio.us/DELICIOUSUSERNAME?v=3&extended='+Q+'%20'+ext+'&tags='+tags+'&url='+encodeURIComponent(location.href)+'&title='+encodeURIComponent(document.title));location.href='WORDPRESSURL/wp-admin/bookmarklet.php?text='+encodeURIComponent(Q+'%20'+ext)+'&popupurl='+encodeURIComponent(location.href)+'&popuptitle='+encodeURIComponent(document.title);