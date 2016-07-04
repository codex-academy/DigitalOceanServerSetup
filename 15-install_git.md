---
layout : default
title : Install GIT .1
---

<h3>1.Install GIT</h3>

Once you have logged on, install GIT (we are going to use GIT to sync our work from github so our projects could exist on our digitalOcean cloud server which is our [VPS/Droplet] )

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo apt-get update && sudo apt-get install git`

The word sudo indicates that you want to run this command as root. You will be prompted for your password - i.e. the safe user password. When you provide your password, the command will run.

`sudo apt-get update && sudo apt-get dist-upgrade && sudo apt-get autoremove`
The one-line command above updates Ubuntu repositories, updates existing installed packages and removes unnecessary packages from your systems.
