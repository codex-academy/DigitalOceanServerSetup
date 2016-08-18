---
layout : default
title : Recently installed program configurations
---

# Recently installed program configurations


Now lets say we are done with all the installations then how would you gain access to those programs ?
Lets make an example of Git, now you just discovered that you should make a small change on your application files and you modified app.js file
Then your ran

`VirtualPrivateServer`$`git add app.js` :white_check_mark:

Then you cannot really commit your file changes from the server till you get the configuration part done.

As a result of the following git command which you would then execute:

`VirtualPrivateServer`$`git commit -m "I just made some specific change"` :x:

then you will get the following message :

![image-title-here](/img/posts_Schematics/firstExGitConfig.png){:class="img-responsive"}


# Why ?

Because you haven't fully configured you Environment.

# Programs to be configured:

* continue with Git

* mysql-server

* Nginx

* pm2

* Already done with firewall, if not you can go to :point_right: [UFW configuration](/25-ufwConfigurationForhttpServer.html).

Lets start by following the menu on our left hand :arrow_lower_left:
