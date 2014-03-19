---
layout: lab
title: Lab 7, Part 4 - Animated Car
prefix: ../../
---
# Lab 7, Part 4 - Animated Car

## Overview

* Make the car move horizontally
* Increment or decrement a variable in the draw function to make the car move along the x-axis

## Instructions

### Cleaning Up
* close processing
* close terminal

### Reusing Your Code

* open up terminal and change to your __~/Desktop/username/lab\_7\_part\_2__ folder
* use pwd to verify that you're in the correct folder
	* you should be in __~/Desktop/username/lab\_7\_part\_2__
	* if you're not, cd into it
* open up your car sketch with __processing__; it should be in... __~/Desktop/username/lab\_7\_part\_2/car__  
* (it may just directly be car.pde)

### Modify Your Sketch

* __we're going to move along the x axis (horizontally)__
* move the call to background from the setup function to the very first line inside your draw function
* create a integer variable called speed, and set it equal to 1; place this after your declaration of the x variable (__outside__ of both the setup and draw methods)
* at the end of your draw method, subtract speed from the x variable to make the car move!

### Saving Your Work as You Go

* as you work, save your file in processing
* additionally, save your work using version control by using the following git commands: status, add, and commit
* some things to remember:
	* __add__ either takes a specific file name or --all
	* for __commit__, don't forget the -m "your commit message" part
		* if you find yourself in an area where you can't type in commands, __CTRL-C__
		* if it looks like you're in a text editor with a bunch of ~'s, type in the following sequence one-by-one
			* &lt;ESC&gt;
			* :q!
			* &lt;ENTER&gt;
	* again, make sure you've __added__ and __committed__ everything
	* if you run git status, you should have nothing to commit:
{% highlight bash %}
git status

# On branch master
nothing to commit (working directory clean)
{% endhighlight %}


### Pushing to a Remote Repository
* when you're done with your sketch, and everything is committed, submit your assignment by pushing to github
* since you already added a remote repository, all you have to do is push your remote repository
{% highlight bash %}
git push origin master
{% endhighlight %}
* verify that your changes are in github by refreshing your repository page

<!-- close_-->
