---
layout: lab
title: Branching and Merging
prefix: ../../
---
# Lab 6 - Branching and Merging

In this lab, you'll be modifying your a previous program.  You will use your cloned copy of face_var and modify face_var so that it includes eyebrows.


## General Instructions

Some logistics:

* because we're cloning (or already cloned a repository), there's no need to initialize a new repo 
* we'll be using branches to manage our changes

## Eyebrows

### Set up Your Local Repository
* open terminal, change to your __~/Desktop/username/
* use pwd to verify that you're in the correct folder
	* you should be in __~/Desktop/username/
	* if you're not, cd into it
* once you're in the correct folder, clone your __face\_var__ repository (get the url of the repository by going to github and browsing to your __face\_var__ repository)
{% highlight bash %}
git clone https://github.com/foureyes/face_var.git
{% endhighlight %}
* if you type ls, you should now see your __face\_var__ directory
* cd into __face\_var__
* now... configure your user name and email for your commits (these do not have to be the same as your github account)
{% highlight bash %}
# in the directory of your repository
git config user.name  "foo bar baz"
git config user.email foo@bar.baz
{% endhighlight %}

<!-- end bold__ -->

### Modify Your Sketch - Draw Some Eyebrows!

You will be creating the following drawing (of course, the face you drew will be different from this example, but the main change is the addition of eyebrows.  Optionally, you can put on glasses.  Or both!):

![eyebrows](eyebrows.png)

* let's try using branches
	* in terminal, in the face_var directory
	* list branches
{% highlight bash %}
git branch
{% endhighlight %}
	* should only show 1 branch: master (it will have a star in front of it)
	* create a new branch called eyebrows
{% highlight bash %}
git branch eyebrows
{% endhighlight %}
	* list branches again...
{% highlight bash %}
git branch
{% endhighlight %}
	* should show 2 branches: master and eyebrows
	* switch to the eyebrows branch
{% highlight bash %}
git checkout eyebrows
{% endhighlight %}
	* list branches again...
{% highlight bash %}
git branch
{% endhighlight %}
	* now the star should be next to eyebrows; you're in the right branch
	* now you're ready to make your changes in your new branch
* draw eyebrows
	* use the existing x and y variables to draw eyebrows relative to the eyes
	* you would call line... but all four paremeters would be based on the x and y variables
	* when you're done drawing, call status, add and commit to save your work
* merging back to master
	* __close processing__
	* switch back to the master branch
{% highlight bash %}
git checkout master
{% endhighlight %}
	* make sure you're in master
{% highlight bash %}
git branch
{% endhighlight %}
	* find the difference between the old branch and the new branch
{% highlight bash %}
git diff master eyebrows
{% endhighlight %}
	* merge...
{% highlight bash %}
git merge eyebrows
{% endhighlight %}
	* push everything up to github (we don't have add a remote repository, because it's already defined)
	* we'll push both branches
{% highlight bash %}
git push origin master
git push origin eyebrows
{% endhighlight %}
* verify that your changes are in github by refreshing your repository page

