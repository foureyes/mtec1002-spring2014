---
layout: lab
title: Lab 11, Part 3 - Github Pages
prefix: ../../
---

# Lab 11, Part 3 - Github Pages

## Overview

* create a processing sketch
* add a project page to describe it using github pages

## Instructions

### Cleaning Up

* close terminal

### Prep Work

* if it's not already created, make a directory on your desktop with your first initial and last name
	* it should be __~/Desktop/username/__
	* do this using terminal
* in terminal change to your __~/Desktop/username/__ folder
* use pwd to verify that you're in the correct folder
	* you should be in __~/Desktop/username/__
	* if you're not, cd into it

### Fork and Clone

__Fork__

* log in to github.com
* open this url: https://github.com/MTEC1002/lab\_11\_part\_3.git
* click on fork
![fork](../../resources/img/github-fork.png)
* wait for it...
* you should now have a repository url that you can copy


__Clone__

* copy the url from your newly forked repository
* it should look something like: https://github.com/yourusername/lab\_11\_part\_3.git
* if you don't see your repository url...
	* click on your user name on the upper right corner
![name](../../resources/img/github-name.png)
	* click on the repositories tab
![repository](../../resources/img/github-repositories.png)
* click on the repository named lab\_11\_part\_3
* open terminal
* use __pwd__ to make sure that you're in __~/Desktop/username__ 
	* if you're already in this folder, then you're fine!
	* otherwise, you may be one folder in; if you are, __cd ..__ 
* clone this repository 
{% highlight bash %}
git clone https://github.com/yourusername/lab_11_part_3.git
{% endhighlight %}

__Configuration__

* cd into the directory that you just cloned
{% highlight bash %}
cd lab_11_part_3.git
{% endhighlight %}
* use git config to set the name and email that you want displayed on your commits
{% highlight bash %}
git config user.name  "your name!"
git config user.email your@email.address
{% endhighlight %}


### Creating a Project with a Project Page

#### Sketch

* create a processing sketch called __circle__ and save it in your lab\_11\_part\_3 directory
* in your processing sketch
	* draw a yellow circle with a 200 pixel diameter in the center of your sketch
	* create a blue background
	* make the window size 500 x 500
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)... 
* use git push origin master to save your work to your remote server

#### github Pages

* follow [this guide](https://help.github.com/articles/creating-project-pages-manually) to create a project page that shows up under:
	* yourusername.github.io/lab\_11\_part\_3/

