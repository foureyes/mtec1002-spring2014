---
layout: slides
title: Operations and Variables
---
<section markdown="block" class="title-slide">
# Operations and Variables
{% include title-slide-footer.html %}
</section>

<section markdown="block">
##  Operations on Strings and Numeric Types
</section>

<section markdown="block">
### int operations 
<aside>The Usual...</aside>

As you'd expect: addition, subtraction and multiplication &rarr;

* add - __+__ 
* subtract - __-__
* multiply __\*__
</section>

<section markdown="block">
### Division is Special

* the division operator is __/__
* __what do you think 5/2 gives__ &rarr;			
* __what type is the result?__ &rarr;

<div class="incremental" markdown="block">
{% highlight pycon %}
>>> 5/2
2.5
>>> type(5/2)
<class 'float'>
>>> 
{% endhighlight %}
</div>
</section>

<section markdown="block">
### We Don't Need No Decimal Points
<aside>Integer Division</aside>

* the integer division operator is __//__ (double forward slash)
* it will always give back an integer - for example 21//10 gives back 2
* if the result is a float, it will go to the nearest integer to the left of the number line!
* __what will 5//2 give back__
* __what will -5//2 give back__

<div class="incremental" markdown="block">
{% highlight pycon %}
>>> 5//2
2
>>> -5//2
-3
{% endhighlight %}
</div>
</section>

<section markdown="block">
### Modulus Operator (Remainder)
<aside>What's Left Over?</aside>
* the remainder operator is % (the percent symbol)
* __what would 5%2 give back?__ &rarr;

<div class="incremental" markdown="block">
{% highlight pycon %}
>>> 5%2
1
{% endhighlight %}
</div>
</section>

<section markdown="block">
### Exponentiation 
<aside>We NEED MORE STARS</aside>
* the exponentiation operator is __\*\*__ (two asterisks)
* __what do we get for 2**2__? &rarr;

<div class="incremental" markdown="block">
{% highlight pycon %}
>>> 2**2
4
{% endhighlight %}
</div>
</section>

<section markdown="block">
### Order of Operations
<aside>Too Many Operators!  What To Do First?</aside>

* as you would expect (remember PEMDAS?)
* __what does 12 + 10 / 5  give?

<div class="incremental" markdown="block">
{% highlight pycon %}
>>> 12 + 10 / 5
14.0
{% endhighlight %}

__BTW, what type did we get back?__

float! (division, even with integers, gives back floats)
</div>
</section>


<section markdown="block">
### ((Parentheses))
<aside>(I Use Them A Lot</aside>
* you can use parentheses to group expressions...
* this will affect odrer of operations
* __what will (6 + 4) * 5 return?__ &rarr;

<div class="incremental" markdown="block">
{% highlight pycon %}
>>> 12 + 10 / 5
14.0
{% endhighlight %}
</div>
</section>

<section markdown="block">
### You Could Always Use It As a Calculator
<aside>A Quick Activity</aside>

__Translate this formula__ &rarr;

* 9 divided by 5 * C + 32
* use 37 for C
* do you recognize the forumla?
</section>

<section markdown="block">
## str Operations
</section>

<section markdown="block">
### Multiplication!?
* the multiplication operator is __*__
* it returns a new string with the original string duplicated the number of times specified by the operand on the right side
* __what would "hey" * 3 return?__ &rarr;

<div class="incremental" markdown="block">
{% highlight pycon %}
>>> "hey" * 3
'heyheyhey'
{% endhighlight %}
</div>
</section>

<section markdown="block">
### String Concatenation
* use the __+__ to stitch together strings
* it's basically just adding strings together
* for example: print("this" + "knocked " + "my" + "socks" + "off") &rarr;
* why are the words all smashed together? 
* how would we fix it? 
* __let's try different types! - does it work?__ &rarr;
	* with an int? try: 3 + " blind mice" &rarr;
	* with a float?
	* what kind of error are we getting?
</section>

<section markdown="block">
### Let's Fix It!
<aside>Type Conversion...</aside>

You can change from one type to another using functions of the same name as the type.  Let's look at what autocomplete says about the following functions and demo them.  &rarr;

* __int__
* __str__
* __float__

A few notes:

* unlike print, these functions return a value!
* sometimes this is called __casting__.
</section>

<section markdown="block">
###And This Helps... How? 
__Let's fix our previous string concatenation__ &rarr;

{% highlight pycon %}
3 + " blind mice"
{% endhighlight %}

<div class="incremental" markdown="block">

{% highlight pycon %}
>>> str(3) + " blind mice"
'3 blind mice'
{% endhighlight %}
</div>
</section>

<section markdown="block">
### Review
* what operators do we use for exponentiation and integer division?
* what does -10//3 give back?
* what's an easy way of creating a string that has 100 exclamation points in it? 
* what's string concatenation?
</section>


<section markdown="block">
## Variables
</section>

<section markdown="block">
### What's a Variable?
* __variable__ - name that refers to a value
* this terminology is important; very specific... __name__ and __value__
* we can now use that name instead of the explicit value
* sometimes you'll hear me say the string "literal" - representation of a value within a program... i mean... the thing in quotes
</section>

<section markdown="block">
### So How Do Variables Actually Work?
{% highlight pycon %}
some_variable_name = "a value"
{% endhighlight %}

* this is an __assignment statement__ - binds a value to a name
* the equals sign __assignment token__ - the "operator" that we use to bind a name to a value
	* name on left
	* value on right
	* eeezy.... just like maths
</section>

<section markdown="block">
### Another Aside - Interactive Shell
Whenever you type something in the interactive shell, it will always return a value. &rarr;

* a value returns a value
* a variable returns a value
* a function can return a value
* if a function doesn't actually return a value, like print, the resulting value will be None (NoneType)
</section>

<section markdown="block">
### Some More Miscellaneous Comments
* how can I tell if it printed something vs just return?
	* kind of confusing... strings, you can tell... because it shows a representation of the value that's returned
	* well, almost every line returns a value... unless it starts a new block of code (with a colon) or it's a continued line.
* another btw,__metasyntactic variable__ - typical to use foo, bar, baz as placeholders for real values - meant to represent arbitrary name
</section>

<section markdown="block">
### Variables That Aren't Defined Yet
* __what happens when you use a variable that doesn't exist?__ &rarr;	

<div class="incremental" markdown="block">
{% highlight pycon %}
>>> foo
Traceback (most recent call last):
  File "<pyshell#0>", line 1, in <module>
    foo
NameError: name 'foo' is not defined
>>> 
{% endhighlight %}
</div>
</section>

<section markdown="block">
### More About Reassignment

* you can reassign or rebind
* __let's see that in action__ &rarr;
{% highlight pycon %}
>>> a = 23
>>> a
23
>>> a = "foo"
{% endhighlight %}
</section>

<section markdown="block">
### Naming Variables
* you can make them as long as you want... though I suppose it could crash your computer
	* __what's an easy way to create a long variable name?__ &rarr;
	* __btw, you can autocomplete in the shell by using tab__ &rarr;
* names can only be alphanumeric (numbers and letters) or the underscore
* the first character has to be a letter or an underscore
* __case sensitive__ - case matters
* the name can't be a keyword or reserved word
</section>

<section markdown="block">
### Am I a Valid Name?
* _foo
* 1_foo
* foo
* 1foo
* $foo
* foo$
</section>

<section markdown="block">
### Let's Actually Use Some Variables
* exclaim = "!!!" 
* add a string to a variable that has a string in it
* 9 / 5 * c + 32
* let's convert 37...
</section>

<section markdown="block">
### Silly Tricks
* multiple assignment
* swapping values
</section>

