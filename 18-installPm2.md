---
layout : default
title : Install pm2
---
# Install pm2

# Use NPM To Install A Package Called PM2.

Reminder. (NPM stands for - Node Package Manager ) and there are times when you will find deceiving meanings whereby people would say the NPM abbreviation stands for  (“No Problem Man”) .

NPM is a package manager that you will use to install frameworks and libraries to use with your Node.js applications. NPM was installed with Node.js. PM2 is a sweet little tool that is going to solve two problems for you:
It is going to keep your site up by restarting the application if it crashes. These crashes should NOT happen, but it is good know that PM2 has your back. (Some people may be aware of Forever.js, another tool that is used to keep node based sites running - I think you will find that PM2 has a lot to offer.)
It is going to help you by restarting your node application as a service every time you restart the server. Some of use know of other ways to do this, but pm2 makes it easier, and it has some added flexibility.
Install PM2 by typing the following at the command line:<br />

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo npm install pm2 -g`
