---
layout: lab
title:  Lab - Publish Your Code to Github
prefix: ../../
---
# Lab - Publish Your Code to Github

## Objectives

* creating a remote repository on github
* setting a remote repository for your project
	* git remote add
* pushing your changes to a remote repository
	* push

## Overview

1. create a repository on github
2. push your shapes repository to it

## Part 1 - Creating a Remote Repository on Github

* go to [github.com](github.com)
* create an account if you don't already have one
* create a new repository by clicking on the __new repository__ icon on the upper right hand corner
![create a new repository](lab_2_github_new_repo.png)
* fill in the information for your new repository
* the name of your repository should be lab_5_processing_shapes
* the rest of the form should be filled out accordingly:
![name new repository](lab_2_github_name_repo.png)

## Part 2 - Pushing Code to Github
* let's add github as a remote repository for your project; you'll need the url to start
* copy your repository's url from github:
![repo url](lab_2_github_repo_url.png)
* it should be something similar to:  https://github.com/foureyes/lab_5_processing_shapes.git
* now... in terminal...
* __make sure you're in your shapes directory__
* use the url you just copied with __git remode add__ to identify github as a remote repository (called __origin__):
{% highlight bash %}
git remote add origin https://github.com/foureyes/lab_5_processing_shapes.git
{% endhighlight %}
* finally, push your changes to gihub:
{% highlight bash %}
git push origin master
{% endhighlight %}
* verify that your changes are in github by refreshing your repository page
