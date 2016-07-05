---
layout: default
title: Create a safe server user account
---

# `1`.Create a Safe Account to Run Your Code

Create a new user and disable root access

At the prompt on your server (should look something like this
`root@dropletname:~#`,


enter adduser followed by the customUserName you want the new user to have.<br />
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`adduser customUserName`



adduser UserName
You'll be asked to create a password. What you type will not show up on screen, but type your password and hit enter. Then retype and hit enter again:


Enter new UNIX password:
Retype new UNIX password:
SAVE YOUR PASSWORD somewhere safe!

Once you've created and confirmed your new password, you'll be asked a few questions:

Changing the user information for customUserName

Enter the new value, or press ENTER for the default
    Full Name []:
    Room Number []:
    Work Phone []:
    Home Phone []:
    Other []:
Is the information correct? [Y/n] Y
You can leave these blank if you don't need this info for your new user.

NB Remember some of your programs are already existing -Programs like Git, Nodejs and Npm.
You dont have to re-install these are already installed by root.
