---
layout: slides
title: MTEC1002 - Control
---

<section markdown="block" class="title-slide">

# Variables and Control Structures

{% include title-slide-footer.html %}
</section>

<section markdown="block">
### Variables

Variables are like a buckets that we put a value in.

{% highlight java %}
int x = 0;
{% endhighlight %}
</section>

<section markdown="block">
### Types

Types are the class or kind of value/data that we're dealing with.  Right now, we'll only deal with a primitive type called int.  int represents an integer.  Whenever you declare a variable you have to specify its type.  Consequently:

{% highlight java %}
int x = 0;
{% endhighlight %}
</section>

<section markdown="block">
### Conditionals

Conditionals allow branching of code.  Use comparison operators to compare values (even variables!):

* == - equals
* != - not equals
* &gt;, &gt;= - greater than or greater than equal
* &lt;, &lt;= - less than or less than equal

{% highlight java %}
x = 0;
if (x < 5) {
	print("less than five);
} else {
	print("greater than five);
}
{% endhighlight %}
</section>

<section markdown="block">
### For Loops

for loops allow you to repeat a block of code for a specific number of times.

{% highlight java %}
for(int i = 0; i < 10; i++) {
	println(i);
}
{% endhighlight %}
</section>

<section markdown="block">
### For Loops Continued

* keyword __for__, open parens
* start value and variable, semicolon
* end condition, semicolon
* incrementor, close parens


{% highlight java %}
for(int i = 0; i < 10; i++) {
	println(i);
}
{% endhighlight %}
</section>

<section markdown="block">
### Follow Along

* a square w/ x and y set as variables
* two squares w/ x and y set as variables
* two circles w/ x and y set as variables
* a vertical line of circles, alternating color (use a for loop)
</section>


<section markdown="block">
## [Drawing More Stuff](draw_more_stuff.html)
</section>
