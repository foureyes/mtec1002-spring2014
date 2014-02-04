---
layout: lab
title: Lab 9, Part 3 - Face
prefix: ../../
---
# Lab 9, Part 3 - Face (Again!)

## Overview

Goals for this lab:

* Fork lab\_9\_part\_3
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
* open this url: https://github.com/MTEC1002/lab\_9\_part\_3
* click on fork
![fork](github-fork.png)
* wait for it...
* you should now have a repository url that you can copy __in your account__
* it should look something like: https://github.com/yourgithubusername/lab\_9\_part\_3.git
* open terminal
* make sure that you're in __~/Desktop/username__ 
* __clone__ this repository
* __cd__ into the lab\_9\_part\_3 directory
* use pwd to make sure you're in the right directory again - this time, it should be: __~/Desktop/username/_lab\_9\_part\_3__ 

### Drawing a Face

![face](face.png)

* open processing and navigate to __~/Desktop/username/_lab\_9\_part\_3__ 
* open up the face sketch
* voila!  we're done

### Creating a Function

* create a function called __drawFace__
	* it should return nothing (void)
	* it should take no parameters
	* the signature should be something like: void drawFace()
	* remember to add opening and closing curly braces on new lines after your function definition: { and }
	* move your code from your draw function to your __drawFace__ function:
		* copy everything within the curly braces of your draw function...
		* paste it between the curly braces of your __drawFace__ function
	* in your draw function, _call_ your __drawFace__ function
* run to see if your fuce function works
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_3 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed

### Adding Parameters to Your Function

* add x and y parameters to your __drawFace__ function
* change your call to the function so that it includes two parameters: 250 for x and 250 for y
* modify your drawing so that every x-coordinate and y-coordinate for your ellipse is relative to the new x and y parameters that are being passed in
	* go through every ellipse call and substitute in variables for hard-coded x and y coordinates
	* use subtraction and addition where appropriate
	* for example: ellipse(x, y, 120, 60);
	* another example: ellipse(x + 20, y + 20, 120, 60);
* run to see if your new face function works
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_3 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed

### Adding Interactivity Using the Mouse

![face_mouse](face_mouse.png)

* add a function called __mouseClicked__ at the bottom of your code, outside of draw and drawFace
	* it should returning nothing (void)
	* it should take no parameters
	* the signature should be something like: void mouseClicked() 
	* remember to add opening and closing curly braces on new lines after your function definition: { and }
* move your call to drawFace from your draw function to your new __mouseClicked__ function
	* drawFace should be within the curly braces of __mouseClicked__
	* instead of using 250 and 250, use the following variables in your drawFace function call: __mouseX__, __mouseY__
* run your program
* click around the screen
* it should [look like this](face_mouse.mov)
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_3 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed

### Adding Interactivity Using the Keyboard

* create two variables above your draw function... 
	* they should be integers
	* call them x and y
	* set them both equal to 250
* move your call to drawFace back to your draw function
* instead of calling your drawFace function  with mouseX and mouseY, use the new __x__ and __y__ variables that you just created
* remove your function definition for mouseClicked 
* replace it with a function called keyPressed
	* it should take no parameters
	* the signature should be something like: void keyPressed() 
	* remember to add opening and closing curly braces on new lines after your function definition: { and }
	* in the body of your function use four if statements to determine what key was pressed
		* compare keyCode to UP, DOWN, LEFT, RIGHT
		* for example: if(keyCode == UP)
	* in each if statement either add or subtract 3 from either x or y
		* for example, pressing up will move the face up, so subtract 3
* run your program
* try pressing the arrow keys
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_3 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed
