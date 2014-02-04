---
layout: lab
title: Lab 9, Part 1 - Ice Cream
prefix: ../../
---
# Lab 9, Part 1 - Ice Cream

## Overview

Goals for this lab:

* Fork lab\_9\_part\_1
* Draw some ice cream!
* Move the drawing into a function
* Refactor your function to take variables, adjust your drawing accordingly
* (Optional) Make a lot of ice cream!

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

### Fork and Clone the FIRST Part of Lab 9

* go to github.com
* make sure you're still logged in
* open this url: https://github.com/MTEC1002/lab\_9\_part\_1
* click on fork
![fork](github-fork.png)
* wait for it...
* you should now have a repository url that you can copy __in your account__
* it should look something like: https://github.com/yourgithubusername/lab\_9\_part\_1.git
* open terminal
* make sure that you're in __~/Desktop/username__ 
* __clone__ this repository
* __cd__ into the lab\_9\_part\_1 directory
* use pwd to make sure you're in the right directory again - this time, it should be: __~/Desktop/username/_lab\_9\_part\_1__ 

### Makin' Some Ice Cream

![ice_cream](ice_cream.png)

* open processing and navigate to __~/Desktop/username/_lab\_9\_part\_1__ 
* open up the ice\_cream sketch
* draw an ice cream cone with two scoops
	* a triangle for the cone:   
		* the fill should be 200, 100, 50;
		* the triangle coordinages should be (250, 400), (290, 280), and (210, 280)
	* two ellipses for the scoop of strawberry
		* the fill should be 240, 160, 190
		* ellipse one should be at (250, 250) with diameter 100
		* ellipse two should be at (250, 290) with dimensions of 100 by 30    
	* two ellipses for the scoop of vanilla
		* the fill should be 255, 235, 160
		* ellipse one should be at (250, 180) with diameter 100
		* ellipse two should be at (250, 220) wiht dimensions of 100 by 30   
* run to see if your ice cream drawing works
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_1 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed

### Creating a Function

* create a function called __drawIceCream__
	* it should return nothing (void)
	* it should take no parameters
	* the signature should be something like: void drawIceCream()
	* remember to add opening and closing curly braces on new lines after your function definition: { and }
	* move your code from your draw function to your __drawIceCream__ function:
		* copy everything within the curly braces of your draw function...
		* paste it between the curly braces of your __drawIceCream__ function
	* in your draw function, _call_ your __drawIceCream__ function
* run to see if your ice cream function works
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_1 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed

### Adding Parameters to Your Function

* add x and y parameters to your __drawIceCream__ function
* change your call to the function so that it includes two parameters: 250 for x and 250 for y
* modify your drawing so that every x-coordinate and y-coordinate for your ellipse or triangle is relative to the new x and y parameters that are being passed in
	* go through every ellipse or triangle call and substitute in variables for hard-coded x and y coordinates
	* use subtraction and addition where appropriate
	* for example: ellipse(x, y, 120, 60);
	* another example: ellipse(x + 20, y + 20, 120, 60);
* run to see if your new ice cream function works
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_1 (if you're not, cd into it)
* use git to __add__ and __commit__
* now change the x and y values in your function call (maybe... 300 and 300); see that the drawing moved!
* __save__ it (apple-s)
* go back to terminal; make sure you're in ~/Desktop/username/lab\_9\_part\_1 (if you're not, cd into it)
* use git to __add__, __commit__, and __push__ to origin master
* check your repository to see that your changes were pushed

### (Optional) Ice Cream Wallpaper

![ice_cream_wallpaper](ice_cream_wallpaper.png)

* use nested for loops in your draw function to draw an ice cream wallpaper
* there's probably room for about 5 columns and 3 rows
* when you're done, save it, add, commit and push

