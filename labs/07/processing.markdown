---
layout: slides
title: MTEC1002 - Processing
---

<section markdown="block" class="title-slide">

# Processing

{% include title-slide-footer.html %}
</section>

<section markdown="block">
### So, I Lied; We Need to Know Some Programming

So... we'll start from the ground up.  

I already did a quick preview of processing, but now, we'll go into it in-depth.
</section>

<section markdown="block">
### Documentation / Reference

* processing documentation...
* two ways to access
	* online reference: [http://processing.org/reference/](http://processing.org/reference/)
	* highlight (may or may not work for you!)
</section>

<section markdown="block">
### Boilerplate Code

What do we write for every processing program?

<div class="incremental">
{% highlight bash %}
void setup() {
}

void draw() {
}
{% endhighlight %}
</div>
</section>

<section markdown="block">
### Statements and Comments


* Statements are basically instructions for the computer; they make up a program.  Statements end in a semicolon (;).
* anything that requires curly braces does not need a semicolon (void draw() for example)
* comments are notes embedded within code that have no effect on the program; they start with //

[http://processing.org/learning/basics/statementscomments.html](http://processing.org/learning/basics/statementscomments.html)
</section>

<section markdown="block">
### Curly Braces

{} denote the start and end of a block of code

</section>

<section markdown="block">
### Function Calls

There are some built-in function that we call in processing.  Functions require parentheses and an optional list of arguments.  For example:
{% highlight java %}
// rect is the function
// 0, 0, 50, 50 are all arguments or parameters
rect(0, 0, 50, 50);
{% endhighlight %}
</section>

<section markdown="block">
### Math

Processing supports the usual mathematical operations
{% highlight java %}
* __\*__ - multiply
* __/__ - divide
* __+__ - add
* __-__ - subtract
* __%__ - modulo (remainder)
{% endhighlight %}
</section>

<section markdown="block">
### Variables

* variables hold a value
* starts with a type (right now, we just know int for integer)
* variable name is on the left
* value or _expression_ is on the right
* ends with semicolon
{% highlight java %}
int x = 12;
{% endhighlight %}
</section>

<section markdown="block">
### Variables Continued

* you can reassign variables
* you can assign variables to an _expression_
	* using other variables as values
* where to define variables
* built-in
	* width
	* height
</section>

<section markdown="block">
### Some Functions That We Know

What are some functions that we know?

<div class="incremental">
{% highlight java %}
* rect
* ellipse
* background
* size
* fill
* stroke
* noStroke
{% endhighlight %}
</div>
</section>

