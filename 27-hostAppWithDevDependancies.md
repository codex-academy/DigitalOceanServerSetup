---
layout : default
title : Deploy your application
---


<h3>Deploy your application</h3>

# Running your app on server

Connnect to your server :

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`username@serverDomainName`

We would advice you to create your project folder on your home directory using the following command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`mkdir projects && cd projects`


After changing to your /projects folder you should clone your website git repo with the following command :

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">`
git clone git@github.com:username/repo.git`


Then finally you will Install all your npm modules by running the next following command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo npm install -g && sudo npm install --save`


`NB` The `-g` flag installs `node_modules` GLOBALLY as a result YOU WILL NOT HAVE `node_modules` folder to Exist on your local project files. The`--save` flag installs `node_modules` folder and it saves it locally inside your project. At this stage you should be having your updated .gitignore file existing because of the (git pull) command that you've ran onto the terminal, no more package.json file modification. If you want to make other changes then it would mean this file should be last modified when you first ran npm install `node_module-name` from your local machine;

You now need run :

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`pm2 start index.js`

* you can replace the `index.js` file with` app.js` or `server.js` depending on the express server code that you implemented to your file.

<br/>

# What's next ? :thought_balloon: ...

Go to your browser and type your application url:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
url=`http://yourServerName:appsPORTNUMBER`

OR

If you are arleady on your local machine terminal you can just type do the following depending on the browser of your choice:
`google-chrome http://yourServerName:appsPORTNUMBER`

<h3>Same Applies for firefox</h3>
`firefox http://yourServerName:appsPORTNUMBER`

# Just one last Tip to update your application

<h3>software is always changing ...</h3>

* You need to update your app on your your local machine and push your changes to github   

* Connect to your server again and change to your project's directory then run git pull command:

`git pull`

<h3>Remeber!</h3>

* After pulling you have to restart your remote server pm2 program [`application-id`] using the following command:

`pm2 restart your application (process id)`

If you don't know the id of your app you will then type the following command :
`pm2 status`

(In this case we are having four deployed apps) so the following is going to be our Output ~>
![image-title-here](/img/posts_Schematics/pm2StatusApplicationId.png){:class="img-responsive"}

You will then follow this procedure again and again :repeat: ...

:clap: Then you're DONE!  :end:
