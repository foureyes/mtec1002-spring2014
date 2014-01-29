---
layout: lab
title: Lab 8, Part 2 - Conditionals
prefix: ../../
---
# Lab 8, Part 2 - Conditionals

## Overview

Goals for this lab:

* Fork lab\_8\_part\_2, a drawing of yellow car
* Animate the car
* Make the car _loop_ back to the other side of the screen when it goes off screen
* Make the car turn around when it hits either end of the screen 

## Instructions

### Cleaning Up
* close processing
* close terminal

### Prep Work

Make sure your folder is set up

* if it's not already created, make a directory on your desktop with your first initial and last name
	* it should be __~/Desktop/username/__
	* do this using terminal
* in terminal change to your __~/Desktop/username/__ folder
* use pwd to verify that you're in the correct folder
	* you should be in __~/Desktop/username/__
	* if you're not, cd into it

Fork and clone the __second__ part of lab 8

* go to github.com
* make sure you're still logged in
* open this url: https://github.com/MTEC1002/lab\_8\_part\_2
* click on fork
![fork](github-fork.png)
* wait for it...
* you should now have a repository url that you can copy
* it should look something like: https://github.com/jversoza/lab\_8\_part\_2.git
* open terminal
* make sure that you're in __~/Desktop/username__ 
* __clone__ this repository
* __cd__ into the lab\_8\_part\_2 directory
* use pwd to make sure you're in the right directory again - this time, it should be: __~/Desktop/username/_lab\_8\_part\_2__ 

### Animation

* open processing and navigate to __~/Desktop/username/_lab\_8\_part\_2__ 
* open up the car sketch
* animate the car
	* there is already a variable that holds the x value of the car
	* create another variable called speed; that will hold how fast your car moves
	* at the end of your draw function (but inside it)... add speed to x
	* run your program
	* __save__ it (apple-s)
	* go back to terminal; make sure you're in ~/Desktop/username/lab\_8\_part\_2 (if you're not, cd into it)
	* use git to __add__, __commit__, and __push__ to origin master
	* check your repository to see that your changes were pushed
* make the car start at the other side of the screen when it goes off screen
	* see this video for an exampe: [car animation - loop around](car_animation_pass.mov)
	* use an if statement to check if the x value of your car is outside of the screen dimensions
	* if it is, reset the value of that variable so that it is now on the other side of the screen
	* __save__ it (apple-s)
	* go back to terminal; make sure you're in ~/Desktop/username/lab\_8\_part\_2 (if you're not, cd into it)
	* use git to __add__, __commit__, and __push__ to origin master
	* check your repository to see that your changes were pushed
* make the car turn around if gets to the edge of the screen
	* see this video for an exampe: [car animation - turn around](car_animation_turn.mov)
	* use an if statement to check if the x value of your car is at the edge of the screen
	* if it is, change your speed variable so that it's going the other way (one way to do this is to multiply by -1)
	* you should check both sides!
	* go back to terminal; make sure you're in ~/Desktop/username/lab\_8\_part\_2 (if you're not, cd into it)
	* use git to __add__, __commit__, and __push__ to origin master
	* check your repository to see that your changes were pushed
* (optional) can you make the car move up and down instead of left and right?  how would you do that?
	* if you try this, save your work, add and commit...
	* use your commit message to say that you did the optional work
