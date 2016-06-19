---
title: Updating ShortenLinks
layout: post
categories:
    - fun
---
I've updated [ShortenLinks](https://github.com/bsoist/ShortenLinks) a bit since [my last post][lastpost] on the subject so I thought I'd document it again. If you're more interesting in why I set things up this way, [that post][lastpost] and other past posts on the subject might be more helpful.

The DNS zone file for the domain I use has CNAMEs set up for a couple of subdomains I use for other things - this one ( www ) included - and the any other subdomain and the apex point to an Apache server I run on EC2.

My apache2 config for this domain has two virtual hosts.

One is for the apex domain and it redirects to my [about page](http://www.bsoi.st/about/).

The other is for * and is set to a folder where I have a CGI script ( linkscgi.py saved with the name index.cgi ) that does a location redirect to my Cloud Cannon site. 

So for any subdomain I don't have reserved already, `sub.bsoi.st` will redirect to `links.cloudvent.net/sub/`

My [previous post][lastpost] explains how those folders are creating using linkit.py.

[lastpost]: {% post_url 2014-03-08-how-i-shorten-links %}
