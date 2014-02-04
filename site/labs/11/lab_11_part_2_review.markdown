---
layout: lab
title: Lab 11, Part 2 - HTML and CSS Review
prefix: ../../
---
# Lab 11, Part 2 - HTML and CSS Review

## Overview

* review HTML and CSS
* review uploading files

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
* open this url: https://github.com/MTEC1002/lab\_11\_part\_2.git
* click on fork
![fork](../../resources/img/github-fork.png)
* wait for it...
* you should now have a repository url that you can copy


__Clone__

* copy the url from your newly forked repository
* it should look something like: https://github.com/yourusername/lab\_11\_part\_2.git
* if you don't see your repository url...
	* click on your user name on the upper right corner
![name](../../resources/img/github-name.png)
	* click on the repositories tab
![repository](../../resources/img/github-repositories.png)
* click on the repository named lab\_11\_part\_2
* open terminal
* use __pwd__ to make sure that you're in __~/Desktop/username__ 
	* if you're already in this folder, then you're fine!
	* otherwise, you may be one folder in; if you are, __cd ..__ 
* clone this repository 
{% highlight bash %}
git clone https://github.com/yourusername/lab_11_part_2.git
{% endhighlight %}

__Configuration__

* cd into the directory that you just cloned
{% highlight bash %}
cd lab_11_part_2.git
{% endhighlight %}
* use git config to set the name and email that you want displayed on your commits
{% highlight bash %}
git config user.name  "your name!"
git config user.email your@email.address
{% endhighlight %}


### Create a Two Page Site!

#### Home Page

* with TextWrangler create a page called __home.html__ in your lab\_11\_part\_2 directory
* start with the [basic structure](http://www.htmldog.com/guides/html/beginner/tags/) needed for an html5 document
* put in a [title](http://www.htmldog.com/guides/html/beginner/titles/) called: Lab 11 Home
* create a [heading](http://www.htmldog.com/guides/html/beginner/headings/), h1, with text: Lab 11, Part 2 - Review
* create a smaller [heading](http://www.htmldog.com/guides/html/beginner/headings/), h2, with text: Home
* create a [list](http://www.htmldog.com/guides/html/beginner/lists/) under the heading
* in that list put two list items that are [links](http://www.htmldog.com/guides/html/beginner/links/):
	* home links to home.html
		* add a class to this list item called 'active'
	* about links to about.html
* create a [paragraph](http://www.htmldog.com/guides/html/beginner/paragraphs/) under that list
* in your paragraph tag, write in: Welcome to lab 11!!!!  That's a lot of exclamation points!!!!!  Have some more!!!!
* add an [image](http://www.htmldog.com/guides/html/beginner/images/) at the end of your page
	* &lt;img&gt; (no closing tag)
	* add a src attribute, set it equal to an image of a pizza
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)... you can wait to use git push at the end of the lab


#### About Page

* with TextWrangler create a page called __about.html__ in your lab\_11\_part\_2
* start with the [basic structure](http://www.htmldog.com/guides/html/beginner/tags/) needed for an html5 document
* put in a [title](http://www.htmldog.com/guides/html/beginner/titles/) called: Lab 11 About
* create a [heading](http://www.htmldog.com/guides/html/beginner/headings/), h1, with text: Lab 11, Part 2 - Review
* create a smaller [heading](http://www.htmldog.com/guides/html/beginner/headings/), h2, with text: About
* create a [paragraph](http://www.htmldog.com/guides/html/beginner/paragraphs/) under that list
* in your paragraph tag, write in: This is for MTEC1002
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)... you can wait to use git push at the end of the lab

#### Style Your Pages

* with TextWrangler create a stylesheet called __mystyles.css__ in your lab\_11\_part\_2
* edit __about.html__ so that [it uses your stylesheet](http://www.htmldog.com/guides/css/beginner/applyingcss/)
* edit __home.html__ so that [it uses your stylesheet](http://www.htmldog.com/guides/css/beginner/applyingcss/)
* in your stylesheet, make sure that the entire page uses sans-serif fonts
* make your largest headers red
* put a black border around every element with a class of active
* put in [this](http://images.wikia.com/adventuretimewithfinnandjake/images/3/3a/S1e1_flip_out.png) as a repeating background image!
* make the margins around your paragraphs 20px
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)
* git push origin master!

### Upload all of Your Files to Your Server

* review the [previous lab](lab_11_part_1_remote.markdown) 
* upload your files to your server using any method from above:
	* scp
	* sftp (commandline)
	* sftp (graphical)
