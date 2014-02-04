---
layout: lab
title: Lab 12, Part 3 - Bootstrap
prefix: ../../
---

# Lab 12, Part 3 - Bootstrap

## Overview

* see what using a css framework like [bootstrap](http://twitter.github.io/bootstrap/) can help accomplish
* __we won't be forking and cloning another lab__; we'll be using the same repository as we did in part 1

## Instructions

### Prep Work

* in terminal 
* use pwd to make sure you're in your __~/Desktop/username/lab_12_part_1__ folder
* (we're using the same repository as we did in parts 1 and 2)
* if you're not in that folder, cd into it

### Revisiting Our Homepage

* 
* include bootstrap css to your index
{% highlight html %}
<link href="//netdna.bootstrapcdn.com/twitter-bootstrap/2.3.1/css/bootstrap-combined.min.css" rel="stylesheet">
{% endhighlight %}
* add a [div](http://www.htmldog.com/guides/html/intermediate/spandiv/) element around all of your content (that is write after body) and give it a class called container
{% highlight html %}
<div class='container'>
{% endhighlight %}
* refresh your page to see the changes
* use [bootrap components](http://twitter.github.io/bootstrap/components.html) to create navigation and other styles
* add two classes (called nav and nav-pills) to your first ul (your list of links); separate them with a space
{% highlight html %}
<ul class='nav nav-pills'>
{% endhighlight %}
* refresh your page to see the changes
* add a div element with class hero-unit around all of the content below the navigation list!
{% highlight html %}
<div class="hero-unit">
{% endhighlight %}
* refresh your page to see the changes
* use git __status__, __add__, and __commit__ to save your work
* ...then __push__ to __origin__ __gh-pages__
* check your __home page: 
	* open http://yourusername.github.io/lab\_12\_part\_1/ in your browser (replace yourusername with your actual username)
