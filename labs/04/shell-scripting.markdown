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
### Running Scripts Continued

If we change to /, we'll see that our command will no longer work to run the script.

However, we can use the full path to the script to run it! (Notice, there's no dot at the beginning)

{% highlight bash %}
/full/path/to/name_of_file.sh
{% endhighlight %}
</section>

<section markdown="block">
### A Few Odds and Ends

* environment variables
* $PATH, $USER, 
* env
* ps
* kill
</section>

<section markdown="block">
### Environment Variables

__environment variables__ - are _dynamic named values_ that affect the way processes (programs) run on your computer.  for example, they may specify:

* the locations where your programs are stored so that they can be easily executed
* the current user


</section>

<section markdown="block">
### env

__env__ shows the list of current environment variables and their values

{% highlight bash %}
env
{% endhighlight %}
</section>

<section markdown="block">
### Setting and Using Environment Variable

setting

{% highlight bash %}
MYVAR="some value"
{% endhighlight %}

using

{% highlight bash %}
echo $MYVAR
{% endhighlight %}
</section>

<section markdown="block">
### Common Environment Variables

__$PATH__ - contains a colon-separated list of directories that the shell searches for commands that do not contain a slash in their name (commands with slashes are interpreted as file names to execute, and the shell attempts to execute the files directly)
__$USER__ - the current user
__$HOME__ - the full path to the current user's home directory

{% highlight bash %}
echo $PATH
{% endhighlight %}
</section>

<section markdown="block">
### ps

Show all running processes...

{% highlight bash %}
ps aux
{% endhighlight %}

Look for a specific process...

{% highlight bash %}
ps aux | grep -i program_to_find
{% endhighlight %}

The first number after username is the process ID

{% highlight bash %}
jversoza       34930   0.0  
{% endhighlight %}
</section>


<section markdown="block">
### kill

....and when you have a process id, you can kill that program!

{% highlight bash %}
kill 12345
{% endhighlight %}
</section>
