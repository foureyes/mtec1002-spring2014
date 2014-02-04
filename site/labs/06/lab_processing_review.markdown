---
layout: lab
title: Git and Processing Exercises
prefix: ../../
---
# Lab 6 - Git and Processing Exercises

In this lab, you'll be creating two sketches

1. circles and squares
2. lines
	1. multiple lines
	2. gradient

## General Instructions

Some logistics:

* __save all of these in your Desktop/username (your first initial, last name) folder first!__
* __save as the name of the thing that you're drawing__

For each sketch:

1. create a local repository
2. commit your work as you code
3. when you're done with all of your code
4. create a remote repository on github
5. push to github

For the second sketch, commit after the first part, and then again after the second part.

## Part 1 - circles_squares

### Set up Your Local Repository
* create a folder called __lab\_6\_part\_1__ in your ~/Desktop/username folder
* open terminal, change to your __~/Desktop/username/lab\_6\_part\_1__ folder
* use pwd to verify that you're in the correct folder
	* you should be in __~/Desktop/username/lab\_6\_part\_1__
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
* put in your setup and draw methods
* name your sketch __circles_squares__ and save it in __~/Desktop/username/lab\_6\_part\_1__
* again, make sure you've __saved__! 
* add your empty sketch to your local repository that you created above
* do this by making sure you're in __~/Desktop/username/lab\_6\_part\_1__
* get the status: 
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
#	circles_squares/
{% endhighlight %}
* you may have just circles_squares.pde instead of the folder circles_squares; that's fine...
* add your changes so that they'll be committed
{% highlight bash %}
git add --all
{% endhighlight %}
* commit your work
{% highlight bash %}
git commit -m 'initital commit for circles squares'
{% endhighlight %}

### Draw Circles and Squares

You will be creating the following pattern:

![circles squares](circles_squares.png)

* create the pattern in the image above
	* draw alternating circles and squares
	* use a for loop
	* and a conditional (if... else)
	* using mod (__%__ - if(i % 2 == 0)) will help alternate
	* each should be 20 pixels apart
	* each square should be 40 x 40
	* each square should be yellow
	* each circle should have a diamater of 40
	* each circle should be blue
* use the following git commands to save your work: status, diff, add and commit
	* remember, __add__ either takes a specific file name or --all
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
* create a repository on github named __lab\_6\_part\_1__
	* go to [github.com](github.com)
	* create an account if you don't already have one
	* create a new repository by clicking on the __new repository__ icon on the upper right hand corner
![create a new repository](lab_2_github_new_repo.png)
	* fill in the information for your new repository
	* the name of your repository should be __lab\_6\_part\_1__
	* the rest of the form should be filled out accordingly
	* an example from the last class:
![name new repository](lab_2_github_name_repo.png)
	* keep the url handy... it should be something like: __https://github.com/foureyes/lab\_6\_part\_1.git__
	* here's an example from the last class:
![repo url](lab_2_github_repo_url.png)
* once you've created your repository, go to your __lab\_6\_part\_1__ folder in terminal
* use __pwd__ to __make sure you're in the right directory__
* use the url you just copied with __git remode add__ to identify github as a remote repository (called __origin__):
{% highlight bash %}
git remote add origin https://github.com/foureyes/lab_6_part_1.git
{% endhighlight %}
* finally, push your changes to gihub:
{% highlight bash %}
git push origin master
{% endhighlight %}
* verify that your changes are in github by refreshing your repository page

<!-- close_-->





## Part 2 - lines

### Set up Your Local Repository
* create a folder called __lab\_6\_part\_2__ in your ~/Desktop/username folder
* open terminal, change to your __~/Desktop/username/lab\_6\_part\_2__ folder
* use pwd to verify that you're in the correct folder
	* you should be in __~/Desktop/username/lab\_6\_part\_2__
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
* put in your setup and draw methods
* name your sketch __lines__ and save it in __~/Desktop/username/lab\_6\_part\_2__
* again, make sure you've __saved__! 
* add your empty sketch to your local repository that you created above
* do this by making sure you're in __~/Desktop/username/lab\_6\_part\_2__
* get the status: 
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
#	lines/
{% endhighlight %}
* you may have just lines.pde instead of the folder lines; that's fine...
* add your changes so that they'll be committed
{% highlight bash %}
git add --all
{% endhighlight %}
* commit your work
{% highlight bash %}
git commit -m 'initital commit for lines'
{% endhighlight %}

### Draw Lines

#### Draw Lines, 10 Pixels Apart
You will be creating the following pattern:

![lines](lines_10_apart.png)

* create the pattern in the image above
	* create a sketch that's 400 x 400 using the size function in setup (see the [online documentation for size](http://processing.org/reference/size_.html))
	* use a for loop to draw 40 lines, each 10 pixels apart
	* use the line function (see the [online documentation for line](http://processing.org/reference/line_.html)) with your loop variable (probably i) as the y values for your end points 
	* your loop variable, i, will probably have to be multiplied by some constant 
	* hint: you can try making your loop go only 40 iterations
	* hint: you can do something like i * _some constant_ to get your y values
	* hint: you can use _width_ as your second x value to get your line to go all the way across (see the [onine documentation for width](http://processing.org/reference/width.html))
* use the following git commands to save your work: status, diff, add and commit
	* use a meaningful commit message like... git commit -m 'created 40 lines, 10 pixels apart'
	* remember, __add__ either takes a specific file name or --all
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

#### Create a Color Gradient With Lines

You will be modifying your program to create the following sketch:

![gradient](gradient.png)

* create the sketch above
	* using your previous sketch...
	* instead of drawing your lines 10 pixels apart, draw them right next to eachother
	* hint: that means your loop should go up to _height_ rather than 40... since you'll need 400 lines!
	* change the color of your line on each iteration of the loop by using stroke() (see the [online documentation for stroke](http://processing.org/reference/stroke_.html)
		* set the red value to your loop variable over 2! 
		* keep the green and blue values constant (somewhere above 150)
* use git diff to see your changes
* now use add and commit to save them!
* once you're done committing....
* run git status, you should have nothing to commit:
{% highlight bash %}
git status

# On branch master
nothing to commit (working directory clean)
{% endhighlight %}


### Pushing to a Remote Repository
* when you're done with your sketch, and everything is committed, submit your assignment by pushing to github
* create a repository on github named __lab\_6\_part\_2__
	* go to [github.com](github.com)
	* create an account if you don't already have one
	* create a new repository by clicking on the __new repository__ icon on the upper right hand corner
![create a new repository](lab_2_github_new_repo.png)
	* fill in the information for your new repository
	* the name of your repository should be __lab\_6\_part\_2__
	* the rest of the form should be filled out accordingly
	* an example from the last class:
![name new repository](lab_2_github_name_repo.png)
	* keep the url handy... it should be something like: __https://github.com/foureyes/lab\_6\_part\_2.git__
	* here's an example from the last class:
![repo url](lab_2_github_repo_url.png)
* once you've created your repository, go to your __lab\_6\_part\_2__ folder in terminal
* use __pwd__ to __make sure you're in the right directory__
* use the url you just copied with __git remode add__ to identify github as a remote repository (called __origin__):
{% highlight bash %}
git remote add origin https://github.com/foureyes/lab_6_part_2.git
{% endhighlight %}
* finally, push your changes to gihub:
{% highlight bash %}
git push origin master
{% endhighlight %}
* verify that your changes are in github by refreshing your repository page
