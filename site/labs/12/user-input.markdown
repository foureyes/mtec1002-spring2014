---
layout: slides
title: User Input (CSCI-UA.0002-006 - Spring 2013 - Slides)
---

<section markdown="block" class="title-slide">
# User Input
{% include title-slide-footer.html %}
</section>

<section markdown="block">
### Getting Input From the Shell

* we can prompt the user through the console / terminal / shell / command prompt
* the user enters input through the same mechanism
</section>

<section markdown="block">
### The input() Function
* what parameter's does it take? &rarr;
* what does it return? &rarr;
* what if the user input is a number? &rarr;

<div class="incremental" markdown="block">
* input takes one parameter - the prompt that is displayed
* it returns a string representing the user's input
* it will always return a string - even if the user inputs a number
</div>
</section>

<section markdown="block">
### Let's Try Some Examples of input()
{% highlight python %}
>>> s = input(">")
>foo
>>> type(s)
<class 'str'>
>>> x = input(">")
>5
>>> type(x)
<class 'str'>
>>> x = int(input(">"))
>5
>>> type(x)
<class 'int'>
{% endhighlight %}

</section>

<section markdown="block">
### Write a Program That Asks For a Name
Here's the sample output; the text after the &gt; is user input.

{% highlight python %}
What's your name?
>Joe
Hi Joe
{% endhighlight %}
<div class="incremental" markdown="block">
__A potential solution...__ &rarr;

{% highlight python %}
print("What's your name?")
name = input(">")
print("Hi %s" % name)
{% endhighlight %}
</div>
</section>

<section markdown="block">
### Write a Program That Adds Exclamation Points
Here's the sample output; the text after the &gt; is user input.

{% highlight python %}
How loudly?
>4
This is really loud!!!!
{% endhighlight %}
<div class="incremental" markdown="block">
__A potential solution...__ &rarr;

{% highlight python %}
loudly = input("How loudly?\n>")
print("This is really loud" + "!" * int(loudly))
{% endhighlight %}
</div>
</section>

<section markdown="block">
### Review
* what's the idiomatic way of swapping values in Python?
* how do we get user input?
* when we get input, what's the type of the value that's returned?
</section>

<section markdown="block">
## [A Whirlwind Tour of Conditionals](conditionals.html)
</section>
