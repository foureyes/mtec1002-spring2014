---
layout: lab
title: Lab 9, Part 4 - Duck!
prefix: ../../
---
# Lab 9, Part 4 - Duck!

## Overview

Goals for this lab:

* Fork lab\_9\_part\_4
* Draw a face!
* Move your drawing into a function that draws a face 
* Refactor your function to take variables, adjust your drawing accordingly
* Use mouseClicked, mouseX and mouseY to add mouse interactivity
* Use keyPressed, keyCode, UP, DOWN, LEFT, RIGHT to add keyboard interactivity

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

### Fork and Clone the THIRD Part of Lab 9

* go to github.com
* make sure you're still logged in
* open this url: https://github.com/MTEC1002/lab\_9\_part\_4
* click on fork
![fork](github-fork.png)
* wait for it...
* you should now have a repository url that you can copy __in your account__
* it should look something like: https://github.com/yourgithubusername/lab\_9\_part\_4.git
* open terminal
* make sure that you're in __~/Desktop/username__ 
* __clone__ this repository
* __cd__ into the lab\_9\_part\_4 directory
* use pwd to make sure you're in the right directory again - this time, it should be: __~/Desktop/username/_lab\_9\_part\_4__ 

### Drawing a Duck (Quack!)

![duck](duck.png)

* open processing and navigate to __~/Desktop/username/_lab\_9\_part\_4__ 
* open up the duck sketch
* use two ellipses to draw the duck's body and head
* use a triangle to draw the duck's beak
* you can just put in the actual integer values (numbers) for drawing shapes

### Creating a Function

* create a function called __drawDuck__
	* it should return nothing (void)
	* it should take no parameters
	* the signature should be something like: void drawDuck()
	* remember to add opening and closing curly braces on new lines after your function definition: { and }
	* move your code from your draw function to your __drawDuck__ function:
		* copy everything within the curly braces of your draw function...
		* paste it between the curly braces of your __drawDuck__ function
	* in your draw function, _call_ your __drawDuck__ function
* run to see if your duck function works
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_4 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed

### Adding Parameters to Your Function

* add one parameter, an integer named x, to your __drawDuck__ function
* change your call to the function so that it includes one parameter: 250 for x
* modify your drawing so that every x-coordinate for your ellipse or triangle is relative to the new x parameter that's being passed in
	* go through every ellipse or triangle call and substitute in variables for x values
	* use subtraction and addition where appropriate
	* for example: ellipse(x, 250, 120, 60);
	* another example: ellipse(x + 20, 250, 120, 60);
* run to see if your new face function works
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_4 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed


### Adding Interactivity Using the Keyboard

* create one variable above your draw function... 
	* it should be an integer
	* call it x
	* set it equal to 250
* create a function called keyPressed at the end of your program (after the last curly brace for draw)
	* it should take no parameters
	* the signature should be something like: void keyPressed() 
	* remember to add opening and closing curly braces on new lines after your function definition: { and }
	* in the body of your function use two if statements to determine what key was pressed
		* compare keyCode to LEFT and RIGHT
		* for example: if(keyCode == LEFT)
	* in each if statement either add or subtract 3 from x 
		* for example, pressing left will move the duck left, so subtract 3
* run your program
* try pressing the arrow keys
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_4 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed
