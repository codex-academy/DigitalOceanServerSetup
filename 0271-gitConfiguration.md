---
layout : default
title : Git Configuration
---

# Git Configuration

You can specify your git configuration setup with the git config command in order for git to recognize you commits:

You need to start off by typing the following reset command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`git config --global --unset-all user.name`

![image-title-here](/img/posts_Schematics/gitHubConfigEx.png){:class="img-responsive"}

Then you can setup your username by typing the following Git Config command:

*You should replace yourGithubUserName with your real githubUsername that you use to log in to you github Account*

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`git config --global --add user.name "yourGithubUserName"`


<h3>You can now setup your link your github account with your email account</h3>
To know your email you can simply go to github press the `1.`:arrow_down_small:`arrow` next to your github avatar. Go to `2.`settings then you should see `3.`email on Personal Settings menu, then `4.`That's your mail indicated as primary and Public.

<h3>Setting it globally onto your server terminal you will then follow the next few steps below:</h3>

You need to start off by typing the following reset command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`git config --global --unset-all user.mail`

Then you can setup your email by typing the next Git Config command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`git config --global --add user.mail "yourEmail"`
