---
layout: lab
title:  Lab - A Short Program with Version Control
prefix: ../../
---
# Lab - A Short Program with Version Control

## Objectives

* create a local repository
	* git init
* get info about your repository and your working directory
	* git status
	* git diff
* stage your changes and take a snapshot of your work
	* git add
	* git commit
* revert to a previous version
	* git reset

## Overview

1. write a simple processing program 
2. edit your program and track your changes with version control

## Part 1 - A Simple Processing Program

### Prep Your Working Folder
1. if it does not already exist, create a folder on your desktop:
	* name it using your __first initial and your last name__
	* use terminal to do this
2. in terminal change into this newly created directory
	* verify that you're in the correct directory by using pwd
	* it should return something like: __/Users/professor/Desktop/jversoza__
3. if you are not in the correct directory:
	* go to your Desktop in terminal by using cd
	* verify that you created your directory using ls
	* change into your directory using cd
4. example of verification below:
{% highlight bash %}
walsh-9:jversoza joe$ pwd
/Users/professor/Desktop/jversoza
{% endhighlight %}

### Create a Simple Processing Program
* open processing
	* if you have two versions, open the latest version
	* do not run the update
* a new sketch should have opened automatically
* immediately save your program by going to the upper menu: __File &rarr; Save As__
![save as](lab_1_save_as.png)
* name your program: __shapes__
![name](lab_1_name.png)
* verify your program exists in your folder
	* go back to terminal
	* use pwd to make sure you're in: __/Users/professor/Desktop/jversoza__
	* use __ls__ to show that there's a new folder called __shapes__
* create a simple program that draws a circle
* go back to processing
* define your setup and draw functions
{% highlight bash %}
void setup() {
  
}

void draw() {
  // draw your shapes here  
}
{% endhighlight %}
* in your setup function, between the curly braces, __set the size of your window to 200 by 150...__ [see size() in the processing docs](http://processing.org/reference/size_.html)
* in your setup function __set your background to green__... [see backround() in the processing docs](http://processing.org/reference/background_.html)
* in your draw function, __draw a blue circle with a diameter of 50__... [see ellipse() in the processing docs](http://processing.org/reference/ellipse_.html), [as well as fill()](http://processing.org/reference/fill_.html)
![blue circle](lab_1_blue_circle.png)

## Part 2 - Version Control, Making and Tracking Changes

### Create a Repository from Your Shapes Program, Your Initial Commit

* go to terminal
* verify that you&quot;re in your in: __/Users/professor/Desktop/jversoza__
* use ls to show that the __shapes__ directory is present
* change into the shapes directory
* verify that you're in: __/Users/professor/Desktop/jversoza/shapes__
* create a repository by using the following command:
{% highlight bash %}
git init
{% endhighlight %}
* verify that your repository was created by checking the status of your working directory using __git status__
{% highlight bash %}
git status
{% endhighlight %}
* you should see the following output... __make sure that shapes.pde appears in the output!__
{% highlight bash %}
# On branch master
#
# Initial commit
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#	shapes.pde
nothing added to commit but untracked files present (use "git add" to track)
{% endhighlight %}
* set your name for this repository using __git config user.name "your name"__
{% highlight bash %}
git config user.name "Joe Versoza"
{% endhighlight %}
* set your email for this repository using __git config user.email your@email.address__ 
{% highlight bash %}
git config user.email your@email.address
{% endhighlight %}
* track your pde file (your processing program) and add it to your staged changes by using __git add name_of_file__:
{% highlight bash %}
git add shapes.pde
{% endhighlight %}
* verify that you have staged your changes by using __git status__ again
{% highlight bash %}
git status
{% endhighlight %}
* you should see the following output... __make sure that shapes.pde appears in the output!__
{% highlight bash %}
# On branch master
#
# Initial commit
#
# Changes to be committed:
#   (use "git rm --cached <file>..." to unstage)
#
#	new file:   shapes.pde
#
{% endhighlight %}
* save your work / take a snapshot by using __git commit -m 'your commit message'__
{% highlight bash %}
git commit -m 'added shapes.pde'
{% endhighlight %}
* your output should end in something like...
{% highlight bash %}
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 shapes.pde
{% endhighlight %}
* notice that now, when you check the status of your repo, you see that there's nothing staged and no changes in your working directory
{% highlight bash %}
 git status
# On branch master
nothing to commit (working directory clean)
{% endhighlight %}

### Editing Your Code and Tracking Changes

* let's add a red square that's 40 by 40 on the upper left corner of your processing program... [see rect() in the processing docs](http://processing.org/reference/rect_.html), and of course, fill()
![red square](lab_1_red_square.png)
* __save your program__
* go back to terminal and use the command the we learned to check the __status__ of your working directory
* the output should end with with the following lines:
{% highlight bash %}
# On branch master
# Changed but not updated:
#   (use "git add <file>..." to update what will be committed)
#   (use "git checkout -- <file>..." to discard changes in working directory)
#
#	modified:   shapes.pde
#
no changes added to commit (use "git add" and/or "git commit -a")
{% endhighlight %}
* let's see what changes were made to the file!  use __git diff__:
{% highlight bash %}
git diff --color
{% endhighlight %}
* the output should look something like:
{% highlight diff %}
--- a/shapes.pde
+++ b/shapes.pde
@@ -7,5 +7,6 @@ void draw() {
   // draw your shapes here
   fill(0, 0, 255);
   ellipse(100, 75, 50, 50);
-
+  fill(255, 0, 0);
+  rect(0, 0, 49, 40);
 }
{% endhighlight %}
* note that the plus symbols are lines in the new version of the file!
* stage your changes by using the command that we used to __add__ files to the set of changes that we're going to commit
* check that you've staged your changes by using the command for getting the __status__ of our working directory again... the output should look like:
{% highlight bash %}
# On branch master
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
#	modified:   shapes.pde
#
{% endhighlight %}
* go ahead and save your changes by using the command that we learned to __commit__ staged changes.  remember to add a commit message like "added a red square".  the output should look like:
{% highlight bash %}
[master 9622f04] added a red square
 1 files changed, 11 insertions(+), 0 deletions(-)
{% endhighlight %}
* now use __git log__ to show all of the changes that you've made so far
{% highlight bash %}
git log
{% endhighlight %}
* the output should look like:
{% highlight bash %}
commit 9622f0471b72e77de958771d8997a40e66620525
Author: Joe Versoza <joe@walsh.local>
Date:   Wed Mar 6 08:21:11 2013 -0500

    added a red square

commit d5b42be244348b0d640765b410519ba821c93ea7
Author: Joe Versoza <joe@walsh-9.(none)>
Date:   Wed Mar 6 08:00:03 2013 -0500

    added shapes.pde
{% endhighlight %}
* finally, let's add a readme file
* go back to terminal
* ensure that you're in the __shapes__ directory
* run the following commands to create and edit your README file
{% highlight bash %}
touch README.md
nano README.md
# in nano, type in "this is the first part of lab 5"
{% endhighlight %}
* save your file in nano by:
	* typing CTRL + O
	* typing ENTER after seeing: __File Name to Write: README.md__
* exit nano by typing CTRL + X
* check the __status__ of your working directory
* __add__ your README.md file to your list of staged changes
* __commit__ your change

### Reverting a Commiti and Unstaging Changes
* change the color of your rectangle to blue
* __save your work__
* use git status and git diff to see your change
* use git add to stage your change
* use git status again to see that your change was staged
* use git commit to save your work
* uh-oh... didn't mean to do that.  
* use __git reset HEAD^__ to move your commit back to modifications in your working directory
{% highlight bash %}
git reset HEAD^
{% endhighlight %}
* the output should be:
{% highlight bash %}
Unstaged changes after reset:
M	shapes.pde
{% endhighlight %}
* notice that the commit became changes in your working directory!
{% highlight bash %}
git status

# On branch master
# Changed but not updated:
#   (use "git add <file>..." to update what will be committed)
#   (use "git checkout -- <file>..." to discard changes in working directory)
#
#	modified:   shapes.pde
#
{% endhighlight %}
* you can __stage__ those changes again with git add
{% highlight bash %}
git add shapes.pde 
git status

# On branch master
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
#	modified:   shapes.pde
#
{% endhighlight %}
* however, this time, instead of commit, you can unstage the changes again if you want to undo items that you've added by using an alternative form of __reset__
{% highlight bash %}
git reset shapes.pde 
{% endhighlight %}
* output should be:
{% highlight bash %}
Unstaged changes after reset:
M	shapes.pde
{% endhighlight %}
