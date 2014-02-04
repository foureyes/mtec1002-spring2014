---
layout: slides
title: MTEC1002 - Git and Processing
---

<section markdown="block" class="title-slide">

# Version Control With Git, Using Processing

{% include title-slide-footer.html %}
</section>

<section markdown="block">
### Version Control With Git

The material in these slides was sourced from:

* [gitref.org](http://gitref.org/)
* [pro git](http://git-scm.com/book/en/Getting-Started-About-Version-Control)
</section>

<section markdown="block">
### What's Version Control?

<div class="incremental" markdown="block">
* __Version control software__ allows you to record changes to a file or set of files over time so that you inpsect or even revert tospecific versions.
* think of it as software that let's you take snapshot of your work
* or keeping track of all of the changes to your files
</div>
</section>

<section markdown="block">
### Why Use Version Control?

<div class="incremental" markdown="block">
* with version control, you can:
	* revert files or the entire project to a previous state
	* review changes made over time, and who made them
	* you can easily recover from accidentally breaking or deleting code
* we can version any kind of file, but we're mostly using text files
</div>
</section>

<section markdown="block">
### Three Kinds of Version Control

What are they?  Which one are we using?

<div class="incremental" markdown="block">
* local
* centralized
* distributed
* we're using git
</div>
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
### What's the Difference Between git and github?

<div class="incremental" markdown="block">
* git is the version control software that we're using
* (__let's talk a little bit about git &rarr;__)
	* free and open source
	* Linus Torvalds
* github is a web site that can be used as a remote git repository or central repository
</div>
</section>

<section markdown="block">
### Uh.  So What's a Repository?

<div class="incremental" markdown="block">
* __repository__ - the place where your version control system stores the snapshots that you _save_
* think of it as the data store where all the historical versions of your files are located
</div>
</section>

<section markdown="block">
### What's Your Working Copy and Staging Area?

<div class="incremental" markdown="block">
* __working copy__ - the version of the code that you're currently modifying / working on
* __stage__ - define the _changes_ that you'd like to commit
</div>
</section>

<section markdown="block">
### What's a Commit?  What's a diff?

<div class="incremental" markdown="block">
* __commit__ - save a snapshot of your work
* __diff__ - the line-by-line difference between two files or sets of files
</div>
</section>

<section markdown="block">
### What Are the Commands That We Learned?

<div class="incremental" markdown="block">
* git init
* git config
* git add
* git commit
* git log
* git diff
* git reset
* git add remote
* git push
</div>
</section>

<section markdown="block">
### git init

init - create a repository from the existing directory of files

"you use git init to make an existing directory of content into a new Git repository...", can be completely locally

{% highlight java %}
# in the directory of your repository
git init
{% endhighlight %}
</section>

<section markdown="block">
### git config

config - configure your user name and email for your commits

{% highlight java %}
# in the directory of your repository
git config user.name  "foo bar baz"
git config user.email foo@bar.baz
{% endhighlight %}
</section>

<section markdown="block">
### git add

add - mark a change to be staged

{% highlight java %}
# in the directory of your repository

# add all
git add --all 

# add specific file
git add myfile.txt
{% endhighlight %}
</section>

<section markdown="block">
### git commit

commit - take a snapshot of your work

{% highlight java %}
# in the directory of your repository
# don't forget the commit message

git commit -m 'commit message goes here'
{% endhighlight %}
</section>

<section markdown="block">
### git log

log - show commit history of your repository or file

{% highlight java %}
# in the directory of your repository

git log
{% endhighlight %}
</section>

<section markdown="block">
### git diff

diff - show the line-by-line differences between your last commit and your working directory

{% highlight java %}
# in the directory of your repository
# use --color for syntax highlighting

git diff --color
{% endhighlight %}
</section>

<section markdown="block">
### git reset

reset - revert last commit... or unstage changes
{% highlight java %}
# unstage changes
git reset filename.txt

# revert last commit
git reset HEAD^
{% endhighlight %}
</section>

<section markdown="block">
### git push

push - send your code to a remote repository

{% highlight java %}
# push master branch to remote repository called origin
git push origin master
{% endhighlight %}
</section>

<section markdown="block">
### git remote add 

remote add - add a remote repository

{% highlight java %}
git remote add origin https://github.com/foureyes/lab_5_processing_shapes.git
{% endhighlight %}
</section>

<section markdown="block">
### Typical Workflow

__You'll be doing this often!__

1. (if it's not created) create a repository
2. work on code
3. add changes you want to be saved
4. optionally... check the status of your working directory, check on the changes you've made
5. optionally... at any point in time, if you have a remote repo associated, you can push
</section>

<section markdown="block">
### Typical Workflow

And the actual translation to commands (you'll repeat #3, #4, and #5 a lot)

1. (if you don't have a repository yet) git init
2. (make changes)
3. git add --all 
4. git commit -m 'my message'
5. (optionally throughout) git status
6. (optionally...) git push origin master)
</section>
<section markdown="block">
### Follow Along

* some setup
	* open terminal
	* delete mtec folders
	* delete your folder, etc.
	* create a new folder: 1st initial last name
</section>
<section markdown="block">
### A Repository and a Program

* create a local repository in a directory called lab_6_review
* create a new sketch
* draw a square - 40 by 40 somewhere near the center, 400 by 400 should be size 
* call it lots_of_squares
* save it in lab 6 review... you can save the folder rather the file
* run status
* add and commit
* now... add color to your square
* status, diff and commit with message about color
</section>

<section markdown="block">
### More Program!

* now draw 10 of those squares using a for loop
* status, diff and commit with message for loop
* now check the log...
* now... if a square is the 5th one from the top, make it a different color
* status, diff and commit with message for loop
* now check the log...
</section>

<section markdown="block">
### Remote Repositories

* ok... that's great.  what if you want to share... or you're at lab computer and you want save elsewhere
* we'll use github
* create a repository - pretend that it's doing a git init on their server
* take the url, cp and paste it for the next step
* remote add a repo... origin is name of repo, branch will usually  be master
* push
</section>

<section markdown="block">
### Processing Review

* rect
* elipse	
* variables
* for loop
* if statements
</section>

<section markdown="block">
### Lines and strokeWeight

* line(x1, y1, x2, y2)
* strokeWeight(diameter)
</section>
