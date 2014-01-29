---
layout: slides
title: MTEC1002 - Git Workflow
---

<section markdown="block" class="title-slide">

# Git Workflow

{% include title-slide-footer.html %}
</section>

<section markdown="block">
### For the Remainder of Our Labs...

* you'll be using git to save your work
* you'll be using git and github accounts to submit your work
* I'll check your github accounts when I check your labs
</section>

<section markdown="block">
### General Workflow

* create a repository
	* git init
	* git config user.name "joe v"
	* git config user.email "joe@example.email"
* program!  ... and periodically save your work
	* git status
	* git add --all
	* git commit -m 'my commit message'
	* go back 
* create a remote repository on github
	* git remote add origin http://some.url/project.git
	* git push origin master
</section>

<section markdown="block">
### Workflow Continued

* in the labs, I mention that you should commit
* add and commit often, even if I don't explicitly say so in the labs (though it always comes at the end)
* you can wait to push last
</section>

<section markdown="block">
### Managing Multiple Projects

For each part in the lab we may have to:

* create a new repository to work on a __new__ project
* clone (copy) an existing repository to work on an __existing__ project
* note that anything in the __repository directory__ can potentially be tracked by git / version control
</section>

<section markdown="block">
### Processing and Git

* before you use git status, add and commit, make sure you save with processing!
* saving in processing and saving using git are different!
* see the saved marker
![unsaved](unsaved.png)
* note that depending on how you save (and possibly what version of processing you use), you may end up with:
	* a folder with your sketch's name with one file in it
	* or one pde file with your sketch's name
* either is fine
</section>

<section markdown="block">
### Cleaning Up

* It's usually a good idea to close your processing window as well as your terminal when moving on to the next part in a lab
* (processing doesn't automatically load stuff if your file changes outside of processing)
</section>
