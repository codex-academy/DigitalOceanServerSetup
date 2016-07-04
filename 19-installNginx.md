---
layout : default
title : Install Nginx .4
---

# 5.Install Nginx

<h2>OVERVIEW</h2>

Nginx (pronounced "engine x") is a free, open-source, high-performance HTTP server. Nginx is known for its stability, rich feature set, simple configuration, and low resource consumption. For these reasons, it is a great alternative to the more commonly used Apache web server.

Following the steps below will show you how to install Nginx and test its functionality. Be sure to follow our more advanced how-to on configuring virtual hosts afterwards, which will give you the ability to serve multiple websites from your (VPS) Server.

<h3>Install Nginx with command</h3>

5.a)<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`apt-get install Nginx`

By default, Nginx will not start automatically, so you need to use the following command. Other valid options are `stop` and `restart`.
 To restart we need to run the following command:

 <input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
 `sudo /etc/init.d/nginx start`

<h3>The results should be like the following.</h3>

* `Starting nginx`:
 the configuration file /etc/nginx/nginx.conf syntax is ok
configuration file /etc/nginx/nginx.conf test is successful nginx.

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">`Test Nginx by pointing your web browser to your domain name or IP address. You should see the default Nginx page as shown in Figure 1 below: `

# Figure 1
![image-title-here](/img/posts_Schematics/Checkifnginxisinstalled.png){:class="img-responsive"}
