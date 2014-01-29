---
layout: lab
title: Lab 7, Part 1 - Snowman
prefix: ../../
---
# Lab 7, Part 1 - Snowman

## Overview

* You're creating a snowman.  Just in time for... spring!?
* You'll have to use variables.
* &#9731;&#9731;&#9731;&#9731;&#9731;&#9731;&#9731;
* [Unicode Snowman for You](http://unicodesnowmanforyou.com/)

## Instructions

### Set up Your Local Repository
* using the commandline, create a folder called __lab\_7\_part\_1__ in your ~/Desktop/username folder
* change to your __~/Desktop/username/lab\_7\_part\_1__ folder
* use pwd to verify that you're in the correct folder
	* you should be in __~/Desktop/username/lab\_7\_part\_1__
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
* __immediately__ name your sketch by saving it as __snowman__ in your __~/Desktop/username/lab\_7\_part\_1__ folder
* put in your setup and draw methods
* __save your sketch again!__
* go back to terminal; make sure you're in __~/Desktop/username/lab\_7\_part\_1__
* in terminal, check the status of your repository - you should have a folder or file called __snowman__ that's not yet _staged_
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
#	snowman/
{% endhighlight %}
* again, you may snowman.pde instead of the folder snowman; that's fine...
* using git, save a revision of your empty sketch to your local repository that you created above by...
* adding your changes so that they'll be committed
{% highlight bash %}
git add --all
{% endhighlight %}
* and then... actually commit your work
{% highlight bash %}
git commit -m 'an empty sketch for creating a snowman'
{% endhighlight %}

### Drawing Your Snowman

* You will be creating the following sketch:
![snowman](snowman.png)
* in the setup() function, set the size of your window to 500 x 500 by using the [size](http://processing.org/reference/size_.html) function
* create two variables outside of the draw() function, they should be x and y
* create 3 circles for the snowman's body... the first two _arguments_ of the circle should be the variables you created with potential additions or subtractions
* optionally... draw a face!
* save your sketch in processing __and__ save your work using version control too!

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
* create a repository on github named __lab\_7\_part\_1__
	* go to [github.com](github.com)
	* create an account if you don't already have one
	* create a new repository by clicking on the __new repository__ icon on the upper right hand corner
![create a new repository](lab_2_github_new_repo.png)
	* fill in the information for your new repository
	* the name of your repository should be __lab\_7\_part\_1__
	* the rest of the form should be filled out accordingly
	* an example from the last class:
![name new repository](lab_2_github_name_repo.png)
	* keep the url handy... it should be something like: __https://github.com/foureyes/lab\_7\_part\_1.git__
	* here's an example from an earlier class:
![repo url](lab_2_github_repo_url.png)
* once you've created your repository, go to your __lab\_7\_part\_1__ folder in terminal
* use __pwd__ to __make sure you're in the right directory__
* use the url you just copied with __git remode add__ to identify github as a remote repository (called __origin__):
{% highlight bash %}
git remote add origin https://github.com/foureyes/lab_7_part_1.git
{% endhighlight %}
* finally, push your changes to github:
{% highlight bash %}
git push origin master
{% endhighlight %}
* verify that your changes are in github by refreshing your repository page

<!-- close_-->
