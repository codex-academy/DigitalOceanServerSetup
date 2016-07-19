---
layout : default
title : NginX Configuration
---

# NginX Configuration


Now that we added some rules for your firewall you will notice that you're no longer able to go to your sites by just typing your domain server address with port number attached. It's just loads but nothing comes to appear!

Is that an error ??? `NO`

<h3>Let us begin to configure nginx</h3>

We need to first change to a specific nginX folder that contains a default configuration file by typing the following:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`cd /etc/nginx/sites-available/`

If you can list all the files on that are inside the [sites-available] directory you should only see one file which is the file named:`default`

Do you see it ?

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
Got it

Then you can proceed and edit that file by typing:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo nano default`

There would be a bunch of commented out lines and as a suggestion, you need to cleanup that file and have a your default configuration setup similar to the following example:
<pre>
<code>server {
    listen 80;
    server_name example.projectcodex.co;
    location / {
        proxy_pass http://localhost:{portNumber};
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
     }
}
</code></pre>
You will need to replace `serverDomainName` with your own serverDomainName. Same applies for the `portNumber` it should be the port number defined from your app.js or index.js or server.js or whatever fileName.

Then you need to check whether the configuration you've just applied has been saved by executing the previous following command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`nano default`

<h3>output should be like the following~></h3>

![image-title-here](/img/posts_Schematics/nginxConfEx.png){:class="img-responsive"}

* Nothing else should be written on the default file.

Then if so Exit using `ctrl + x` key you will get confirmation message that asks you to save file with default as fileName and then press `y` to save the current changes you made, thereafter you'll be taken out from the terminal text editor.

Then you will have to restart nginX service by executing the following command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo service nginx restart`

![image-title-here](/img/posts_Schematics/nginXStatus.png){:class="img-responsive"}

If you got the same response to the above diagram you should know that your configuration file is on a good state :wink:
