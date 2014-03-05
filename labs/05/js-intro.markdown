---
layout: slides
title: MTEC1002 - JavasCript
---

<section markdown="block" class="title-slide">

# Introducing JavaScript

{% include title-slide-footer.html %}
</section>

<section markdown="block">

### Let's Talk About

* What is __JavaScript__ _anyway_, and where have you seen it?
* Why are _we_ using JavaScript?
* The tools that we'll need for programming in JavaScript
* A quick JavaScript demo

</section>

<section markdown="block">

### A Book That You May Be Interested In

__Check out [Eloquent JavaScript](http://eloquentjavascript.net/) if you'd like to follow along with a book__.&rarr;

* it's a great JavaScript / intro to programming book
* the [online version](http://eloquentjavascript.net/contents.html) is free
* a lot of the material in the JavaScript portions of this class is based off of the [second edition of Eloquent JavaScript](http://eloquentjavascript.net/2nd_edition/)

</section>

<section markdown="block">
## Does anyone know what JavaScript is?

<aside>Or perhaps you've used it before!</aside>
</section>

<section markdown="block">
### JavaScript

* __JavaScript__ is a __widely used__, __high-level__ programming language that is __available on many platforms__
* __JavaScript__ and __Java__ are two entirely different programming languages
</section>

<section markdown="block">
###  Some History

Originally created in 1995 as a way to add interactivity (through programming) to web pages in __Netscape Navigator__!

<div markdown="block" class="img-container">
<img src="../../resources/img/netscape.gif" width="300" height="300">
</div>
</section>

<section markdown="block">
### Where is it Now?

__JavaScript is now a widely used programming language!__

* it's usage is ubiquitous; it's common to have _some_ JavaScript on a web page
* it's usage has gone beyond web page interactivity:
	* processing.js
	* server side language (node.js)
	* embedded scripting language (max/msp)
</section>

<section markdown="block">
### As Seen On...

Here are some particularly _awesome_ uses of JavaScript:

* [Khan Academy uses JavaScript/Process.js to teach computer science](https://www.khanacademy.org/cs/programming/variables/p/challenge-bucktooth-bunny)
* [Creative programming, user interface experimentation (hakim.se)](http://hakim.se/experiments)
* [Sophisticated interactivity on web pages (Interactive Ear)](http://www.amplifon.co.uk/interactive-ear/index.html)
* [Skifree.js!](http://basicallydan.github.io/skifree.js/)

\* (we're going to start off small, though)
</section>

<section markdown="block">
### It's a High Level Language

As compared to a low level language __what does being a high level programming language mean?__ &rarr;

<div class="incremental" markdown="block">
* __meant for humans to read and write__ (unlike machine language or assembly) 
* consequently, easier to read and write; closer to a __natural language__
* __abstracts away details of underlying machine__ (you don't have to know about _registers_, your CPU's instruction set, etc.)
* must be __compiled__ (translated) or __interpreted__ (translated _on-the-fly_) into a language that the computer can understand (such as machine language)
</div>
</section>

<section markdown="block">
### It's Available!

* it's available on every major browser (such as Chrome, Safari or Internet Explorer)
* not only are you able to run JavaScript, but... if you have a web browser and a text editor, you will be able to write JavaScript programs as well!
* __check out the JavaScript _console_ in Chrome__ &rarr;
* In Chrome: View &rarr; Developer &rarr; JavaScript Console
</section>

<section markdown="block">
##  (And Again) JavaScript is not Java!
</section>

<section markdown="block">
###  And We're Doing This Because?

__Why are we learning JavaScript?__ &rarr;

<div class="incremental" markdown="block">
* we need _something_ to put into version control
* some understanding of basic JavaScript will be helpful in other classes
* JavaScript is a __widely used__, __high-level__ programming language that is __available on nearly every platform__
* It's _fun_ (really!)
</div>
</section>

<section markdown="block">
### So, Let's Write Some JavaScript

* there are multiple ways to program in JavaScript, depending on what you're trying to build
* all of our JavaScript will be browser based so that we can use Chrome and Chrome's __JavaScript Console__
* we'll create files using a text editor, __SublimeText__
* we'll version our files using git

</section>

<section markdown="block">
### Clarification: Let's Write Some JavaScript for the Browser

* Because we're targetting Chrome's __JavaScript Console__ we'll be writing our JavaScript in web pages
* that means editing __.html__ files (with SublimeText)
* it's not good practice to have _actual_ JavaScript code interspersed with your html, but for our purposes of getting started it's ok
* __why do you think this is discouraged?__ &rarr;

<div class="incremental" markdown="block">
* you'll want to separate the logic of your program from its display
* having the two tangled makes it difficult to change one or the other
</div>
</section>

<section markdown="block">
### Our Tools

Again, we'll be using the following:

* __Chrome__ to run and debug our JavaScript programs; we'll use its __JavaScript console__
	* as a place to __output messages__ &rarr;
	* as an __error log__ &rarr;
	* as an __interactive shell__ &rarr;
* __SublimeText__ to edit JavaScript/html files 
</section>

<section markdown="block">
### A Few Steps

Our workflow for creating a JavaScript program will be:

* open __SublimeText__
* create an __.html__ file
* create script tags
* write your __JavaScript__
* debug with Chrome's __JavaScript console__
* ???
* profit (or _pass the course?_)

</section>

<section markdown="block">
### A Quick Example

__Let's check out a short JavaScript program.  Begin by...__ &rarr;

* creating opening a new file and saving it .html in SublimeText
* inserting some basic html (there are _snippets_ in SublimeText if you don't like typing... you can start with html, then tab (_of course_))

{% highlight html %}
<!DOCTYPE html>
<html>
<body>
</body>
</html>
{% endhighlight  %}
</section>

<section markdown="block">
### A Quick Example Continued

__Add some script tags.__ &rarr;

{% highlight html %}
<!DOCTYPE html>
<html>
<body>
<script>
var num = prompt("Please enter a number!");
for(var i = 0; i < num; i++) {
	console.log(i);
}
</script>
</body>
</html>
{% endhighlight  %}
</section>

<section markdown="block">
### A Quick Example Continued Some More

__What does this program do?__ &rarr;

{% highlight html %}
<!DOCTYPE html>
<html>
<body>
<script>
var num = prompt("Please enter a number!");
for(var i = 0; i < num; i++) {
	console.log(i);
}
</script>
</body>
</html>
{% endhighlight  %}

<div class="incremental" markdown="block">
* asks the user for a number
* counts from 0 up to that number
</div>
</section>

<section markdown="block">
## [That was fun, let's go back to some version control](git.html)
</section>
<!--
<section markdown="block">
### 
<div class="incremental" markdown="block">
{% highlight html %}
{% endhighlight  %}
</div>
</section>
-->
