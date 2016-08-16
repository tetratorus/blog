---
title: How to set up a blog using Hexo in 30 mins
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
$ heroku create blog //take note of the endpoint
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

Step 6: 
Write [a blog post](#) about how to set up a blog using Hexo.