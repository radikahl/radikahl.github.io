---
layout: post
title: schnitzeling
excerpt_separator: “”
permalink: 2012/05/28/schnitzeling.html
---
![Schnitzel](https://dl.dropbox.com/u/4255155/blog/schnitzeling.jpg "It made me stronger.")

Yeah... nerd level increased by a bit. Finally there is code running again under my domain that I can actually see, read, browser, change, modify and eat :)

Anyway... even though there is a very [straightforward step-by-step](http://schnitzelpress.org/manual/setup/) guide for setting up the [blog software](http://schnitzelpress.org/ "A Lean, Mean Blogging Machine"), I ran into a little problem: Heroku complained that I didn't specify an app just after I created the app :(

In case anyone else has the issue as well: [Good news everyone](http://www.youtube.com/watch?v=1D1cap6yETA). It can be solved by the following:
<pre>
git remote add heroku git@heroku.com:myblog.git
git config heroku.remote heroku
</pre>

Of course, you gotta have to change *myblog* to whatever you called your application (first command of step 5).