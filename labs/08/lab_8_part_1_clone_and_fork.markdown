---
layout: lab
title: Lab 8, Part 1 - Clone and Fork
prefix: ../../
---
# Lab 8, Part 1 - Clone and Fork

## Overview

Goals for this lab:

* Create a local repository by copying one of your remote repositories on github (__clone__)
	* Clone
	* Make changes to code
	* Save your changes locally and push to your remote repository
* Copy another person's repository on github to work on your own version of the code (__fork__)
	* Fork
	* Clone
	* Make changes to code
	* Save your changes locally and push to your remote repository

## Instructions

### Cleaning Up
* close processing
* close terminal

### Prep Work

* if it's not already created, make a directory on your desktop with your first initial and last name
	* it should be __~/Desktop/username/__
	* do this using terminal
* in terminal change to your __~/Desktop/username/__ folder
* use pwd to verify that you're in the correct folder
	* you should be in __~/Desktop/username/__
	* if you're not, cd into it

### Cloning an Existing Repository 

We're going to copy one of your remote repositories (on github) to your local workstation.

* go to github.com
* login (if you're not already logged in)
* click on your user name on the upper right corner
![name](github-name.png)
* click on the repositories tab
![name](github-repositories.png)
* click on the repository named lab\_7\_part\_2
* (if that repository doesn't exist, use any repository that's available... maybe snowman or face\_var)
* copy the url (it should be something like https://github.com/MTEC1002/lab\_7\_part\_1.git)
* note that the image below says has name specific to my url... your url should be the same as your repository name
![name](github-url.png)
* go back to terminal
* check that you're in ~/Desktop/username/
* clone your repository
{% highlight bash %}
git clone https://github.com/MTEC1002/lab_7_part_1.git
{% endhighlight %}
* in terminal, cd into this new directory

<!-- _end bold -->

### Modifying your Repository

We'll modify your cloned copy and push the changes back.

* open processing
* in processing, go to file&rarr;open (it should be on the upper left corner)
* navigate to the repository that you just cloned
* it should be something like /Users/joe/Desktop/lab_7_part_1/some_file.pde
* open that file
* change the background
* save your file (apple-s or file&rarr;save)
* go back to terminal
* cd into your repository if you're not already in it (it should be the same name as the repository that you cloned... for example,  lab\_7\_part\_1) 
	* make sure that you're in ~/Desktop/username/lab\_7\_part\_1 
	* (just use pwd)
* use git to __add__, __commit__ (don't forget the message)
* since you cloned, your repository is already aware of your remote repository...
* so, all you have to do is push (don't forget origin master)
* check that your code is on github by refreshing the page

### Forking a Repository, Cloning It

Now we'll copy another user's repository to our github account so that we can modify existing code!

* go to github.com
* make sure you're still logged in
* open this url: https://github.com/MTEC1002/lab\_8\_part\_1
* click on fork
![fork](github-fork.png)
* wait for it...
* you should now have a repository url that you can copy
* it should look something like: https://github.com/jversoza/lab\_8\_part\_1.git
* open terminal
* make sure that you're in __~/Desktop/username__ 
* you're probably one folder in so... you might need to __cd ..__
* clone this repository
* cd into the directory that you just cloned

### Make Some Changes

* add another car
	* create another variable (maybe car_2_x)
	* use that to draw the second car
* animate one of the cars
	* add a speed variable
	* increment the x value of one of the cars in the draw loop
* (btw, how would you make the car go up and down)
* add, commit and push

