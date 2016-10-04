---
layout : default
title : mySQL configuration
---


# mySQL configuration

You don't necessarily need to do this,unless you are having problems with the current mySql Program.

Why do we consider this configuration as not a must be done action ?

Because you are going to get same confirmations / prompts as you did the first time you were setting up this program. This will be a useful method of changing a root password.

If you have already got your database code on your script and you are using root as your database user then you've realized that your database password for the user:root configuration on your script.js is not the same as the one that you chose when you were setting up this program ,then this is a good place for your otherwise you should have a separate user for each specific database such that chances of you getting errors with your configuration on your script.js would be minimal.

In order to configure it, we would have to terminate mySql process by executing the following command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`VirtualPrivateServer`$`sudo service mysql stop`

Then to start with the configuration you will then need to know the current version.
To get current version type the following command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`VirtualPrivateServer`$`mysql --version` :white_check_mark:

 and it would not allow you to use the following method for version checking:
 `mysql -v`  :x:

Now that you know the current version, you can type next command to re-configure mySql:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`VirtualPrivateServer`$`sudo dpkg-reconfigure mysql-server-<yourCurrentVersion>`

Remember to type yourCurrentVersion without `< >` signs

Like this: `sudo dpkg-reconfigure mysql-server-5.5`

With that :sparkles: you're done. :stuck_out_tongue_winking_eye:
