---
layout: lab
title: Creating and Setting Up Git Repositories
prefix: ../../
---
# Lab 4 - Part 1 - Creating and Setting Up Git Repositories

In this lab, you'll be:

1. creating two repositories, one local and one remote
2. linking the two with each other so that they can be synchronized
3. associate a name and email address with your local repository


## Instructions

### Set up Your Local Repository

This will create a local git repository to store your work for this lab.  The repository will be in ~/Desktop/yourname/lab-04-version-control.

* open terminal
* create a folder that consists of your first initial and last name on your Desktop
{% highlight bash %}
cd ~/Desktop
mkdir myname
{% endhighlight %}
* within that folder, create another folder called __lab-04-version-control__ and change into it
{% highlight bash %}
cd myname
mkdir lab-04-version-control
cd lab-04-version-control
{% endhighlight %}
* use pwd to verify that you're in the correct folder
	* you should be in __~/Desktop/myname/lab-04-version-control__
	* if you're not, cd into it
* to prove that this is not yet a repository, list __all__ files in your current directory 
{% highlight bash %}
ls -al
{% endhighlight %}
* it should mostly be empty
{% highlight bash %}
total 0
drwxr-xr-x  2 joe  staff   68 Feb 26 07:52 .
drwxr-xr-x  3 joe  staff  102 Feb 26 07:52 ..
{% endhighlight %}
* in your lab-04 folder, create your repository!
{% highlight bash %}
git init
{% endhighlight %}
* it should say:
{% highlight bash %}
Initialized empty Git repository in /Users/joe/Desktop/jversoza/lab-04-version-control/.git/
{% endhighlight %}
* show that this worked by listing __all__ files in your current directory
{% highlight bash %}
ls -al
{% endhighlight %}
* check that this shows __.git__ 
* by the way, what's in that .git directory (use ls .git to take a peek)
* now... configure your user name and email for your commits (these do not have to be the same as your github account)
{% highlight bash %}
# in the directory of your repository
git config user.name  "my user name"
git config user.email "my@email.address"
{% endhighlight %}
* finally, use git config again to see if this worked:
{% highlight bash %}
git config -l
{% endhighlight %}

### Create Your Remote Repository

This will create a remote git repository on github.  It will also link your local repository with this remote repository.  In order to submit your work, you will send your files / changes from your local repository to the remote repository on github.


* log in to github; you should see the list of repositories on the right	
![Repository List](../../resources/img/repos-screen.png)
* you should have 3 lab related repositories
* go back to terminal
* using the commandline, create a remote repository on github by using the command below...
* substitute your github username where it says "your github user name" (keep the single quotes, though.  this is lab-04-version-control (you can see that specified at the end of the command)
{% highlight bash %}
curl -u 'your github user name' https://api.github.com/user/repos -d '{"name":"lab-04-version-control"}'
{% endhighlight %}
* it should output a bunch of text!
{% highlight bash %}
Enter host password for user 'jversoza':
{
  "id": 17210769,
  "name": "lab-04-version-control",
  "full_name": "jversoza/lab-04-version-control",
  "owner": {
    "login": "jversoza",
	...
}
{% endhighlight %}
* refresh your page on github
* you should see the new repository added
* go back to terminal
* make sure you're in your local repository folder for __lab-04-version-control__
	* use __pwd__ to do this
	* you should be in __~/Desktop/yourname/lab-04-version-control__
	* if you're not in your lab folder, change your directory to it
* run this command to show that you have not linked your local repository to any remote repository yet
{% highlight bash %}
git remote -v show
{% endhighlight %}
* it should _do nothing_
* now, link your local repository to your remote repository on github by using git remote add (make sure to substitute your github username where it says "your user name")
{% highlight bash %}
git remote add origin https://github.com/your user name/lab-04-version-control.git 
{% endhighlight %}
* (alternatively, if you click on your repo you can see your remote repository's url on the lower right hand side of the page...)
![Repository List](../../resources/img/repos-url.png)
* to check that you've linked properly, run the following command again:
{% highlight bash %}
git remote -v show
{% endhighlight %}
* it should show origin ... and your repository url
{% highlight bash %}
origin	https://github.com/jversoza/lab-04-version-control.git (fetch)
origin	https://github.com/jversoza/lab-04-version-control.git (push)
{% endhighlight %}
