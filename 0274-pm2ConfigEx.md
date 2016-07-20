---
layout : default
title : pm2 Configuration
---

# pm2 Configuration

Lets simplify our deployment update cycle by adding a new configuration file so Called ecosystem.json


We have to first generate this with the following command:
`pm2 ecosystem`

<h3>Output~></h3>
File /home/user-account/ecosystem.json generated


Then you have to be able to easily navigate to this file by using the following command:
`ls`

You then have to open it and see hows it done before modifications wiht the following command:
`sudo nano ecosystem.json`

# full pm2's ecosystem.json File configuration overview

<pre><code>{
  "apps" : [{
    "name"      : "[API]",
    "script"    : "[app].js",
    "env": {
      "COMMON_ENV_VAR": "true"
    }
    "env_production": {
      "NODE_ENV": "production",
    }
  },{
    "name"      : "[WEB]",
    "script"    : "[web].js"
  }],
  "deploy" : {
    "production" : {
      "user" : "node",
      "host" : "212.83.163.1",
      "repo" : "git@github.com:[repo].git",
      "ref"  : "origin/master",
      "path" : "/projects",
      "post-deploy" : "pm2 startOrRestart ecosystem.json --env production"
    },
    "dev" : {
      "user" : "node",
      "host" : "212.83.163.1",
      "repo" : "git@github.com:repo.git",
      "ref"  : "origin/master",
      "path" : "/projects",
      "post-deploy" : "pm2 startOrRestart ecosystem.json --env production"
    }
  }
}</code></pre>

# Let's start with the "apps" object Below.

<pre><code>
"apps" : [{
  "name"      : "[API]",
  "script"    : "[app].js",
  "env": {
    "COMMON_ENV_VAR": "true"
  }
  "env_production": {
    "NODE_ENV": "production",
  }
},{
  "name"      : "[WEB]",
  "script"    : "[web].js"
}],
</code></pre>

Then on "apps":- you will need replace `"name" key`:`value[API]` with your custom application name instead of [API] and replace `"script" key`:`value[app]` with your proper script name instead of [app]. If you can notice the example above on that "apps" object we are having two different apps then its going to be the same procedure if you are going to deploy two apps.

# Now its time for use to get all our changes automatically from git by modifying the "deploy"'part which contains two objects.

<pre><code>
"deploy" : {
  "production" : {
    "user" : "node",
    "host" : "212.83.163.1",
    "repo" : "git@github.com:[repo].git",
    "ref"  : "origin/master",
    "path" : "/projects",
    "post-deploy" : "pm2 startOrRestart ecosystem.json --env production"
  },
  "dev" : {
    "user" : "node",
    "host" : "212.83.163.1",
    "repo" : "git@github.com:repo.git",
    "ref"  : "origin/master",
    "path" : "/projects",
    "post-deploy" : "pm2 startOrRestart ecosystem.json --env production"
  }
}
</code></pre>
