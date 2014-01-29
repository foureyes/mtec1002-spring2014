---
layout: lab
title: Lab 8, Part 3 - More Animation
prefix: ../../
---
# Lab 8, Part 3 - More Animation

## Overview

Goals for this lab:

* We'll use if statements to create a parallax background
* We'll start with a drawing of a car
* Instead of animating the car itself...
* We'll animate the background to create the effect of motion


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

Fork and clone the __third__ part of lab 8

* go to github.com
* make sure you're still logged in
* open this url: https://github.com/MTEC1002/lab\_8\_part\_3
* click on fork
![fork](github-fork.png)
* wait for it...
* you should now have a repository url that you can copy
* it should look something like: https://github.com/jversoza/lab\_8\_part\_3.git
* open terminal
* make sure that you're in __~/Desktop/username__ 
* __clone__ this repository
* __cd__ into the lab\_8\_part\_3 directory
* use pwd to make sure you're in the right directory again - this time, it should be: __~/Desktop/username/_lab\_8\_part\_3__ 

### Parallax Background

* create a moving [mountain background (see the movie)](car_animation_mountain.mov)
* draw a gray mountain in the background
	* to create a variable that will hold its x coordinate outside of the draw loop (call it something like __mountain\_x__)
	* use the [triangle](http://processing.org/reference/triangle_.html) function to draw a gray mountain in the background
		* make sure to use the variable above for its x coordinates (there are 3)!
	* __save__ it (apple-s)
	* go back to terminal; make sure you're in ~/Desktop/username/lab\_8\_part\_3 (if you're not, cd into it)
	* use git to __add__, __commit__, and __push__ to origin master
	* check your repository to see that your changes were pushed
* animate the gray mountain so that it moves from right to left
	* create a variable for the mountain's speed (name it __mountain\_speed__)
	* at the end of your draw loop, increment the mountain's x value using speed
		* something like: mountain_x += mountain_speed
	* __save__ it (apple-s)
	* go back to terminal; make sure you're in ~/Desktop/username/lab\_8\_part\_3 (if you're not, cd into it)
	* use git to __add__, __commit__, and __push__ to origin master
	* check your repository to see that your changes were pushed
* animate the gray mountain so that when it gets to the left hand side of the screen, it goes back to the right hand of the screen
	* use an if statement to change the x location of the mountain when it goes off screen
	* at the end of your draw loop, increment the mountain's x value using speed
		* something like: mountain_x += mountain_speed
	* __save__ it (apple-s)
	* go back to terminal; make sure you're in ~/Desktop/username/lab\_8\_part\_3 (if you're not, cd into it)
	* use git to __add__, __commit__, and __push__ to origin master
	* check your repository to see that your changes were pushed
* create a [tree background (see the movie)](car_animation_mountain_tree.mov)
* first draw a tree
	* use a green triangle and a brown rectangle to draw a tree
	* do this by creating a variable for the x coordinate of the tree
	* ...and drawing the shapes relative to that variable
	* __save__ it (apple-s)
	* go back to terminal; make sure you're in ~/Desktop/username/lab\_8\_part\_3 (if you're not, cd into it)
	* use git to __add__, __commit__, and __push__ to origin master
	* check your repository to see that your changes were pushed
* animate the tree so that it behaves like the mountain: right to left, and go back to right when off screen
	* follow the similar directions for mountain to create this animation
	* __save__ it (apple-s)
	* go back to terminal; make sure you're in ~/Desktop/username/lab\_8\_part\_3 (if you're not, cd into it)
	* use git to __add__, __commit__, and __push__ to origin master
	* check your repository to see that your changes were pushed
* (optional) use a for-loop to create [a stripe on the road](car_animation_stripe_move.mov)
* (optional) create two trees... when the tree goes off screen on the left, place it at a random location on the right off screen
