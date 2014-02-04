---
layout: slides
title: MTEC1002 - Version Control With Git
---

<section markdown="block" class="title-slide">

# Version Control With Git

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

__Version control software__ allows you to record changes to a file or set of files over time so that you inpsect or even revert tospecific versions.__

* can be applied to any kind of file, but we're mostly using text files
* with version control, you can:
	* revert files or the entire project to a previous state
	* review changes made over time, and who made them
	* you can easily recover from accidentally breaking or deleting code
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

* __git__ - the distributed version control system that we're using
* __github__ - a website that can serve as a remote repository for your git project
* __repository__ - the place where your version control system stores the snapshots that you _save_
</section>

<section markdown="block">
### Some More Terminology

* __working copy__ - the version of the code that you're currently modifying / working on
* __stage__ - define the _changes_ that you'd like to commit
* __commit__ - save a snapshot of your work
* __diff_ - the line-by-line difference between two files or sets of files
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

1. make changes
2. git add --all
3. git commit -m 'my message'

(optionally... git push origin master to send to remote repository)
</section>

<section markdown="block">
### Submitting Assignments

Make sure to push your changes to github at least once to submit homework!
</section>

<section markdown="block">
### Let's Try...

* write a simple program that draws a square with no outline
* creating a repository locally
* making changes
* creating a remote repository
* pushing your project to the remote repository

</section>
