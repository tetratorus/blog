---
title: Setting up a blog with Hexo
subtitle: in less than 30 mins
readtime: 5 min read
date: 2016-08-09 20:11:07
tags:
---
Step 1:
Go to [Hexo.io](https://hexo.io/), install Hexo, and create a blog on your local machine.
<br>

Step 2:
Get a [Heroku account](https://id.heroku.com/login) and install the [Heroku toolbelt](https://toolbelt.heroku.com/).
<br>

Step 3:
Create a new Heroku app.
```
$ heroku create blog //take note of your repository URL
```
<br>

Step 4:
Follow the instructions for [deploying Hexo on Heroku](https://hexo.io/docs/deployment.html#Heroku).
<br>

Step 5:
Deploy.
```
$ hexo generate -d
```
<br>
