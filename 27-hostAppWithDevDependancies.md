---
layout : default
title : Deploy your application
---


<h3>Deploy your application</h3>

# Running your app on server

Connnect to your server :

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`username@dns`

We would advice you to create your project folder on your home directory using the following command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`mkdir projects && cd projects`


After changing to your projects folder you should clone your website git repo with the following command :

~/projects $<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">`git clone git@github.com:username/repo.git`


Then finally you will Install all your npm modules by running the next following command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo npm install -g && sudo npm install --save`


`NB` The `-g` flag installs `node_modules` GLOBALLY as a result YOU WILL NOT HAVE `node_modules` folder to Exist in your local project files. The`--save` flag installs `node_modules` folder and it saves it locally inside your project. At this stage you should be having your updated .gitignore file existing because of the (git pull) command that you've ran onto the terminal, no more package.json file modifications should be made thus means this file should be last modified when you first ran npm install `node_module-name` from your personal machine;

You now need run :

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`pm2 start index.js || app.js || server.js`

<br/>

# What's next ? :thought_balloon: ...

Go to your browser and type your application url:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
url=`http://yourDNS:appsPORTNUMBER`

Then you're DONE!  :end:
