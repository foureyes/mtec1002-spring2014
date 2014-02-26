---
layout: slides
title: MTEC1002 - Creating and Setting Up Local and Remote Repositories 
---

<section markdown="block" class="title-slide">

# Creating and Setting Up Repositories 

{% include title-slide-footer.html %}
</section>

<section markdown="block">
### Commands for Creation and Set Up of Repositories

For most of our work, we'll be creating a __local repository__ to work on in class and a __remote repository__ on github to submit our work.  Here are some commands we'll use:

* git init
* git config ...
	* git config user.name  "__your user name__"
	* git config user.email __your@email.address__
* curl -u '__your user name__' https://api.github.com/user/repos -d '{"name":"__repository name__"}'
* git remote add ...
</section>


<section markdown="block">
### git init

__git init__ - creates a new _local_ repository (using the files in the existing directory)

* you can tell a repository is created by running ls -l ... it creates a .git directory
* again, this creates a new repository - a place to archive / save all versions of your files

{% highlight bash %}
# in the directory of your repository
git init
{% endhighlight %}
</section>


<section markdown="block">
### git config

__git config__ - configure your user name and email for your commits 

* this has nothing to do with your computer's account or your account on github
* this information helps track changes

{% highlight bash %}
# in the directory of your repository
git config user.name  "foo bar baz"
git config user.email foo@bar.baz
{% endhighlight %}
</section>

<section markdown="block">
### Creating a Remote Repository


You can actually use github as a remote repository.  Here's how you create a remote repository on github through the commandline:

{% highlight bash %}
curl -u 'user name' https://api.github.com/user/repos -d '{"name":"repo"}'
{% endhighlight %}

* note that it uses our good friend, curl
* use your github user name to fill in user name
* the repository (repo) will be given in the instructions
* it'll ask you for a password (when you type in your password, the screen will not display what you type)
</section>

<section markdown="block">
### git remote add 

__git remote add__ - add a remote repository so that you can synchronize changes between it and your local repository

{% highlight bash %}
git remote add origin https://github.com/jversoza/my_new_lab.git
{% endhighlight %}

The last bit is the url to your repository on github
</section>

<section markdown="block">
## [All together now (part 01 of this lab)](lab-04-git-part-01.html)
</section>

<section markdown="block">
## [On to Changing and Saving Files](changing-files.html)
</section>
