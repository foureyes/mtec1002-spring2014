---
layout: slides
title: MTEC1002 - Version Control 
---

<section markdown="block" class="title-slide">

# Version Control

{% include title-slide-footer.html %}
</section>


<section markdown="block">
### Version Control (With Git)

The material in these slides was sourced from:

* [gitref.org](http://gitref.org/)
* [pro git](http://git-scm.com/book/en/Getting-Started-About-Version-Control)
* [git - the simple guide](http://rogerdudler.github.io/git-guide/)
</section>

<section markdown="block">
### Um.  First... Archiving?

__What are some ways you've used to keep / save different versions of files?__ &rarr;

<div class="incremental" markdown="block">
* adding a date to a file name?
* adding extensions to files, like .bak?
* organizing copies by folders?
* ...perhaps folders with timestamps / dates
* ummm... etc.

__What are some drawbacks of these methods of saving versions of files?__ &rarr;

* it's all manual 
* ... and, consequently, tedious and error prone
</div>
</section>

<section markdown="block">
### Sharing / Collaborating

Have you ever worked on a programming project with more than one person?  __How did you share your code?__ &rarr;

<div class="incremental" markdown="block">
* email?
* usb?
* dropbox?

__What are some issues with these methods (well, except for dropbox)?__

* hard to find a specific version
* which one is the latest?
* how do you deal with conflicting changes?
</div>
</section>

<section markdown="block">
## Enter: Version Control
</section>

<section markdown="block">
### What's Version Control?

__Version control software__ allows you to record changes to a file or set of files over time so that you can inspect or even revert to specific versions.

* can be applied to any kind of file, but we're mostly using text files
* with version control, you can:
	* leave __comments__ on changes that you've made
	* __revert__ files to a previous state
	* __review__ changes made over time, and track __who__ made them
	* __you can easily recover from accidentally breaking or deleting code__
	* automatically __merge__ changes to the same file
</section>

<section markdown="block">
### So... Um.  Why?

<aside>What does this all mean?</aside>  

Version control can help us:

* stop using .bak files!
* collaborate with others 
	* share our code
	* merge changes from different sources
* document our work
* group related changes
</section>

<section markdown="block">
## Oh.  And it's kind of _expected_ that you know this as a professional programmer.
</section>

<section markdown="block">
###  We’re Using git!

* __git__ is the version control system that we're using
* it’s a __modern distributed version control__ system
* it has emerged as __the standard__ version control system to use
* (some others are...)
	* mercurial
	* subversion (svn)
	* cvs
</section>

<section markdown="block">
### A Bit About Git

It was developed by Linus Torvalds... __who?__ &rarr;

<div markdown="block" class="img-container">
![Linux](../../resources/img/linus-torvalds.jpg)
</div>

<div class="incremental" markdown="block">
(the guy who made [Linux](http://en.wikipedia.org/wiki/Linux))
</div>
</section>

<section markdown="block">
## By the way, does the name, git, sound familiar?  Where have seen it before?

</section>
<section markdown="block">
### Github vs git

__GIT AND GITHUB ARE DIFFERENT!__ 

* so... we used github to submit assignments
* __github is a website__ that hosts git repositories
* on it's own __git is just version control__

</section>

<section markdown="block">
### Who Uses Git and Github?

Git is used to maintain a variety of projects, like:

* the [Processing IDE](https://github.com/processing/processing)
* or [Twitter's Bootstrap](https://github.com/twbs/bootstrap)
* or [Ruby on Rails](https://github.com/rails/rails)

Some people use github to distribute open source code... for example:

* __id software__ has a bunch of [stuff hosted on git](https://github.com/id-Software)
</section>

<section markdown="block">
### Local Version Control

[See the diagram on pro git](http://git-scm.com/book/en/Getting-Started-About-Version-Control)

* equivalent to what we may have done manually:
	* save files in folder with locally as a _snapshot_ of current state of code
	* recover by going through folders on computer
	* see versions by the timestamped folder name
* all of this is automated through software
	* stores changes to your files in a local database
	* an example of local version control is RCS

</section>

<section markdown="block">
### Centralized Version Control

[See the diagram on pro git](http://git-scm.com/book/en/Getting-Started-About-Version-Control)

* promoted collaboration; everyone got code from the same place
* single server that has all of the versioned files
* everyone working on it had a _working copy_, but not the full repository
* an example is subversion (SVN)

</section>

<section markdown="block">
### Distributed Version Control

[See the diagram on pro git](http://git-scm.com/book/en/Getting-Started-About-Version-Control)

* everyone has full repository
* can connect to multiple __remote__ repositories 
* can push and pull to individuals, not just _shared_ or _centralized_ servers
* single server that has all of the versioned files
* everyone working on it had a _working copy_

</section>

<section markdown="block">
## We're Using Git, a Distributed Version Control System

</section>


<section markdown="block">
### Some Terminology

__repository__ - the place where your version control system stores the snapshots that you _save_

* think of it as the place where you store all previous/saved versions of your files
* this could be:
	* __local__ - on your computer
	* __remote__ - a copy of versions of your files on another computer
</section>

<section markdown="block">
### Some More Terminology

* __git__ - the distributed version control system that we're using
* __github__ - a website that can serve as a remote _repository_ for your project

__What's a remote repository again?__ &rarr;

<div class="incremental" markdown="block">
A copy of versions of your files on another computer.
</div>
</section>

<section markdown="block">
### Where Are My Files

In your __local repository__, git _stores_ your files and versions of your files in a few different _conceptual_ places:

* __the working directory / working copy__ - stores the version of the files that you're currently modifying / working on
* __index__ - the staging area where you put stuff that you want to _save_ (or... that you're about to _commit_)
* __HEAD__ - the most recent saved version of your files (or... the last _commit_ that you made)
</section>

<section markdown="block">
### Another Way to Look at It


* __the working directory / working copy__ - stuff you've changed but haven't saved
* __index__ - stuff that you're about to save
* __HEAD__ - stuff that you've saved
</section>

<section markdown="block">
### Aaaaand.  More Terminology.

* __commit__ - save a snapshot of your work
* __diff__ - the line-by-line difference between two files or sets of files
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
### Ok.  Great!

__Remind me again, what's github?__ &rarr;

* __github is a website__ 
* it can serve as a __remote git repository__
	* that means it can store all versions of your files
	* (after you've sent changes to it)
</section>

<section markdown="block">
## We can now submit assignments using the commandline
</section>


<section markdown="block">
### Submitting Assignments

* we will continue to use github to submit assignments
* however, instead of using the web interface and copying and pasting ...
* we can use a combination of git commands to send files to github
</section>

<section markdown="block">
## [Let's Start Off With Creating Repositories](creating-repositories.html)
</section>
