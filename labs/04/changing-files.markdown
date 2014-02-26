---
layout: slides
title: MTEC1002 - Changing Files
---

<section markdown="block" class="title-slide">

# Making, Saving, and Sharing Changes

{% include title-slide-footer.html %}
</section>

<section markdown="block">
### git status

__git status__ - show what changes are ready to be committed as well as changes that you are working on in your working directory that haven't been staged yet

{% highlight bash %}
git status
{% endhighlight %}
</section>

<section markdown="block">
### git add

http://rogerdudler.github.io/git-guide/img/trees.png
__git add__ - mark a change to be staged

{% highlight bash %}
# in the directory of your repository

# add all
git add --all 

# add specific file
git add myfile.txt
{% endhighlight %}
</section>

<section markdown="block">
### git commit

__git commit__ - take a snapshot of your work

{% highlight bash %}
# in the directory of your repository
# don't forget the commit message

git commit -m 'commit message goes here'
{% endhighlight %}
</section>

<section markdown="block">
### git log

__git log__ - show commit history of your repository or file

{% highlight bash %}
# in the directory of your repository

git log
{% endhighlight %}
</section>

<section markdown="block">
### git diff

__git diff__ - show the line-by-line differences between your last commit and your working directory

{% highlight bash %}
# in the directory of your repository
# use --color for syntax highlighting

git diff --color
{% endhighlight %}
</section>

<section markdown="block">
### git reset

__git reset__ - revert last commit... or unstage changes
{% highlight bash %}
# unstage changes
git reset filename.txt

# revert last commit
git reset HEAD^
{% endhighlight %}
</section>

<section markdown="block">
### git push

__git push__ - send your code to a remote repository

{% highlight bash %}
# push master branch to remote repository called origin
git push origin master
{% endhighlight %}
</section>


<section markdown="block">
### Typical Workflow

1. make changes
2. git status
3. git add --all
4. git status
5. git commit -m 'my message'

(optionally... git push origin master to send to remote repository)
</section>

