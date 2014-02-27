---
layout: lab
title: Saving and Sending Changes to Your Repository
prefix: ../../
---
# Lab 4 - Part 2 - Saving and Sending Changes to Your Repository

In this lab, you'll be:

1. creating and editing files in your local repository
2. saving those changes
2. sending those changes to your remote repository on github


## Instructions

### Creating and Saving Changes Locally, Sending to Remote Repository

In this part of the lab, you will create a text file in your local repository, and then you'll send it to your remote repository.

* open terminal
* make sure you're in your local repository folder for lab-04-version-control
	* use __pwd__ to do this
	* you should be in __~/Desktop/yourname/lab-04-version-control__
	* if you're not in your lab folder, change your directory to it
	* if this doesn't exist yet... make sure you completed the [first part of this lab](lab-04-git-part-01.html)
* use __git status__ to show that there aren't any changes yet
{% highlight bash %}
git status
{% endhighlight %}
* it should give the following output
{% highlight bash %}
# On branch master
#
# Initial commit
#
nothing to commit (create/copy files and use "git add" to track)
{% endhighlight %}
* create a file called __README.markdown__
	* use touch to do this
* use __nano__ to edit __README.markdown__
{% highlight bash %}
nano README.markdown
{% endhighlight %}
* type in the following line
{% highlight bash %}
This is lab 04
{% endhighlight %}
* exit and save your file (&lt;ctrl-x&gt;,&lt;y&gt;,&lt;enter&gt;)
* use __git status__ to show that you've made changes
{% highlight bash %}
git status
{% endhighlight %}
* it should give the following output; notice that it contains README.markdown 
{% highlight bash %}
pines:lab-04-version-control joe$ git status
# On branch master
#
# Initial commit
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#	README.markdown
nothing added to commit but untracked files present (use "git add" to track)
{% endhighlight %}
* if we want to save this file in the repository, we have _stage_ it (that is, mark it as something that we're ready to save / commit)
{% highlight bash %}
git add --all
{% endhighlight %}
* to check that you've staged your commit, use __git status__ again
{% highlight bash %}
git status
{% endhighlight %}
* it should output the following text (note that README.markdown moved from _untracked_ to _Changes to be committed_)
{% highlight bash %}
# On branch master
#
# Initial commit
#
# Changes to be committed:
#   (use "git rm --cached <file>..." to unstage)
#
#	new file:   README.markdown
#
{% endhighlight %}
* now we're ready to commit (that is, save the file to the local repository); everything after the -m is the message that will be associated with the changes that you've made
{% highlight bash %}
git commit -m "added a README file"
{% endhighlight %}
* the output of the command should be:
{% highlight bash %}
[master (root-commit) 7a2e2f6] added a README file
 1 file changed, 1 insertion(+)
 create mode 100644 README.markdown
{% endhighlight %}
* check the status again 
{% highlight bash %}
git status
{% endhighlight %}
* notice that there is nothing staged and no more changes!
{% highlight bash %}
# On branch master
nothing to commit, working directory clean
{% endhighlight %}
* to show the changes that you've saved so far, use __git log__
{% highlight bash %}
git log --color
{% endhighlight %}
* it should show you the following...
{% highlight bash %}
commit 7a2e2f6ff86407b7707f78cf8c9a12b1dd843de9
Author: joe <jversoza@citytech.cuny.edu>
Date:   Wed Feb 26 08:54:14 2014 -0500

    added a README file
{% endhighlight %}
* you can share your changes / send them to a remote repository by using __git push__
{% highlight bash %}
git push origin master
{% endhighlight %}
* it should result in:
{% highlight bash %}
Counting objects: 3, done.
Writing objects: 100% (3/3), 242 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/jversoza/lab-04-version-control.git
 * [new branch]      master -> master
{% endhighlight %}
* go back to github and look in your repository.  you should see that file appear.
![Repository List](../../resources/img/repos-added.png)

### Making Changes, Showing Changes, Showing History

In this part of the lab, you will make changes to an existing file.

* add another line to your README.markdown
{% highlight bash %}
This is lab 04
It's about version control
{% endhighlight %}
* use git diff to show your changes
{% highlight bash %}
git diff --color
{% endhighlight %}
* use git status, add and commit to save your changes
* finally, use git push to send them to your remote repository
* check that they are in your folder


### (Optional) Practice Making Changes / Adding Files

* create another file called test.sh
{% highlight bash %}
echo "hello"
{% endhighlight %}
* save locally and push to your remote repository


