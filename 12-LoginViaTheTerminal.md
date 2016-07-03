---
layout: default
title: Welcome yourself to the Cloud-Computing.
---

#Open a Terminal window to get started.</h3>

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
