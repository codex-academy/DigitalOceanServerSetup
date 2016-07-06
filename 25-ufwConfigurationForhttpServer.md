---
layout: default
title: check the ufw state before modifying the ufw configuration
---

# Uncomplicated FireWall Setup

# :eyes: Check UFW Status and Rules :eyes:

At any time, you can check the status of UFW with this command:
`sudo ufw status verbose`

By default, UFW is disabled so you should see something like this:
<h3>Output:</h3>

`Status: inactive`

If UFW is active, the output will say that it's active, and it will list any rules that are set. For example, if the firewall is set to allow SSH (`port 22`) connections from anywhere, the output might look something like this:

# Configuring a Basic Firewall

This is the bare minimum firewall configuration. It will only allow traffic on your SSH port and all other services will be inaccessible. If you plan on running additional services, you will need to open the firewall at each port required.

If you plan on running an HTTP web server, you will need to allow access to port 80:<br />
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo ufw allow 80/tcp`


After you've finished adding the exceptions, you can review your selections by typing:<br />
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo ufw show added`


If everything looks good, you can enable the firewall by typing:<br />
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo ufw enable`

You will be asked to confirm your selection, so type `"y"` if you wish to continue. This will apply the exceptions you made, block all other traffic, and configure your firewall to start automatically at boot.


Remember that you will have to explicitly open the ports for any additional services that you may configure later. For more in-depth information, check out our article on configuring the ufw firewall.
