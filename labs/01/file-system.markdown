---
layout: slides
title: MTEC1002 - File System
---

<section markdown="block" class="title-slide">
# Navigating the File System
{% include title-slide-footer.html %}
</section>

<section markdown="block">
### Navigating the File System

<aside>In Three Parts</aside>

* OSX's directory structure
* A little bit about pathnames
* How to get around using the commandline
</section>

<section markdown="block">
## Let's Look at OSX's Directory Structure
</section>

<section markdown="block">
### First, Some Definitions

What's a __directory__? &rarr;

<div class="incremental" markdown="block">
* a __directory__ is a cataloging structure on a file system that references other files (and directories)
* we can think of it as _a thing that contains files_ (it's a little more complex than that, though)
* they're usually used to organize files
* (technically, on OSX, a directory is a file itself! it's a file that lists the names of items on a disk or other piece of storage media)
</div>
</section>

<section markdown="block">
### More Definitions

What's a __folder__? &rarr;

<div class="incremental" markdown="block">
* it's essentially the same thing as a directory
* but it's the graphical representation (like the little folder icons in finder)
</div>
</section>

<section markdown="block">
### Even More Definitions

What's a __pathname__? &rarr;

<div class="incremental" markdown="block">
* a __pathname__ is the general form of the name of a file or directory; it specifies a unique location in a file system
* for example, in finder, to locate a file or folder, you follow a particular path - __let's check this out__ &rarr;. 
* __what's the path to the Desktop starting from the _top most_ folder, the hard drive (probably Macintosh HD on the lab computers)?__ &rarr;
</div>
</section>

<section markdown="block">
### Some Structure

Each operating system organizes their files and directories differently.  OSX's file structure looks like this (it's similar to other UNIX based file systems):

* __/__ - (also called __root__) the top most folder on a disk (the directory that _contains_ all of the other files and directories)
* __/Applications__ - where shared applications are kept
* __/Users__ - all user accounts and their accompanying files are stored here
* __/Volumes__ - all disks that are attached to your computer including USB drives, hard drives, etc.
* __/System__ - _system specific_ files, libraries, preferences that are critical to the operating system

</section>

<section markdown="block">
### More About the User's Directory

It's worth noting the directories nested under Users.  They should seem familiar to you.

* __/Users/username__ - (also called __home__ when you're in your own username's directory) contains files specific to that particular user
* __/Users/username/Desktop__ - represents the user's Desktop
* __/Users/username/Downloads__ - the user's downloads folder
</section>


<section markdown="block">
## And Now... To Pathnames!

<aside>We know a little bit about the file system structure; let's take a closer look at how we locate files</aside>
</section>

<section markdown="block">
### What's a Pathname Again?

A __pathname__ is the general form of the name of a file or directory; __it specifies a unique location in a file system__.
</section>

<section markdown="block">
### Path Separator

A __path separator__ is a character that's used to join together each directory in a pathname that contains nested directories (for example, Desktop was located under Users and username...  there was a character that separated each directory).  

__What character represents the path separator on OSX (we just saw this)?__ &rarr;

<div class="incremental" markdown="block">
* it's a __forward slash__, __/__
* (sometimes just called __slash__ when referencing directories) 
* it's __not backslash__ (that's the path separator for Windows!)
</div>
</section>

<section markdown="block">
### Absolute vs Relative Paths

* __absolute paths__ are paths expressed as starting from root
	* example: /Users/username/Desktop
* __relative paths__ are paths expressed as relative from the current working directory
	* example (if you're starting from /Users/username): Desktop

We'll look at this a little bit more in the next class.
</section>

<section markdown="block">
### Some Special Paths

There are shortcuts to represent specific paths:

* __~ (tilde)__ is _your_ home directory
* __/ (slash)__ is root directory

The following paths are relative to the directory _that you're in_:

* __. (dot)__ is the current directory
* __.. (dot dot)__ is the parent directory
* __../.. (dot dot slash dot dot)__ is the parent of the parent directory

</section>

<section markdown="block">
### Let's See Some Pathnames Through Finder

* Desktop
* Downloads
* root (probably Macintosh HD)
</section>

<section markdown="block">
## Now That We Know About Pathnames, We Can Navigate the File System Using the Commandline! (EXCITED YET!?)

<aside>Let's learn some commands</aside>
</section>

<section markdown="block">
### ls

__List all of the files (and directories) in the current directory. &rarr;__ 

Think: _list_ (we just saw this!).

{% highlight bash %}
$ ls
Applications	Documents   ....
{% endhighlight %}
</section>

<section markdown="block">
### ls pathname

__List all of the files (and directories) in the directory specified by the pathname. &rarr;__ 

{% highlight bash %}
$ ls Desktop
cuny-first.png		fractal mountains
{% endhighlight %}
</section>

<section markdown="block">
### ls -l

__The -l flag gives detailed output about each file in the directory &rarr;__ 

Think: _l for long version_.

{% highlight bash %}
$ ls -l
drwx------   3 joe  staff   102 Nov  1 15:08 Applications
drwx------+  7 joe  staff   238 Jan 28 22:46 Desktop
{% endhighlight %}
</section>

<section markdown="block">
### ls -a

__The -a flag lists all files, including hidden ones &rarr;__ 

Think: _a for all_.

{% highlight bash %}
$ ls -a
.			.config			Dropbox
{% endhighlight %}
</section>

<section markdown="block">
### ls -al

__You can combine flags by placing them one after the other.  This outputs a detailed list of all files. &rarr;__ 

{% highlight bash %}
$ ls -al
drwxr-xr-x+ 67 joe   staff   2278 Jan 30 02:07 .
drwxr-xr-x   5 root  admin    170 Aug 13  2011 ..
-rw-r--r--@  1 joe   staff  24580 Jan 30 02:19 .DS_Store
-rw-r--r--   1 joe   staff   3459 Mar 21  2011 .RData
{% endhighlight %}
<!-- remove_highlight -->
</section>

<section markdown="block">
### ls -t

__The -t flag sorts by time. &rarr;__ 

{% highlight bash %}
$ ls -lt
total 0
drwxr-xr-x   2 joe  staff    68 Jan 30 02:07 mtec1002
drwx------@ 19 joe  staff   646 Jan 29 21:21 Dropbox
drwxr-xr-x   9 joe  staff   306 Jan 29 19:31 projects
{% endhighlight %}
<!-- remove_highlight -->
</section>

<section markdown="block">
### Combining Flags and Arguments

You can use multiple flags... and combine them with an argument as well. __What do you think this does?__ &rarr;

{% highlight bash %}
$ ls -alt Desktop
{% endhighlight %}

<div class="incremental" markdown="block">
It lists all of the files in Desktop (if you're in your _home_ folder), ordered by time, including hidden files and showing extra information.

{% highlight bash %}
drwxr-xr-x+ 40 joe  staff    1360 Jan 29 01:12 ..
-rw-r--r--@  1 joe  staff    6148 Jan 25 01:46 .DS_Store
drwx------+  6 joe  staff     204 Jan 24 08:26 .
-rw-r--r--@  1 joe  staff  245447 Jan 23 23:15 cuny-first.png
drwxr-xr-x  16 joe  staff     544 Oct 28 18:46 fractal mountains
-rw-r--r--   1 joe  staff       0 Aug 31 22:41 .localized
{% endhighlight %}
</div>
<!-- remove_highlight -->

</section>

<section markdown="block">
### pwd

__Shows the directory that you're currently in.__ &rarr;

Think: _print working directory_.

{% highlight bash %}
$ pwd
/Users/joe
{% endhighlight %}
</section>

<section markdown="block">
### hostname

__Prints out the name of your computer &rarr;__

{% highlight bash %}
$ hostname
walsh-9
{% endhighlight %}
</section>

<section markdown="block">
### mkdir

__Creates a directory with the name of the argument supplied. &rarr;__

Think: _make directory_

One argument is _required_: the name of the directory to create.

{% highlight bash %}
$ mkdir my_animated_gifs
{% endhighlight %}
</section>

<section markdown="block">
### mkdir dir1/dir2/dir3

__This attempts to create 3 directories nested within eachother. &rarr;__

Forward slash (/) shows that a directory is within the directory preceding it.  dir1/dir2 means dir2 in dir1.

However, nested directories don't work as an argument for mkdir. (Unless...)
{% highlight bash %}
$ mkdir dir1/dir2
mkdir: dir1: No such file or directory
{% endhighlight %}
</section>

<section markdown="block">
### mkdir -p dir1/dir2

__The -p flag allows you to create multiple directories nested within eachother. &rarr;__

{% highlight bash %}
mkdir -p dir1/dir2
$ ls
dir1
$ ls dir1
dir2
{% endhighlight %}
</section>

<section markdown="block">
### cd

__Changes current directory to the directory specified in the argument. &rarr;__

Think: _change directory_

One argument is _required_: the name of the directory to change to.

{% highlight bash %}
$ cd Desktop
$ pwd
/Users/joe/Desktop
{% endhighlight %}
</section>

<section markdown="block">
### A Reminder About Special Paths

* . (dot) is current directory
* .. (dot dot) is parent directory
* ../.. (dot dot slash dot dot) is parent of parent directory
* / (slash) is root directory
* ~ (tilde) is home directory

</section>

<section markdown="block">
### Using Special Paths 

Let's use special paths with cd &rarr;

{% highlight bash %}
$ pwd
/Users/joe
$ cd ../
$ pwd
/Users
$ ls
Shared	joe
$ cd ~
$ pwd
/Users/joe
$ cd /
$ pwd
/
{% endhighlight %}
</section>

<section markdown="block">
### Back to Directory 

__Pass - (dash) as an argument to cd to go back to the directory you just changed from. &rarr;__

{% highlight bash %}
$ pwd
/Users/joe
$ cd /tmp
$ pwd
/tmp
$ cd -
/Users/joe
{% endhighlight %}
</section>

<section markdown="block">
### rmdir

__Removes a directory with the name of the argument supplied. &rarr;__

Think: _remove directory_

One argument is _required_: the name of the directory to remove.

{% highlight bash %}
$ mkdir foo
$ ls
foo
$ rmdir foo
$ ls

{% endhighlight %}
</section>

<section markdown="block">
### pushd/popd

__Change to directory, but save current one for later. &rarr;__

* pushd requires one argument, the directory to change to.
* you can pushd multiple directories
* popd takes you back to the last saved directory
* you can continue to use popd until there are no more saved directories

</section>

<section markdown="block">
### pushd/popd Continued

{% highlight bash %}
$ pwd
/Volumes
$ pushd ~/Desktop/
~/Desktop /Volumes
$ pushd /Applications/
/Applications ~/Desktop /Volumes
$ popd
~/Desktop /Volumes
$ pwd
/Users/joe/Desktop
$ popd
/Volumes
{% endhighlight %}

</section>

<section markdown="block">
### __Activity__: Drills!

Entering commands _flash cards_ x 10 (use set 2)

We'll do this together, then try downloading it yourself:

1. Download [drills.py](drills.py) to the home directory
2. Type python drills.py
3. When prompted for a number, enter 2
4. CTRL-C quits
</section>

<section markdown="block">
### __Lab__

[Navigating the File System](lab-file-system.txt)

* Type each command (with arguments and flags) exactly
* Only press &lt;ENTER&gt; when instructed...
* &lt;TAB&gt;, &lt;ENTER&gt;, &lt;UP&gt;, &lt;DOWN&gt; are the actual keys!
* Paste answer or output below the dashed line (------------)

</section>

<section markdown="block">
### __Activity__: Drills!

Entering commands _flash cards_ x 10 (use set 12)

We'll do this together, then try downloading it yourself:

1. Download [drills.py](drills.py) to the home directory
2. Type python drills.py
3. When prompted for a number, enter 12
4. CTRL-C quits
</section>

