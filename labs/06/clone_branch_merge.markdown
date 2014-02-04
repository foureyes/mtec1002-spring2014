---
layout: slides
title: MTEC1002 - Clone, Branch, Merge
---

<section markdown="block" class="title-slide">

# Clone, Branch Merge

{% include title-slide-footer.html %}
</section>

<section markdown="block">
### For Reference...

[Branching and Merging](http://git-scm.com/book/en/Git-Branching-What-a-Branch-Is)
[Clone](http://gitref.org/creating/#clone)
</section>

<section markdown="block">
### git clone

{% highlight bash %}
git clone http://some.url/repo.git
{% endhighlight %}

creates a local repository from a remote repository in the directory that you're in
</section>

<section markdown="block">
### git branch

{% highlight bash %}
git branch
{% endhighlight %}

lists all of the branches.  start denotes the branch that you're on.
</section>

<section markdown="block">
### git branch branchname

{% highlight bash %}
git branch branchname
{% endhighlight %}

create a branch with name branchname
</section>

<section markdown="block">
### git checkout branchname

{% highlight bash %}
git checkout branchname
{% endhighlight %}

switch to branch with name branchname
</section>

<section markdown="block">
### git merge branchname

{% highlight bash %}
git merge branchname
{% endhighlight %}

merge code from branch called branchname to current working branch
</section>
