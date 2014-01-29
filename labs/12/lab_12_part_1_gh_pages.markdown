---
layout: lab
title: Lab 12, Part 1 - GitHub Pages
prefix: ../../
---

# Lab 12, Part 1 - GitHub Pages

## Overview

* use [github pages](http://pages.github.com/) to __publish__ a page

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
* open this url: https://github.com/MTEC1002/lab\_12\_part\_1.git
* click on fork
![fork](../../resources/img/github-fork.png)
* wait for it...
* you should now have a repository url that you can copy


__Clone__

* copy the url from your newly forked repository
* it should look something like: https://github.com/yourusername/lab\_12\_part\_1.git
* if you don't see your repository url...
	* click on your user name on the upper right corner
![name](../../resources/img/github-name.png)
	* click on the repositories tab
![repository](../../resources/img/github-repositories.png)
* click on the repository named lab\_12\_part\_1
* open terminal
* use __pwd__ to make sure that you're in __~/Desktop/username__ 
	* if you're already in this folder, then you're fine!
	* otherwise, you may be one folder in; if you are, __cd ..__ 
* clone this repository 
{% highlight bash %}
git clone https://github.com/yourusername/lab_12_part_1.git
{% endhighlight %}

__Configuration__

* cd into the directory that you just cloned
{% highlight bash %}
cd lab_12_part_1.git
{% endhighlight %}
* use git config to set the name and email that you want displayed on your commits
{% highlight bash %}
git config user.name  "your name!"
git config user.email your@email.address
{% endhighlight %}


### Creating a Project Page

#### Verify Your GitHub Account

To create pages on github, you need to have a valid email address.  You can prove that you have a valid email address by going through github's email verification process.

* if haven't done so already, log in to [github.com](http://github.com)
* go to your github account settings
![account](../../resources/img/github-account.png)
* go to your email settings
![email](../../resources/img/github-emails.png)
* click on _verify_ to verify your email address
![verify](../../resources/img/github-verify.png)
* you should see confirmation that the email was sent
![sent](../../resources/img/github-sent.png)
* log in to your email
* find the confirmation email
* it should be from GitHub with a subject of "Please verify..."	
![subject](../../resources/img/github-subject.png)
* click on the link to verify your email address
* _Whew!_.  On to the next step...

#### Create Your Page in a Branch

* show what branch you're currently working in:
{% highlight bash %}
git branch
{% endhighlight %}
* this should result in (the star means that you're currently working on that branch):
{% highlight bash %}
* master
{% endhighlight %}
* create another branch in your local repository; call it gh-pages
{% highlight bash %}
git checkout -b gh-pages
{% endhighlight %}
* git should respond with:
{% highlight bash %}
Switched to a new branch 'gh-pages'
{% endhighlight %}
* now... check which branch you're on
{% highlight bash %}
git branch
{% endhighlight %}
* the star should be next to gh-pages
{% highlight bash %}
* gh-pages
  master
{% endhighlight %}
* create a new file called index.html using nano
{% highlight bash %}
nano index.html
{% endhighlight %}
* add the text: "My GitHub Page"
* CTRL-X to save (press Y, then enter when prompted to save the file)
* use __status__, __add__, and __commit__ to save your changes
* finally, send to github using git __push__, but make sure it goes to origin __gh-pages__!
{% highlight bash %}
git push origin gh-pages
{% endhighlight %}
* this should give back the following output (note the part that's gh-pages -&gt; gh-pages):
{% highlight bash %}
 * [new branch]      gh-pages -&gt; gh-pages
{% endhighlight %}
* wait about 5 to 10 minutes... (this is just for the first time that you create a page)
* open http://yourusername.github.io/lab\_12\_part\_1/ in your browser (replace yourusername with your actual username)

#### What to do While Waiting

Let's try out a different text editor (we've used two: nano and TextWrangler)

* download [Sublime Text 2](http://www.sublimetext.com/)
* ([here's the direct download link](http://c758482.r82.cf2.rackcdn.com/Sublime%20Text%202.0.1.dmg))
* extract the dmg (this might have been done automatically)
* drag the icon to the desktop
* start SublimeText2
* go to File &rarr; open
* browse to your Desktop &rarr; username folder &rarr; lab\_12\_part\_1 &rarr; __index.thml__
* open the file
* overwrite what's in your file with:
	* basic [html structure](http://www.htmldog.com/guides/html/beginner/tags/)
	* a [heading](http://www.htmldog.com/guides/html/beginner/headings/) that says lab_12_part_1
	* and a [list](http://www.htmldog.com/guides/html/beginner/lists/) with five elements, all [links](http://www.htmldog.com/guides/html/beginner/links/)
		* the first goes to your homepage: __index.html__ ... call it __home__
		* one to the octocat gallery: http://octodex.github.com/ ... call it __octocat__
		* the other to unicode snowman: http://unicodesnowmanforyou.com/ ... call it __snowman__
		* another link to: __about.html__ (not yet created) ... call it __about__
		* one last link to: __practice.html__ (not yet created) ... call it __practice__
* check in on your github page to see if it's available:
	* open http://yourusername.github.io/lab\_12\_part\_1/ in your browser (replace yourusername with your actual username)
* __-----------make sure your previous page (with just text) works before moving on--------------__
* if it works, you can use __status__, __add__, and __commit__ to save your work
* ...then __push__ to __origin__ __gh-pages__
* now look at your page again... 
	* open http://yourusername.github.io/lab\_12\_part\_1/ in your browser (replace yourusername with your actual username)
* finally, use [Fillerama](http://chrisvalleskey.com/fillerama/) to generate content to drop into your page
* copy the generated markup and drop it below the list that you created
* if it works, you can use __status__, __add__, and __commit__ to save your work
* ...then __push__ to __origin__ __gh-pages__
* check out your page again... 

#### Resources and Possibilities
* follow [this guide](https://help.github.com/articles/creating-project-pages-manually) to create a project page that shows up under:
* start making [javascript games](http://basicallydan.github.io/skifree.js/)

