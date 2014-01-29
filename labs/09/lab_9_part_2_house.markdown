---
layout: lab
title: Lab 9, Part 2 - House
prefix: ../../
---
# Lab 9, Part 2 - House

## Overview

Goals for this lab:

* Fork lab\_9\_part\_2
* Draw a house!
* Move your drawing into a function that draws a house
* Refactor your function to take variables, adjust your drawing accordingly
* (Optional) Make a tiny town

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

### Fork and Clone the SECOND Part of Lab 9

* go to github.com
* make sure you're still logged in
* open this url: https://github.com/MTEC1002/lab\_9\_part\_2
* click on fork
![fork](github-fork.png)
* wait for it...
* you should now have a repository url that you can copy __in your account__
* it should look something like: https://github.com/yourgithubusername/lab\_9\_part\_2.git
* open terminal
* make sure that you're in __~/Desktop/username__ 
* __clone__ this repository
* __cd__ into the lab\_9\_part\_2 directory
* use pwd to make sure you're in the right directory again - this time, it should be: __~/Desktop/username/_lab\_9\_part\_2__ 

### Buildin' a House

![house](house.png)

* open processing and navigate to __~/Desktop/username/_lab\_9\_part\_2__ 
* open up the house sketch
* draw a house using three rectangles (house, window and door) and a triangle...
	* here are some recommended dimensions (__you can use your own, though!__):
		* house at (200, 200) with dimensions of 100 by 100
		* roof at (190, 200), (250, 125), and (310, 200)
		* window at (250, 210) with dimensions of 40 by 40
		* door at (210, 230) with dimensions of 35 by 70
* run to see if your house drawing works
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_2 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed

### Creating a Function

* create a function called __drawHouse__
	* it should return nothing (void)
	* it should take no parameters
	* the signature should be something like: void drawHouse()
	* remember to add opening and closing curly braces on new lines after your function definition: { and }
	* move your code from your draw function to your __drawHouse__ function:
		* copy everything within the curly braces of your draw function...
		* paste it between the curly braces of your __drawHouse__ function
	* in your draw function, _call_ your __drawHouse__ function
* run to see if your house function works
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_2 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed

### Adding Parameters to Your Function

* add x and y parameters to your __drawHouse__ function
* change your call to the function so that it includes two parameters: 200 for x and 200 for y
* modify your drawing so that every x-coordinate and y-coordinate for your rect or triangle is relative to the new x and y parameters that are being passed in
	* go through every rect or triangle call and substitute in variables for hard-coded x and y coordinates
	* use subtraction and addition where appropriate
	* for example: rect(x, y, 120, 60);
	* another example: rect(x + 20, y + 20, 120, 60);
* run to see if your new house function works
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_2 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed

### (Optional) Tiny Town 

![house_random](house_random.png)

* use the random function to generate x and y coordinates 
* use these coordinates as arguments to your __drawHouse__ function that you call in draw() 
* don't draw a background
* it should [look like this](house_random.mov) when you're done. 


