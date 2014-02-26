---
layout: slides
title: MTEC1002 - Drawing
---

<section markdown="block" class="title-slide">

# Processing

{% include title-slide-footer.html %}
</section>

<section markdown="block">
### setup() and draw()

Processing programs always have this boiler plate code in it:

{% highlight java %}
void setup() {

}

void draw() {

}
{% endhighlight %}

* these are functions that you define
* you put your code in the spaces between the curl braces
* we'll talk about that more later...
</section>

<section markdown="block">
### Curly Braces

* represent a "block" of code
* or a group of code chunked together
* there's an opening and closing curl brace

</section>

<section markdown="block">
### setup()

* the code in the setup function gets run once
</section>

<section markdown="block">
### draw()

* the code in the setup function gets run repeatedly
</section>

<section markdown="block">
### Program Execution

1. Processing executes setup() exactly once
2. Processing executes draw()
3. Go back to #3 (_forever_ or until you close the program)
</section>

<section markdown="block">
### Statements

A __statement__ is a single line or instruction for Processing to execute.  

* the function __call__, rect() that we saw previously is a statement.
* __all statements must end in a semicolon!!!__

{% highlight java %}
// notice the semicolon!
rect(100, 100, 40, 40);
{% endhighlight %}
</section>

<section markdown="block">
### Calling Functions

Functions are named groups of code that can be executed by using the function's name.  Functions can:

* take values as inputs (optional)
* return values (optional)
* or have _side effects_, like drawing on the screen (optional)

You can call a function by using its name, open parens, a comma separated list of values, close parens... and a semicolon.
{% highlight java %}
// function name, parens, comma separated list of values
rect(100, 100, 40, 40);
{% endhighlight %}
</section>

<section markdown="block">
### size

* specifies the width and height of your window
* arguments are:
	* width in pixels
	* height in pixels
* usually is called in setup

{% highlight java %}
size(640, 480);
{% endhighlight %}
</section>

<section markdown="block">
### background

* paints the entire window with the color specified
* arguments are:
	* red component of color (0 to 255)
	* green component of color (0 to 255)
	* blue component of color (0 to 255)
* usually called in setup, but also called in draw when animating
{% highlight java %}
background(255, 0, 0);
{% endhighlight %}
</section>

<section markdown="block">
### comments

Comments are notes embedded within your code.  Processing doesn't execute these lines as statements... 
{% highlight java %}
// single line comments
/* block
comments */
{% endhighlight %}
</section>

<section markdown="block">
### print

* prints arguments to the console.  Use + to concatenate (_stitch together_) values.
* arguments are:
	* value to be printed out

{% highlight java %}
print('hello there' + '!!!!');
{% endhighlight %}
</section>

<section markdown="block">
### println

* prints arguments to the console, ends with a new line
* arguments are:
	* value to be printed out

{% highlight java %}
println(1);
println(2);
{% endhighlight %}
</section>

<section markdown="block">
### Usual Operators

()'s, +, -, /, * ... and % (modulo or remainder... can be used to determine even or od).
{% highlight java %}
print(5 * 8 + 2);
{% endhighlight %}
</section>

<section markdown="block">
### Coordinate System

* 0, 0 (origin) is on the upper left
* x increases as you go right along the x-axis
* y increases you go down the y-axis
</section>

<section markdown="block">
### Drawing

* functions draw on top of one another
* (that is ... if you call a drawing function after another one... the first one will be obscured)
</section>

<section markdown="block">
### rect

* draws a rectangle
* arguments are:
	* x position of upper left corner
	* y position of upper left corner
	* w width
	* h height
{% highlight java %}
rect(0, 0, 100, 100 );
{% endhighlight %}
</section>

<section markdown="block">
### ellipse

* draws an ellipse
* arguments are:
	* x position of center
	* y position of center
	* w width
	* h height
{% highlight java %}
ellipse(50, 50, 100, 100 );
{% endhighlight %}
</section>

<section markdown="block">
### fill

* changes the fill color of the shapes you draw
* arguments are:
	* red component of color
	* green component of color
	* blue component of color
{% highlight java %}
fill(0, 100, 0);
ellipse(50, 50, 100, 100 );
{% endhighlight %}
</section>

<section markdown="block">
### stroke, noStroke

* outline or don't outline
* no arguments

{% highlight java %}
noStroke();
ellipse(50, 50, 100, 100 );

stroke()
ellipse(50, 50, 100, 100 );
{% endhighlight %}
</section>

<section markdown="block">
### Try Together

Draw a square on the:

* draw upper left
* draw upper right
* center
* lower left
* lower right

Repeat with an ellipse....
Repeat with different colors
</section>

<section markdown="block">
### Try Together

* draw 3 rectangles right next to each other
* draw 3 circles right next to each other
* draw 3 rectangles 10 pixels away from each other
* draw 3 circles 10 pixels away from each other

</section>

<section markdown="block">
## [Draw Some Stuff](draw_stuff.html)
</section>
