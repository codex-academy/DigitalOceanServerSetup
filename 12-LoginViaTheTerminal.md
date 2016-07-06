---
layout: default
title: Initiate the connection .1
---

# Open a Terminal window to get started.</h3>

# Step 1 — Initiate the Connection

At the command prompt, enter the following command to attempt to connect to your server as the root user


(subsitute the highlight word(*SERVER_IP_ADDRESS*) with your server's IP address):

`ssh root@SERVER_IP_ADDRESS`

For example, if the server IP address was `123.456.789.123`, the command would look like this:<br />
$<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`ssh root@123.456.789.123`

<h3>The first time you attempt to connect to your server, you will likely see a warning that looks like this:</h3>

$`The authenticity of host '123.123.123.123 (123.123.123.123)' can't be established.
ECDSA key fingerprint is 79:95:46:1a:ab:37:11:8e:86:54:36:38:bb:3c:fa:c0.Are you sure you want to continue connecting (yes/no)?`

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
Go ahead and type `yes` to continue to connect.

* Here, your computer is telling you that the remote server is not recognized. Since this is your first time connecting, this is completely expected. Skip to step 2, Authentication.

If you happened to destroy a droplet directly prior to creating the one that you are connecting to, you may see a warning like this:

<pre><code>@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!     @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@</code></pre>
* IT IS POSSIBLE THAT SOMEONE IS DOING SOMETHING NASTY!
<br />
<p>Someone could be eavesdropping on you right now (man-in-the-middle attack)!
It is also possible that a host key has just been changed.
...</p>

If this is the case, your new droplet probably has the same IP address as the old, destroyed droplet, but a different host SSH key. This is fine, and you can remove the warning, by deleting the old droplet's host key from your system, by running this command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`ssh-keygen -R SERVER_IP_ADDRESS`
Now try connecting to your server again.



<h3>Now that you know your IP from the account credentials that you have received on your email you need to have a custom (DNS~>|Domain Name Server|)</h3>


# HOW ? :open_mouth:


In order to have the domain name you need to email one of codeX mentors to create it for you, as long as you provided the proper IP Address of your droplet
and you will get your domain Name Server as something like this `username.projectcodex.co`
If you already have an app cloned onto your server that is running with port:3000

you will have to type the following url `username.projectcodex.co:3000` on your browser and you should at this stage be able to run your apps with node or nodemon or permanently run it with pm2 thereafter even if your  app server has crushed your app would automatically run again.

Then after consulting codeX mentor you would then be able to connect to your droplet server using the following command example :

`ssh username@dns`

* remember username could be the `root account` and dns could then be replaced with your `IP address` which it would result on you having to type the following command like the following:

`username@username.projectcodex.co`

:stuck_out_tongue_winking_eye: Got it!
