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

__Create a new file or change the modified date of an existing file&rarr;.__

* think - record the last time you've _touched_ the file.
* takes one argument, the path of the file name that you're modifying/creating
* __if the file already exists__ touch changes the modified date &rarr;
* __if the file does not exist__ it creates it &rarr;


{% highlight bash %}
touch filename.txt
{% endhighlight %}
</section>

<section markdown="block">
### cp

__Copy file to a path&rarr;__

* think: _copy_ (obv!)
* requires two arguments - pathnames for both source and destination
* can take a flag, -r, to copy _recursively_

{% highlight bash %}
cp filename1.txt filename2.txt

# use -r to copy recursively (for example, all nested directories and files)

cp -r dir1 dir2
{% endhighlight %}
</section>

<section markdown="block">
### mv
__Move file to a different location. &rarr;__

* think: _move_.
* requires two arguments - pathnames for both source and destination

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

* requires a single argument, the path to the file

{% highlight bash %}

less filename1.txt

# use <SPACE> to page down
# use <b> to page up
# use <UP>,<DOWN> to navigate by line
# use <q> to quit
# use </> to search
{% endhighlight %}
</section>

<section markdown="block">
### more

__Show the contents of a file with pagination. &rarr;__

* requires a single argument, the path to the file

{% highlight bash %}
more filename1.txt
{% endhighlight %}
</section>

<section markdown="block">
### cat

__Show all of the contents of a file &rarr;__

* requires a single argument, the path to the file

{% highlight bash %}
cat filename1.txt
{% endhighlight %}
</section>

<section markdown="block">
### head

__Show the contents of the start of a file. &rarr;__

* think __head is the beginning / top__ of the file 
* requires a single argument, the path to the file

{% highlight bash %}
head filename1.txt
{% endhighlight %}
</section>

<section markdown="block">
### tail

__Show the contents of the end of a file. &rarr;__

* think __tail is the end of the file__
* requires a single argument, the path to the file
* can be used with flags: -f (realtime) and -n (how many lines should be displayed?)


{% highlight bash %}
tail filename1.txt

# show changes realtime!
tail -f filename.txt

# display last 5 lines
tail -n5  filename.txt
{% endhighlight %}
</section>

<section markdown="block">
### rm

__Remove a file. &rarr;__

* think: _remove_
* requires a single argument, the path to the file
* has an optional flag, -r, for removing recursively
* has an optional flag, -f, for skipping confirmation

{% highlight bash %}
rm filename1.txt

# also... to remove everything recursively (and ignore
# confirmation)... use this (be careful with it!)

rm -rf filename1.txt
{% endhighlight %}
</section>

<section markdown="block">
### wc

__Count the number of words or lines in a file. &rarr;__

* think: _word count_
* requires a single argument, the path to the file
* displays lines, words, bytes

{% highlight bash %}
# count the number of words in a file
wc filename.txt

# count the number of lines in a file
wc -l filename.txt
{% endhighlight %}

</section>


<section markdown="block">
### __Activity__: Drills!

Entering commands _flash cards_ x 3 (use set 3)

We'll do this together, then try downloading it yourself:

1. Download [drills.py](drills.py) to the home directory
2. Type python drills.py
3. When prompted for a number, enter 3
4. CTRL-C quits
</section>

<section markdown="block">
### __Lab__

[Working With Files](lab-03-part-02-working-with-files.txt)

* Type each command (with arguments and flags) exactly
* Only press &lt;ENTER&gt; when instructed...
* &lt;TAB&gt;, &lt;ENTER&gt;, &lt;UP&gt;, &lt;DOWN&gt; are the actual keys!
* Paste answer or output below the dashed line (------------)

</section>

<section markdown="block">
### __Activity__: Drills!

Entering commands _flash cards_ x 3 (use set 123)

We'll do this together, then try downloading it yourself:

1. Download [drills.py](drills.py) to the home directory
2. Type python drills.py
3. When prompted for a number, enter 123
4. CTRL-C quits
</section>

<section markdown="block">
## [Permissions, Editing, Date and Time](permissions-editing-date-time.html)
</section>
