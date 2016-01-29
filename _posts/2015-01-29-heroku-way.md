---
layout: post
title: The Heroku Way
---

Going the Heroku way for developers is a very easy and simple process to adopt. It is the right approach to take if you are building applications and do not want to be tied to a platform/infrastructure specific services/hooks. Heroku in its [architecting apps for Heroku](https://devcenter.heroku.com/articles/architecting-apps) article lays out these points. One point that stands out for me is that __"it is application, not infastructure, focused"__.

Now, if you want to go the _Heroku way_, I hope that this article would give you some information to get you started or provide you guidance.


### Prerequisites 

- Linux or Mac OS X based computer 
  - _(Windows based computer would do but i suggest you go [cygwin](https://www.cygwin.com/) route with the Windows)_
- Familiarity with command line tools

### Getting Started

- [Signup](https://signup.heroku.com/dc) on Heroku for a Developer account 
- Follow Heroku's Getting Started guides
- Learn to use Heroku from the Command Line
- Setup CLI Authentication 

#### What is Heroku's Command Line (CLI)?

  _from Heroku [website](https://devcenter.heroku.com/categories/command-line):_

> The heroku command-line tool is an interface to the Heroku Platform API and includes support for things like creating/renaming apps, running one-off dynos, taking backups, configuring add-ons and managing your app’s state. It’s generally installed in your local dev environment as part of the Heroku Toolbelt.

### CLI authentication

You may do CLI authentication with email and password. Instead, use API token and SSH Keys to get to your Heroku account. This [CLI authentication](https://devcenter.heroku.com/articles/authentication) article for more information.

__with the API Token__

  - On my local, the ~/.netrc looks like this:

![~/.netrc contents]({{site.baseurl}}/assets/img/heroku-netrc.jpg)

### Heroku Version
Typing the command `heroku version` gives the version information for the heroku [toolbelt](https://toolbelt.heroku.com), [cli](https://devcenter.heroku.com/articles/heroku-command) and all the installed [plugins](https://devcenter.heroku.com/articles/using-cli-plugins).


	AK-Mac:flask-app ak$ heroku version
	heroku-toolbelt/3.42.33 (x86_64-darwin10.8.0) ruby/1.9.3
	heroku-cli/4.27.16-cb94b94 (amd64-darwin) go1.5.3
	=== Installed Plugins
	heroku-apps@1.2.3
	heroku-cli-addons@0.2.0
	heroku-fork@4.1.0
	heroku-git@2.4.5
	heroku-local@4.1.6
	heroku-run@2.9.2
	heroku-spaces@2.0.11
	heroku-status@2.1.0



### Create a New App from the CLI

With the Heroku's CLI, you can create a new app with just one command

	(flask-bs-app)AK-Mac:flask-app ak$ heroku create --stack cedar
	Creating sheltered-garden-45928... done, stack is cedar-14
	https://sheltered-garden-45928.herokuapp.com/ | https://git.heroku.com/sheltered-garden-45928.git


Also, you get a git remote on Heroku for your application. With this git repo you can [track your app](https://devcenter.heroku.com/articles/git#tracking-your-app-in-git) with/in git. 

### Screenshots

**New applicaiton on Heroku Dashboard**

![My Dashboard]({{site.baseurl}}/assets/img/heroku-dashboard.png)

**New Application in the Browser**

![New Heroku App]({{site.baseurl}}/assets/img/heroku-new-app.png)


