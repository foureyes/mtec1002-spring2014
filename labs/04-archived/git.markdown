---
layout: lab
title: Media Tech Skill 2 - MTEC 1002 - Spring 2013
prefix: ../../
---
# Version Control

## Why Use It

* stop using .bak files!
	* always have a backup
	* no need to track yourself
* collaborate (branch and merge)
* document
* group related changes

## git

* we're using git!
* it's a _modern_ distributed version control system
	* doesn't have to use a central repository
	* but you can

## Which is Where Github Comes In

* web front-end to git
* addons like issue tracking, wiki, collaboration tools, etc.
* however, git and github are not the same thing!

## We're Going to use the git Commandline Client

* git clone http://repository.url
* git add -a
* git commit -m "your commit message"
* git status
* git push origin master
* git diff

__Let's talk about these...__

<h1>Git</h1>
We'll be using a version control system called git.  We'll also be using github to share code (though - github is <strong>distinct</strong> from git).

<ol>
<li>Create a [github.com](github.com) account if you do not have one; remember your username and password!</li>
<li>open terminal</li>
<li>change directory to Desktop
{% highlight bash %}
cd Desktop
{% endhighlight %}
</li>

<li>make a directory with your first initial and last name
{% highlight bash %}
# use your name to create a directory on the desktop
mkdir first_initial_last_name
{% endhighlight %}
</li>
<li>change directory to the one that you just created
{% highlight bash %}
cd jversoza
{% endhighlight %}
</li>
<li>log into github</li>
<li>
Create a new repository on github.  Call it processing_overview.
</li>
<li>get the http URL of your repository</li>
<li>in terminal,  make sure you're in the directory you just created
{% highlight bash %}
pwd
# should return /Users/professor/Desktop/your_directory_name_here/
{% endhighlight %}
</li>
<li>clone your newly created repository
{% highlight bash %}
git clone https://your_usrname@github.com/your_username/processing_intro.git
{% endhighlight %}
</li>
<li> change directory to the repository that you just checked out 
{% highlight bash %}
cd processing_overview
# should return /Users/professor/Desktop/your_directory_name_here/processing_overview
{% endhighlight %}
</li>
<li markdown="block">
__MAKE SURE YOU'RE IN YOUR REPOSITORY'S DIRECTORY__
{% highlight bash %}
pwd
{% endhighlight %}
</li>
<li>set your username (first initial, last name works)
{% highlight bash %}
# Note that this info is publicly available, so make sure you use a user name you're available
git config user.name "your_username"
{% endhighlight %}
</li>
<li> set your email
{% highlight bash %}
# Note that this info is publicly available, so take care to use an appropriate email address! 
git config user.email "your_email@citytech.cuny.edu"
{% endhighlight %}
</li>
</ol>
<h2>Committing Your Work:</h2>
<ol>
<li>Using terminal, move the folder on your Desktop in mtec1002-lab04 into the folder that you created from cloning (Desktop/your_directory_here/processing_overview)
</li>
<li> change to the processing_overview directory
</li>
<li>run git status
{% highlight bash %}
git status
{% endhighlight %}
</li>
<li>run git add
{% highlight bash %}
git add -a
{% endhighlight %}
</li>
<li>commit your code
{% highlight bash %}
git commit -m "my initial commit"
{% endhighlight %}
</li>
</ol>
<h2>Sending Your Work to github:</h2>
<ol>push your work to github
<li>
{% highlight bash %}
git push
{% endhighlight %}
You should see something like...
{% highlight bash %}
Password for 'github.com': 
Counting objects: 5, done.
Delta compression using up to 16 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 397 bytes, done.
Total 3 (delta 1), reused 0 (delta 0)
...
{% endhighlight %}
</li>
</ol>

* check github to see your code!
* try making a change


