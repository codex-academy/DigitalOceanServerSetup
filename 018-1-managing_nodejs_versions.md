---
layout : default
title : use npm n package to easily manage your nodejs versions
---

# Use npm n package to easily manage your nodejs versions

<h3>Install n</h3>

you can do that by typing the following command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo npm install -g n`


# How to easily manage your nodejs versions with the use n ?

<h3>Okay lets first check if you are having n installed by typing the following command:</h3>
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`n --version`

<strong>Output ~></strong>
<pre><code>2.1.0</code>

or a greater version</pre>
WORKS !!!

In case your application requires you to have a greater version of nodejs installed, then you can choose nodejs version based on the list of various versions that are available.

* You then ask yourself:"How would I know all existing `node versions`?"

<h3>An answer to that, you just have to type the following command:</h3>

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`n list`

<h3>Now install a specific node version</h3>

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo n <versionToBeIntalled>`

<h3>Then check your current node version:</h3>

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`node -v`

<strong>Output ~></strong>
It Should exactly be the node version that you've just installed. :smiley:

with that you've successfully managed to install a custom node version. :ok_hand:
