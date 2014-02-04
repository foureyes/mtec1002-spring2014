---
layout: lab
title: Lab 10, Part 1 - HTML
prefix: ../../
---
# Lab 10, Part 1 - HTML 

## Overview

* create a basic html page

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
* open this url: https://github.com/MTEC1002/lab\_10\_part\_1.git
* click on fork
![fork](../../resources/img/github-fork.png)
* wait for it...
* you should now have a repository url that you can copy


__Clone__

* copy the url from your newly forked repository
* it should look something like: https://github.com/yourusername/lab\_10\_part\_1.git
* if you don't see your repository url...
	* click on your user name on the upper right corner
![name](../../resources/img/github-name.png)
	* click on the repositories tab
![repository](../../resources/img/github-repositories.png)
* click on the repository named lab\_10\_part\_1
* open terminal
* use __pwd__ to make sure that you're in __~/Desktop/username__ 
	* if you're already in this folder, then you're fine!
	* otherwise, you may be one folder in; if you are, __cd ..__ 
* clone this repository 
{% highlight bash %}
git clone https://github.com/yourusername/lab_10_part_1.git
{% endhighlight %}

__Configuration__

* cd into the directory that you just cloned
{% highlight bash %}
cd lab_10_part_1.git
{% endhighlight %}
* use git config to set the name and email that you want displayed on your commits
{% highlight bash %}
git config user.name  "your name!"
git config user.email your@email.address
{% endhighlight %}


### Create an HTML Page!

#### Basic Structure

* open up TextWrangler (try Command+SPACEBAR to search for TextWrangler)
* on the top menu bar, click on File&rarr;Open
	* ![open](../../resources/img/tw-open.png)
* browse to home&rarr;Desktop&rarr;usernamefolder&rarr;lab\_10\_part\_1&rarr;index.html
* create a skeleton page by using the following tags
	* &lt;!DOCTYPE html&gt; (note that this has no closing tag)
	* &lt;html lang="en"&gt;
	* &lt;head&gt;
	* &lt;body&gt;
* view your page by opening it in your browser (double click on the file from finder or option-click&rarr;Open With... your browser)
* add text between the body tags
* view your page (now just hit the refresh/reload button on your browser)
* add a title; it should go in head
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)

#### Paragraphs and Headings

* add another line of text
* view your page (note that there are no line breaks!)
* add paragraph tags around each line of text
* view your page (note that the text is now on separate lines!)
* add some emphasis and strong tags around some text in one of the paragraphs
	* &lt;em&gt; 
	* &lt;strong&gt; 
* view your page (look for italicized and bolded text!)
* add a header tag before each paragraph
	* add an &lt;h1&gt; first
	* add an &lt;h2&gt; next
* add one more header tag, an h1 again... and add another paragraph tag underneath it
* view your page (look for both headers)
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)

#### Lists and Links

* add an ordered list after your headers and paragraphs
	* &lt;ol&gt;
	* &lt;li&gt;
* view your page (look for both headers)
* add an un-ordered list after your previous list
	* &lt;ul&gt;
	* &lt;li&gt;
* change one of your list items so that some of the text within it is a link
	* &lt;a&gt;
* do the same for some text within one of the paragraphs (perhaps link to largest island in a lake)
* add another link in one of your paragraphs (perhaps link to garfield without garfield)
* view your page and check that your links work
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)

#### Images and Tables

* add an image somewhere on your page
	* &lt;img&gt; (no closing tag)
	* add a src attribute, set it equal to http://foureyes.github.io/mtec1002/labs/04/face.png
* view your page 
* add a table
	* make it 2 columns, 3 rows
	* &lt;table&gt;, &lt;tr&gt;, &lt;td&gt;
	* add text into each table cell
* view your page 
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)

### Submit Your Work Through GitHub

* use git to check the __status__, __add__, __commit__ (don't forget the __-m 'message'__ part)
* since you cloned, your repository is already aware of your remote repository...
* so, all you have to do is __push__ (don't forget __origin master__)
* check that your code is on github by refreshing the page
