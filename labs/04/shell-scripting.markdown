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

</div>
</section>

<section markdown="block">
### Permissions Continued

__What permissions does the following line give/remove?__ &rarr;

{% highlight bash %}
chmod u-w name_of_file.sh 
{% endhighlight %}

<div class="incremental" markdown="block">
removes write from user

__What permissions do we have to give a file so that we can "run" it?__ &rarr;

{% highlight bash %}
chmod u+x name_of_file.sh 
{% endhighlight %}
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

* __$PATH__ - contains a colon-separated list of directories that the shell searches for commands that do not contain a slash in their name (commands with slashes are interpreted as file names to execute, and the shell attempts to execute the files directly)
* __$USER__ - the current user
* __$HOME__ - the full path to the current user's home directory

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

<section markdown="block">
### Shell Script Arguments

You can pass arguments to your shell scripts (just like commands like ls, cd, etc.):

{% highlight bash %}
./myscript.sh hello hi
{% endhighlight %}

Within your .sh file (your shell script), you can access these values by using $1, $2, etc ... with each number corresponding to an argument; it starts with $1 as the first argument (the one closest to the command).

{% highlight bash %}
# using variables in your shell script
echo $1
echo $2
{% endhighlight %}
</section>

<section markdown="block">
### Shell Scripts - Using Variables

You can use variables as part of longer strings.  For example, if we called our shell script by writing:

{% highlight bash %}
./myscript.sh example
{% endhighlight %}

Within the script:

{% highlight bash %}
echo "counting words, lines, bytes for ya!"
wc $1.txt
{% endhighlight %}

... would count the words in example.txt
</section>



<section markdown="block">
### Shell Scripts and For Loops

You can use the following syntax to repeat code.  Here $i is a variable that can be used... and it represents each number from 1 through 3.

{% highlight bash %}
for i in {1..3}
do
   echo "Counting $i"
done
{% endhighlight %}
</section>
