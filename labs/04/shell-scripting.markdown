---
layout: slides
title: MTEC1002 - Version Control 
---

<section markdown="block" class="title-slide">

# Some Odds and Ends, Shell Scripting

{% include title-slide-footer.html %}
</section>


<section markdown="block">
### Creating a File, Editing a File, Viewing a File

__What command did we use to create a file?__ &rarr;

<div class="incremental" markdown="block">

{% highlight bash %}
touch name_of_file.txt
{% endhighlight %}

__What command did we use to edit a text file?__ &rarr;

{% highlight bash %}
nano name_of_file.txt
{% endhighlight %}


__What command(s) could we use to show a text file?__ &rarr;

{% highlight bash %}
cat name_of_file.txt 
# (also less and more)
{% endhighlight %}


</div>
</section>

<section markdown="block">
### Permissions

__How do we show the permissions associated with a file?__ &rarr;

<div class="incremental" markdown="block">

{% highlight bash %}
ls -l name_of_file.txt
{% endhighlight %}

__What do the permissions mean?__ &rarr;

* user, group or world ... readable, writable or executable
* u, g, and o ... r, w, and x

__What command do we use to change permissions ?__ &rarr;

{% highlight bash %}
chmod u+x name_of_file.sh 
{% endhighlight %}

__What permissions did the previous line give?__ &rarr;

</div>
</section>

<section markdown="block">
### Running Scripts

__How do we run a file that we made executable?__ &rarr;

<div class="incremental" markdown="block">

{% highlight bash %}
./name_of_file.sh
{% endhighlight %}

__What does dot mean again?__ &rarr;

The current directory

__So what do you think ./ does?__ &rarr;

In the directory I'm currently in... try to execute the following file

</div>
</section>

<section markdown="block">
### A Few Odds and Ends

* environment variables
* $PATH
* env
* ps
* kill
</section>

<section markdown="block">
### Environment Variables

__environment variables__ - are _dynamic_ variables that affect the way processes (programs) run on your computer.  for example, they may specify:

* the locations where your programs are stored so that they can be easily executed

</section>


