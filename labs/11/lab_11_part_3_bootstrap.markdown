---
layout: lab
title: Lab 10, Part 4 - HTML
prefix: ../../
---
# Lab 10, Part 4 - HTML 

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

* log in to github.com (if you're not already logged in)
* open this url: https://github.com/MTEC1002/lab\_10\_part\_4.git
* click on fork
![fork](../../resources/img/github-fork.png)
* wait for it...
* you should now have a repository url that you can copy


__Clone__

* copy the url from your newly forked repository
* it should look something like: https://github.com/yourusername/lab\_10\_part\_4.git
* if you don't see your repository url...
	* click on your user name on the upper right corner
![name](../../resources/github-name.png)
	* click on the repositories tab
![name](../../resources/github-repositories.png)
* click on the repository named lab\_10\_part\_4
* open terminal
* use __pwd__ to make sure that you're in __~/Desktop/username__ 
	* if you're already in this folder, then you're fine!
	* otherwise, you may be one folder in; if you are, __cd ..__ 
* clone this repository 
{% highlight bash %}
using git clone https://github.com/yourusername/lab\_10\_part\_4.git
{% endhighlight %}

__Configuration__

* cd into the directory that you just cloned
{% highlight bash %}
cd lab\_10\_part\_1.git
{% endhighlight %}
* use git config to set the name and email that you want displayed on your commits
{% highlight bash %}
git config user.name  "your name!"
git config user.email your@email.address
{% endhighlight %}


### Create an Your Own Page!

#### Create Your Files

* use TextWrangler to create two new files
* use save as to save both files under your lab\_10\_part\_4 folder that's in your ~/Desktop/username folder
	* use (Save As...)
	* one should be called mypage.html
	* one should be called mystyles.css
* view your page 
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)

#### Lists and Headings

In mypage.html...

* create a heading (largest - h1), with text: Some Useful Information
* create a heading (second largest - h2), with text: Top 3 Cat Names 
* under the heading, create an ordered list of your top 3 cat names
	* maybe: chairman meow, katy purry, yo yo meow
* add another heading (second largest - h2), with text: Do Not Eat List
* under the heading, create an unordered list of foods that you refuse to eat
	* for each food, link to a relevant wikipedia article
* view your page 
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)

#### A Table

In mypage.html...

* add a table containing 4 rows and 2 columns (use table, tr, td)
	* in the first row, first column type in: animal 
	* in the first row, second column type in: awesome
	* in each remaining row, add an animal and yes or no (for example: narwhale and YES!)
* view your page 
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)

#### Paragraphs

In mypage.html...

* create three paragraphs (use p tags)
	* one should have the text: this is the first paragraph
	* the second should be: paragraph number two!!!
	* and the third should be: last one, really...
* in the third paragraph, make the word "really" a link to google

#### Styling

In mypage.html...

* include mystyles.css

In mystyles.css (and mypage.html for some)...

* make all links turn red when they're hovered over
* make all headers (both h1 and h2) uppercase through css
* give all paragraphs a border that's 2 pixels wide, dashed and black
* in the first paragraph, add an id called top (id="top") as an attribute
	* add 50 pixels of padding for a paragraph with an id of top
* add 25 pixels of margin for each paragraph
* double the size of links that are within an element that has an id of top
* choose one list item from the top 3 cat names and one list item from the do not eat list
	* add a class attribute named highlight to both of those list items (class="highlight")
	* add a style that makes all text that has that class have a yellow background
* use git to check the __status__, __add__ to staging, and __commit__ (don't forget the __-m 'message'__ part)

### Upload Your Files!

* open your SFTP client, CyberDuck
* connect to foureyes.in using your account
* navigate to public_html
* open finder... go to ~/Desktop/username/lab_10_part_4
* drag your files to the your sftp client
* check [http://foureyes.in/~username/mypage.html](http://foureyes.in/~username/mypage.html)
