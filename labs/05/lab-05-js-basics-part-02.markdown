---
layout: lab
title: JavaScript Basics
prefix: ../../
---
# Lab 5 - Part 2 - JavaScript Values, Types, Operations, Variables, Calling Functions, and Input/Output

In this lab, you'll be creating a few programs:

1. greetings
2. madlibs and madlibs with prompt
3. temperature
4. miles
5. \*numbers
6. \*print a tree

## Instructions

### Setup

Check your local repository, and start up SublimeText.

* open terminal
* go to your repository folder: __/Users/joe/Desktop/jversoza/lab-05-javascript/__
* once you're in it, check if your repository exists by using git status:
* you should get back:
{% highlight bash %}
# On branch master
#
# Initial commit
#
nothing to commit (create/copy files and use "git add" to track)
{% endhighlight %}
* open up SublimeText

<hr>

### greetings

* using SublimeText, create a new file called __greetings.html__ in your repository directory: __~/Desktop/jversoza/lab-05-javascript/__
* setup an html file, and add script tags... start writing your JavaScript between the script tags
* ask the user for their name
* save that input in a variable
* print out to the JavaScript console "Hi (name that the user entered)!"
* save your file in SublimeText
* use status, add commit and push to save your file in version control and submit it
* example interaction is below (everything after the greater than sign (&gt; is user input using the prompt function):
{% highlight bash %}
(prompt) What's your name?
> Joe
Hi Joe!
{% endhighlight %}

<hr>

### madlibs

Write a program that simulates MadLibs!  It will ask your for words, and then it will print out a story (in this case lyrics), with the user entered words substituted for words in the story.

Part 1

* using SublimeText, create a new file called __madlibs.html__ in your repository directory: __~/Desktop/jversoza/lab-05-javascript/__
* setup an html file, and add script tags... start writing your JavaScript between the script tags
* define 4 variables, set them each equal to a word: a noun, an adjective, an adverb and a verb
* name the variables after the part of speech of the word they are replacing, for example
{% highlight html %}
var noun = 'pizza';
var noun = 'ukulele';
{% endhighlight %}
* write program that __uses those 4 variables__ in these lyrics:
{% highlight bash %}
On a tropical island,
Underneath a molten lava moon.
Hangin' with the hula dancers,
Askin' questions cause' they got all the answers.
{% endhighlight %}
* substitute any words you'd like to change
* use string concatenation to stitch together the lyrics
* print out the new version of lyrics, each line on a separate line
* for example, the __JavaScript console__ may display:
{% highlight bash %}
On a tropical pizza,
Underneath a molten ...
{% endhighlight %}
* save your file in SublimeText
* use status, add commit and push to save your file in version control and submit it

Part 2

* modify your program so that it asks for user input for each variable (don't use hardcoded values anymore)
* this should result in 4 dialog boxes
* and the result of the new lyrics printed out to the __JavaScript console__
* save your file in SublimeText
* use status, add commit and push to save your file in version control and submit it

