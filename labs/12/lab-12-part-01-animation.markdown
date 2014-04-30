---
layout: lab
title: Click
prefix: ../../
---
# Lab 12 - Part 1 - Animation

1. circle-animate
2. circle-boundary
3. circle-boundary-all
4. \*circle-bounce
5. \*circle-bounce-2
6. \*circle-bounce-3

## Instructions

Note that __ALL OF THESE FILES MUST BE SAVED IN THE LOCAL REPOSITORY THAT YOU CREATED FOR THIS LAB__.

### rectangles

Write a program that draws a circle that moves horizontally from left to right

* using SublimeText, create a new file called __circle-animate.html__ in your repository directory: __~/Desktop/jversoza/lab-12-game/__
* setup an html file
* add a style tag in insides the head tag - add the following code to give your canvas element a border:

{% highlight html %}
<style>
#sketch {
	border:1px solid #000;
}
</style>
{% endhighlight %}

* create a canvas element that is 480 by 720
* add script tags
* add a listener to your document to handle onload events... set it to run your main function: document.addEventListener('DOMContentLoaded', main);
* declare the following variables: 
	* sketch - your canvas element
	* context - your drawing instrument
	* circle - an object that contains your circles x, y position and radius
	* dx (set this equal to 2) - the velocity
	* fps (set this equal to 10) - the delay in ms before your animate function is called
	* animation - a variable to keep track of your animation
* create a main function
* start writing your program in your main function
* get your sketch element: sketch = document.getElementById('sketch');	
* create your context: context = sketch.getContext("2d"); 
* create your circle object: circle = {'x':25, 'y':sketch.offsetHeight / 2, 'r':25};
* define a function to be called repeatedly at a specific interval: animation = setInterval(animate, fps);
* note that the animate function will be defined immediately after... outside of the main function
* your main function is finished!
* create another function, outside of main, called animate (this will be called repeatedly, and it will be responsible for clearing the screen and drawing your shapes)


* in the anonymous function, use event.x and event.y to draw a rectangle
* use git status, add, commit, and push to save your file in version control and submit it
* send it to github by using git push
* example image below

![rectangles](../../resources/img/lab-11-rectangle-click.png)


### car

Write a program that draws a car wherever you click.  It will clear the screen on each click so that there is only one car on the canvas.

* using SublimeText, create a new file called __car-click.html__ in your repository directory: __~/Desktop/jversoza/lab-12-game/__
* setup an html file
* create a canvas element of at least 800 by 600
* add script tags
* add a listener to your document to handle onload events... set it to run your main function: document.addEventListener('DOMContentLoaded', main);
* declare two variables - sketch and context
* create a main function
* start writing your program in your main function
* get your sketch element: sketch = document.getElementById('sketch');	
* create your context: context = sketch.getContext("2d"); 
* create a listener for click events: sketch.addEventListener ...
* create an anonymous function (do this as an argument to addEventListener)
* in the anonymous function, use event.x and event.y to draw a car
	* clear the canvas (see slides)
	* this will use a function you define later (called draw_car)
* copy in the draw_circle function from the slides
* create a new function called draw_car... that utilizes the draw_circle function
	* it should have two parameters, x and y
	* draw all of your shapes relative to these values... for example: 
		* context.fillRect(x, y, 120, 40);
		* context.fillRect(x + somevalue, y - anothervalue, 80, 30);
		* draw_circle(x + somevalue, y + anothervalue, 20)
			* (fill in somevalue and anothervalue with numbers)
* draw_car will be used in the anonymous function in event handler...
* use git status, add, commit, and push to save your file in version control and submit it
* send it to github by using git push
* example image below
	
![car](../../resources/img/lab-11-car-click.png)

### \*faces

Write a program that draws a face wherever you click.

* using SublimeText, create a new file called __faces-click.html__ in your repository directory: __~/Desktop/jversoza/lab-12-game/__
* setup an html file
* create a canvas element of at least 800 by 600
* use the code in the previous labs to set up a click interaction
* bring in your draw_circle function 
* create a function to draw a face... and parameterize it appropriately
* the program should draw a face wherever the mouse is clicked
* use git status, add, commit, and push to save your file in version control and submit it
* example image below

![faces](../../resources/img/lab-11-face-click.png)

