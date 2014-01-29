---
layout: lab
title: Lab 7, Part 2 - Car
prefix: ../../
---
# Lab 7, Part 2 - Car

## Overview

* You're creating a car!  Nice!
* You'll have to use variable(s).
* The x location of the car must be calculated relative to these variable(s).
* Note that we're only varying the x-coordinate

## Instructions

### Cleaning Up
* close terminal
* close processing

### Set up Your Local Repository
* using the commandline, create a folder called __lab\_7\_part\_2__ in your ~/Desktop/username folder
* change to your __~/Desktop/username/lab\_7\_part\_2__ folder
* use pwd to verify that you're in the correct folder
	* you should be in __~/Desktop/username/lab\_7\_part\_2__
	* if you're not, cd into it
* once you're in the correct folder, create your repository!

{% highlight bash %}
git init
{% endhighlight %}

* now... configure your user name and email for your commits (these do not have to be the same as your github account)

{% highlight bash %}
# in the directory of your repository
git config user.name  "foo bar baz"
git config user.email foo@bar.baz
{% endhighlight %}

### Create Your Sketch
* create a new sketch in processing
* __immediately__ name your sketch by saving it as __car__ in your __~/Desktop/username/lab\_7\_part\_2__ folder
* put in your setup and draw methods
* __save your sketch again!__
* go back to terminal; make sure you're in __~/Desktop/username/lab\_7\_part\_2__
* in terminal, check the status of your repository - you should have a folder or file name called __car__ that's not yet _staged_
{% highlight bash %}
git status
{% endhighlight %}
* it should show that you have untracked files
{% highlight bash %}
# On branch master
#
# Initial commit
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#	car/
{% endhighlight %}
* again, you may have car.pde instead of the folder car; that's fine...
* using git, save a revision of your empty sketch to your local repository that you created above by...
* adding your changes so that they'll be committed
{% highlight bash %}
git add --all
{% endhighlight %}
* and then... actually commit your work
{% highlight bash %}
git commit -m 'an empty sketch for creating a car'
{% endhighlight %}

### Drawing Your Car

* you will be creating the following sketch:
![car](car.png)
* you should already have a [setup](http://processing.org/reference/setup_.html) and [draw](http://processing.org/reference/draw_.html) function; if you don't... add them
* in your setup function (between the curly braces) set the dimensions of your window by using the [size](http://processing.org/reference/size_.html) function - it should be 500 x 500
* after your setup function, but before your draw function (outside of both...) create a variable called _x_ that will hold an integer value
* assign the value 200 to it
* within your draw function, begin drawing your car...
* set the [fill](http://processing.org/reference/fill_.html) to the color that you want your car to be
* draw the first rectangle, the body of the car, using the [rect](http://www.processing.org/reference/rect_.html) function
	* the first argument should be the variable you created
	* you can use the following values for the y-coordinate, width, and height if you like:
		* y-coordinate: 300
		* width: 80
		* height: 20
* draw the second rectangle, the top of the car, using the [rect](http://www.processing.org/reference/rect_.html) function
	* this time, the x value should have some value added or subtracted to it so that the top part of the car sits centered above the body, or bottom, part of the car
	* you can use the following values for the y-coordinate, width, and height if you like:
		* y-coordinate: 285
		* width: 60
		* height: 15
* change the fill color to black 
* draw wheels!  use the [ellipse](http://www.processing.org/reference/ellipse_.html) function to do this:
	* the x-coordinates of your wheels should be based on your __x variable__
	* however, you'll need to add or subtract some amount to place it correctly
	* you can use the following y-coordinate, width and height for __both__ wheels if you've been using the provided values above (though... feel free to experiment and user your own values!)
		* y-coordinate: 320
		* width: 20
		* height: 20
* test that you can move your car by changing the x coordinate to 0... 
	* if something was left behind, then revisit the your calls to rect and ellipse
	* change numbers to variables where appropriate
* now would be a good time to save your work... you can check out the __Saving Your Work__ section below
* __this part is optional__:
	* add some windows (or rims, or neon lights, or whatever!)
	* create a background scene, like adding a horizon/ground
	* add a shadow
	* for example:
![customized car](customized_car.png)

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
* create a repository on github named __lab\_7\_part\_2__
	* go to [github.com](github.com)
	* create an account if you don't already have one
	* create a new repository by clicking on the __new repository__ icon on the upper right hand corner
![create a new repository](lab_2_github_new_repo.png)
	* fill in the information for your new repository
	* the name of your repository should be __lab\_7\_part\_2__
	* the rest of the form should be filled out accordingly
	* an example from the last class:
![name new repository](lab_2_github_name_repo.png)
	* keep the url handy... it should be something like: __https://github.com/foureyes/lab\_7\_part\_2.git__
	* here's an example from an earlier class:
![repo url](lab_2_github_repo_url.png)
* once you've created your repository, go to your __lab\_7\_part\_2__ folder in terminal
* use __pwd__ to __make sure you're in the right directory__
* use the url you just copied with __git remode add__ to identify github as a remote repository (called __origin__):
{% highlight bash %}
git remote add origin https://github.com/foureyes/lab_7_part_2.git
{% endhighlight %}
* finally, push your changes to github:
{% highlight bash %}
git push origin master
{% endhighlight %}
* verify that your changes are in github by refreshing your repository page

<!-- close_-->
