---
layout:default
title: Running your app
---

# Running your app on server

Connnect to your server : `username@dns`

* We would advice you to create your project folder on your home directory using the following command:
`mkdir projects && cd projects`

After changing to your projects folder you should clone your website git repo with the following command :
`git clone git@github.com:username/repo.git`

Then finally you will Install all your npm modules by running the next following command:
`sudo npm install -g && sudo npm install --save`

note that `-g` flag installs node_modules GLOBALLY and  `--save` installs node_modules folder and saves it locally on your machine or server;
 * You now need run :pm2 start index.js/app.js.
