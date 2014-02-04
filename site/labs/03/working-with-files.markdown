---
layout: slides
title: MTEC1002 - Working With Files
---

<section markdown="block" class="title-slide">
# Working With Files
{% include title-slide-footer.html %}
</section>

<section markdown="block">
### touch

__Create a new file or change the modified date &rarr;.__

{% highlight bash %}
touch filename.txt
{% endhighlight %}
</section>

<section markdown="block">
### cp

__Copy file to a path&rarr;__

(requires two arguments - source and destination)

Think: _copy_.

{% highlight bash %}
cp filename1.txt filename2.txt

# use -r to copy recursively (for example, directories)

cp -r dir1 dir2
{% endhighlight %}
</section>

<section markdown="block">
### mv
__Move file to a different location. &rarr;__

Think: _move_.

{% highlight bash %}
# renaming 
mv filename1.txt filename2.txt

# moving
mv filename.txt dir
{% endhighlight %}
</section>

<section markdown="block">
### less

__Show the contents of a file with pagination. &rarr;__

{% highlight bash %}

less filename1.txt

# use <SPACE> to page down
# use <B> to page up
# use <UP>,<DOWN> to navigate by line
# use <Q> to quit
{% endhighlight %}
</section>

<section markdown="block">
### more

__Show the contents of a file with pagination. &rarr;__

{% highlight bash %}
more filename1.txt
{% endhighlight %}
</section>

<section markdown="block">
### cat

__Show all of the contents of a file &rarr;__

{% highlight bash %}
cat filename1.txt
{% endhighlight %}
</section>

<section markdown="block">
### head

__Show the contents of the start of a file. &rarr;__


{% highlight bash %}
head filename1.txt
{% endhighlight %}
</section>

<section markdown="block">
### tail

__Show the contents of the end of a file. &rarr;__


{% highlight bash %}
tail filename1.txt

# show changes realtime!

tail -f filename.txt
{% endhighlight %}
</section>

<section markdown="block">
### rm

__Remove a file. &rarr;__

Think: _remove_

{% highlight bash %}
rm filename1.txt

# also... to remove everything recursively (and ignore
# confirmation)... use this (be careful with it!)

rm -rf filename1.txt
{% endhighlight %}
</section>

<section markdown="block">
### wc

__Count the number of words or files in a file. &rarr;__

Think: _word count_

{% highlight bash %}
# count the number of words in a file
wc filename.txt

# count the number of lines in a file
wc -l filename.txt
{% endhighlight %}

</section>


<section markdown="block">
### __Activity__: Drills!

Entering commands _flash cards_ x 10 (use set 3)

We'll do this together, then try downloading it yourself:

1. Download [drills.py](drills.py) to the home directory
2. Type python drills.py
3. When prompted for a number, enter 3
4. CTRL-C quits
</section>

<section markdown="block">
### __Lab__

[Working With Files](working-with-files.txt)

* Type each command (with arguments and flags) exactly
* Only press &lt;ENTER&gt; when instructed...
* &lt;TAB&gt;, &lt;ENTER&gt;, &lt;UP&gt;, &lt;DOWN&gt; are the actual keys!
* Paste answer or output below the dashed line (------------)

</section>

<section markdown="block">
### __Activity__: Drills!

Entering commands _flash cards_ x 10 (use set 123)

We'll do this together, then try downloading it yourself:

1. Download [drills.py](drills.py) to the home directory
2. Type python drills.py
3. When prompted for a number, enter 123
4. CTRL-C quits
</section>
