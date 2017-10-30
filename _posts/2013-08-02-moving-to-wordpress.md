---
title: Moving to WordPress
author: bsoist
layout: post
pdrp_attributionLocation:
  - end
dsq_thread_id:
  - 1561168481
categories:
  - fun
---
NOTE: I wrote this over at [Fargo][1], but I cross-posted here so I could tweak the xhtml a little ( still working on templates for my numbering and such). You are reading this on a WordPress powered website. Keep that in mind as you read. I&#8217;m a BIG FAN of WordPress. <img src='http://archive.whsjr.soistmann.com/oped/wp-includes/images/smilies/icon_smile.gif' alt=':)' class='wp-smiley' /> 

Yesterday the [comments over at AVC][2] became quite a love fest for WordPress.

I&#8217;m a big fan of WordPress, and I recommend it to clients and friends all the time, but I don&#8217;t think moving a high profile, heavy traffic website like AVC over to WordPress is a trivial matter.

## I&#8221;ll explain, but first &#8230;

These opinions and suggestions were written with one website in mind. This post is not intended to be advice or a tutorial fit for anyone and everyone to follow.

They are also just that &#8211; opinions and suggestions.

## Why not WordPress?

To be clear, I&#8217;m not against AVC moving to WordPress, but there is one reason I think it&#8217;s worth avoiding WordPress &#8211; or any dynamically driven solution.

  * AVC.com is one of my favorite spots on the Internet. Fred Wilson uses it to share his thoughts on a daily basis, and there is a lot of valuable information there. The comment section is also chock full of the opinions of some very smart people. I&#8217;ve been working on writing something up about that, but that&#8217;s a topic for another day.
  * The content over at AVC should be preserved for future generations. If the content were static, moving it over to another location would be as simple as copying files to a new location. It is now possible to set up an S3 bucket on AWS and serve files from that bucket with no need for a server to maintain. I know that presumes that Amazon will survive and that they will continue to offer S3, but the point remains that serving static content these days is a trivial thing.
  * Working with a database driven website is not. Sure it&#8217;s simple &#8211; even easy for people like me ( and for the three of you that read my blog ), but it requires maintenance of several &#8220;moving parts.&#8221;

## If Fred decides to move to WP, what might be the best way to do that?

There are a lot of tutorials online about this, so I&#8217;m not going into great detail, but this is how it starts.

  1. Finish the new design first. Moving first would require building ( or skinning ) a theme one extra time.
  2. Have an xhtml/CSS professional build a WP theme from that design OR use a theme that can be skinned by a CSS pro.
  3. Export data from the database and have someone who can work with SQL massage the details, paying special attention to the permalinks. Breaking URLs is a huge mistake.
  4. Find a good host known for handling high traffic WordPress sites.
  5. From here, follow the standard procedure, but be sure of three things &#8230; 
      1. Don&#8217;t use more plugins than you really need, make sure they don&#8217;t conflict with one another, and that they are not poorly coded.
      2. Test for performance under extreme load
      3. Be sure you can access old posts at the existing URLs

## But wait, there is a plugin for that &#8230;

I know there are solutions to the issues one might encounter moving to WordPress &#8211; some that I mentioned ( permalinks, performance issues ), and some I did not ( unicode differences, etc. ). My point, after all, is that these issues should be addressed, which implies that they can be addressed. I just think the best approach is to be sure a programmer ( or someone with the right combination of tech savvy, smarts, courage, patience, and time ) carefully handles the transition.

A plugin is only as good as the programmer who built it &#8211; or the last one who edited it. There are, no doubt, many plugins that are very well done, but anyone who has used WordPress to drive a site with any significant traffic will probably tell you stories of plugins that don&#8217;t work as advertised or conflict with other plugins or the core function of WordPress.

## TL;DR

Moving a high profile, heavy traffic, long lived website is not a trivial matter &#8211; no matter where you want to take it.

 [1]: http://bsoist.smallpict.com/2013/08/02/movingToWordpress
 [2]: http://www.avc.com/a_vc/2013/08/a-table-of-contents-for-mba-mondays.html#comments
