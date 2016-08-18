---
layout: default
title: Create a safe server user account
---

# Create a Safe Account to Run Your Code

<h3>Create a new user and disable root access</h3>

At the prompt on your server

  should look something like the following:
`root@dropletname:~#`,


enter adduser followed by the customUserName you want the new user to have.<br />
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`adduser customUserName`



adduser UserName
You'll be asked to create a password. What you type will not show up on screen, but type your password and hit enter. Then retype and hit enter again:

<pre>
<code>Enter new UNIX password:
 Retype new UNIX password:
</code></pre>


SAVE YOUR PASSWORD somewhere safe!

Once you've created and confirmed your new password, you'll be asked a few questions:

Changing the user information for customUserName

Enter the new value, or press `ENTER` for the default
<pre>
<code>Full Name []:
 Room Number []:
 Work Phone []:
 Home Phone []:
 Other []:
</code>
</pre>

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
Is the information correct?
`VirtualPrivateServer`$`[Y/n]`Y

* You can leave these blank if you don't need this info for your new user.

NB Remember some of your programs are already existing -Programs like Git, Nodejs and Npm.
You don't have to re-install these are already installed by root.
