---
layout: slides
title: MTEC1002 - Version Control Review
---

<section markdown="block" class="title-slide">

# Version Control Review

{% include title-slide-footer.html %}
</section>




<section markdown="block">
### Version Control - Definition

__What's version control?__ &rarr;

<div class="incremental" markdown="block">
__Version control software__ allows you to record changes to a file or set of files over time. With version control, you can:

* __revert__ files to a previous state
* __review__ changes made over time, and track __who__ made them
* leave __comments__ on changes that you've made
* __you can easily recover from accidentally breaking or deleting code__
* automatically __merge__ changes to the same file
</div>
</section>

<section markdown="block">
### Motivation

__Why would we use version control?__ (besides being required for this course, obvs!) &rarr;


<div class="incremental" markdown="block">
* have an automatic archive / stop manually backing up files
* make sharing and collaborating with others easier
* it's expected that you know this as a professional programmer
* document your work
</div>

</section>

<section markdown="block">
### Tools

__What version control software are we using?__ &rarr;

<div class="incremental" markdown="block">
* __git__ is the version control system that we're using
* it’s a __modern distributed version control__ system
* it has emerged as __the standard__ version control system to use
* (it was developed by Linus Torvalds, the guy who created Linux!)
</div>
</section>

<section markdown="block">
### Some Potential Confusion

__What's the difference between git and github__ &rarr;

<div class="incremental" markdown="block">
* __git is just version control__
* __github is a website__ that hosts git repositories
* we'll be using __git__ to submit our assignments by posting them to __github__
</div>

</section>



<section markdown="block">
### More Definitions...

Define the following terms: __repository__, __local repository__, __remote repository__, __git__ and __github__

<div class="incremental" markdown="block">

* __repository__ - the place where your version control system stores the snapshots that you _save_
* __local repository__ - the repository on your computer
* __remote repository__ - a copy of versions of your files on another computer
* __git__ - the distributed version control system that we're using
* __github__ - a website that can serve as a remote _repository_ for your project
</div>
</section>

<section markdown="block">
### And Even More Definitions....

Define the following terms: __commit__ and __dif__ &rarr;

<div class="incremental" markdown="block">

* __commit__ - save a snapshot of your work
* __diff__ - the line-by-line difference between two files or sets of files
</div>
</section>

<section markdown="block">
### Where Are My Files

In your __local repository__, git _stores_ your files and versions of your files in a few different _conceptual_ places:

* __the working directory / working copy__ - stuff you've changed but haven't saved
* __index__ - stuff that you're about to save (staging area)
* __HEAD__ - stuff that you've already saved
</section>


<section markdown="block">
### Two Basic Workflows

1. Creating and setting up local and remote repositories
2. Making, saving, and _sharing_ changes
</section>

<section markdown="block">
### Creating Repositories

* create a local repository
* configure it to use your name and email (for tracking purposes)
* create a remote repository
* _link_ the two
</section>

<section markdown="block">
### Making, Saving, and Sharing Changes

* make changes
* put them aside so they can staged for saving / committing
* save / commit
* send changes from local repository to remote repository
</section>

<section markdown="block">
### Github Will Serve as our Remote Repository

* __github is a website__ 
* it stores __git__ repositories
	* that means it can store all versions of your files
	* (but only after you've sent changes to it)
</section>

<section markdown="block">
## ALL ASSIGNMENTS ARE REQUIRED TO BE SUBMITTED VIA COMMANDLINE!
</section>


<section markdown="block">
### git

* git works via the commandline
* the base command is __git__ followed by a specific action
* these commands/actions only work when __you're in a git repository__
* (that is, you have to cd to the directory that contains your repository)

</section>
<section markdown="block">
### Commands for Setting Up Local Repositories...

__How do you create a local repository?__ &rarr;

<div class="incremental" markdown="block">
{% highlight bash %}
git init
{% endhighlight %}

__How do you configure your local repository with your name and email address?__ &rarr;

{% highlight bash %}
git config user.name "your name"
git config user.email "your@email.address"
{% endhighlight %}
</div>

</section>

<section markdown="block">
### Commands for Setting Up Remote Repositories...

__How do you create a remote repository?__ &rarr;

<div class="incremental" markdown="block">
{% highlight bash %}
# for github, you can use curl!
# replace 'your github user name' with your username
# replace 'your repository name' with the name you'd like to call your repository
# keep EVERYTHING ELSE as is
curl -u 'your github user name' https://api.github.com/user/repos -d '{"name":"your repository name"}'
{% endhighlight %}

__How do you link your local and remote repository?__ &rarr;

{% highlight bash %}
# replace "your username" and "the url to your repository" appropriately 
# (keep the @ symbol... it means... your user, at that web site)
git remote add origin "your username"@"the url to your repository"
{% endhighlight %}
</div>
</section>

<section markdown="block">
### Summary for Setting Up and Linking Remote and Local Repositories

{% highlight bash %}
git init
git config user.name  "your user name"
git config user.email "your@email.address"
curl -u 'your github user name' https://api.github.com/user/repos -d '{"name":"your repository name"}'
git remote add origin "your username"@"the url to your repository"
{% endhighlight %}
</section>


<section markdown="block">
### Working With Your Files

__What's the typical workflow for changing and saving your files using version control?__ &rarr;

<div class="incremental" markdown="block">

1. make changes
2. git diff --color (show your changes)
3. git status (to see the status of your changes)
4. git add --all (to stage your changes for committing)
5. git status (to see your staged changes)
6. git commit -m 'my message' (to save your changes)
7. git log --color (show your changes so far)
8. git push origin master (optionally send/share your changes to a remote repository)
</div>
</section>

<section markdown="block">
### git status

__What does git status do?__ &rarr;

<div class="incremental" markdown="block">
__git status__ - show what changes are ready to be committed as well as changes that you are working on in your working directory that haven't been staged yet

</div>
</section>

<section markdown="block">
### git add

<div class="incremental" markdown="block">
__What does git add do?__ &rarr;

{% highlight bash %}
# it marks a file or files as ready to be saved

# add all
git add --all 

# add specific file
git add myfile.txt
{% endhighlight %}
</div>
</section>

<section markdown="block">
### git commit

__What does git commit do?__ &rarr;

<div class="incremental" markdown="block">
{% highlight bash %}
# git commit takes a snapshot of your work
# (it saves it!)

# in the directory of your repository
# don't forget the commit message
git commit -m 'commit message goes here'
{% endhighlight %}
</div>
</section>

<section markdown="block">
### git log

__What does git log do?__ 

<div class="incremental" markdown="block">
{% highlight bash %}
# git log shows you the commit history of your repository or file
git log

# you can also colorize the output:
git log --color
{% endhighlight %}
</div>
</section>

<section markdown="block">
### git diff

__What does git diff do?__ &rarr; 

<div class="incremental" markdown="block">

{% highlight bash %}
# it shows the line-by-line differences between your last commit and your working directory

# use --color for syntax highlighting
git diff --color
{% endhighlight %}
</div>
</section>

<section markdown="block">
### Summary for Working With Files


{% highlight bash %}
# make changes
# look at the differences between your last save and your current changes
git diff --color

# check on the status of your changes
git status

# "stage" or mark your changes as ready to be saved
git add --all

# check the status again to see that you changes are ready to be saved
git status

# save!
git commit -m 'my message'

# show a log of your changes so far
git log --color (show your changes so far)

# send to a remote repository (to submit an assignment)
git push origin master 
{% endhighlight %}
</section>


<section markdown="block">
## All git commands must be run in your repository directory (where you ran git init)
</section>
