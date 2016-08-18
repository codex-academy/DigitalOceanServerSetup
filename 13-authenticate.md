---
layout: default
title: Authenticate .2
---


# Authenticate

* The authentication step involves providing a password and/or a private SSH key to prove that you are authorized to log in as root.

If you added an SSH key to your Droplet, and you have the private key installed on your computer, OpenSSH will attempt to use the key to authenticate to the root account. If you used a key with a passphrase, you will need to provide the passphrase to complete the login process. At this point, if you are unable to log in, you may need to start your ssh-agent and add your SSH keys to it with the following command (assuming your key is called "id_rsa"), then go back to [Step 1](/12-LoginViaTheTerminal.html) :arrow_up: :

eval `ssh-agent -s`

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`LocalMachine`$`ssh-add ~/.ssh/id_rsa`

If you did not add an SSH key to your Droplet, you will be prompted for the temporary password, and you will also be required to change it.

# Follow these steps to complete the login process:

<h3>Copy the temporary password from the email, and paste it into the password prompt</h3>

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`VirtualPrivateServer [PROMPT]`$ At the (current) UNIX password prompt, paste in the temporary password again<br />

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`VirtualPrivateServer [PROMPT]`$ At the Enter new UNIX password prompt, enter a strong password<br />

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`VirtualPrivateServer [PROMPT]`$ At the Retype new UNIX password prompt, enter the same strong password that you just entered.


![image-title-here](/img/posts_Schematics/sshforthefirsttime.png){:class="img-responsive"}

* Don't forget the new password that you set.


You're now logged in! Where To Go From Here?:point_right:
[Software Installation apt-get and npm](/14.programsInstallationCategory.html).
