---
layout: post
title: URL rewrite with Kohana on OS X
excerpt_separator: “”
permalink: 2011/05/19/url-rewrite-with-kohana-on-osx.html
---
Today, I started to work again with the fast and small but [powerful PHP framework](http://kohanaframework.org/ "Kohana PHP Framework") Kohana. I used Kohana 1 on a Linux machine years ago but now it’s Kohana 3.1 on Mac OS X 10.6 (Snow Leopard). Anyway, shortly after the successful installation I wanted to get rid of the mentioning of *index.php* in the URL. I knew about *.htaccess* and *mod_rewrite* from my previous Kohana projects. This time the framework even came with a predefined .htaccess file. However, I didn’t get it to work and only got *404 Not Found* messages when I activated the .htaccess file.

After some research I figured out that I had to change the *None* of *AllowOverride* in */etc/apache2/users/<USER_NAME>.conf* to *All*. That got me from 404 Not Found messages to *403 Forbidden* messages. After some more research and trail and error, I found out that the trick was to append *FollowSymLinks* to the *Options* in the above mentioned conf file.