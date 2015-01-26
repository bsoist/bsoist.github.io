---
title: How I Shorten Links
layout: post
categories:
    Fun
---
One of the things I've obsessed about the most over the years is how I share links. I've always wanted a way to shorten links but have a way to control the whole thing myself and/or move to other systems when necessary. 
For a while I use Adjix which I really liked and the idea was that I could take those links with me. This proved a great idea because the service disappeared and I was able to take my links with me.
by rolling my own solution this time - <a href="https://github.com/bsoist/ShortenLinks">ShortenLinks</a>
I have a Cloud Cannon site at http://links.cloudvent.net. This site is nothing but a bunch of folders that contain one index file that redirects to another URL. I also have an Apache2 server that redirects my short links to those cloud cannon pages. This allows me to add links from any of my computers where I have Dropbox installed without having to be logged in to the server.
Let's look at an example.
	Apache2 redirects http://07.bsoi.st to http://links.cloudvent.net/07
	http://links.cloudvent.net/07/index.html redirect to http://what-if.xkcd.com/30/
If I were to try to make a short link for that URL again, my script would simple print http://07.bsoi.st so I could share the short link. 
If I try to share a new link, linkit.py will ... 
	find an unused short string
	save that and the URL to the CSV file that keeps the history
	create the index.html page and folder in links.coudvent.net
	create the redirect rule and save it to a config file in links.cloudvent.net
I have a cron job ( grab_config.sh ) that runs as root on my server and looks for the config file and updates Apache accordingly.

