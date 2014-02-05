---
layout: slides
title: MTEC1002 - Paths and Review
---

<section markdown="block" class="title-slide">
# Paths and Review
{% include title-slide-footer.html %}
</section>

<section markdown="block">
### Definitions

Define the following terms, and give an example of each.

* command
* flag / option
* argument
* prompt
* pathname
* path separator

</section>

<section markdown="block">
### Definitions Continued

* __commands__ are __verbs__; they tell the computer to do something.  ex. __ls__
* __options__ are like __adverbs__;  they specify how a command is run.  ex. the -l flag in __ls -l__
* __arguments__ are the thing or things that a command acts on; they're like __nouns__ (or more formally, __direct objects__).  ex. Desktop in __ls Desktop__
* the __prompt__ is the symbol (or symbols) that appear in your terminal indicating that the computer is waiting for input
* a __pathname__ is the general form of the name of a file or directory; it specifies a unique location in a file system.  ex. /Users/student/Desktop
* a __path separator__ is a character that's used to join together each directory in a pathname.  ex. /
</section>

<section markdown="block">
### OSX Directory Structure

__What is the top most folder on a disk (the directory that _contains_ all of the other files and directories) called?__

<div class="incremental" markdown="block">
root or /

__What is the full path to the student user's "Home" folder?__

/Users/student or ~

</div>
</section>

<section markdown="block">
### OSX Directory Structure

__What is the full path to the student user's "Desktop"?__

<div class="incremental" markdown="block">

/Users/student/Desktop

__What directory contains all of the disks (USB drives, SSDs, etc.) that are attached to your computer?__ 

/Volumes
</div>
</section>

<section markdown="block">
### OSX Directory Structure Continued

* __/__ - (also called __root__) the top most folder on a disk (the directory that _contains_ all of the other files and directories)
* __/Applications__ - where shared applications are kept
* __/Users__ - all user accounts and their accompanying files are stored here
* __/Volumes__ - all disks that are attached to your computer including USB drives, hard drives, etc.
* __/System__ - _system specific_ files, libraries, preferences that are critical to the operating system
</section>

<section markdown="block">
### Within the User's Directory

* __/Users/username__ - (also called __home__ when you're in your own username's directory) contains files specific to that particular user
* __/Users/username/Desktop__ - represents the user's Desktop
* __/Users/username/Downloads__ - the user's downloads folder
* __/Users/username/Documents__ - the user's documents folder
</section>

<section markdown="block">
### Navigating the File System

__List all of the commands that we know as well as what they do... &rarr;__ 

<div class="incremental" markdown="block">
* __pwd__ - print working directory
* __hostname__ - display name of computer
* __mkdir__ - make a directory 
* __cd__ - change directory
* __ls__ - list contents of current directory
* __rmdir__ - remove a directory
* __pushd__ - save current directory
* __popd__ -  go to most recent saved directory
</div>
</section>

<section markdown="block">
### About ls

__Does ls take any arguments or flags?  If so, what are they? &rarr;__ 

<div class="incremental" markdown="block">
* ls __optionally__ takes __one argument__ - the directory that you'd like to list files in.  ex.  shows all files on your desktop - ls ~/Desktop
* __-l__ - show detailed (long) listing
* __-a__ - display all files, even hidden files
* __-t__ - sort lsting by time
</div>
</section>

<section markdown="block">
### About mkdir

__Does mkdir take any arguments or flags?  If so, what are they? &rarr;__ 

<div class="incremental" markdown="block">
* mkdir __requires one argument__ - the directory that you're creating
* __-p__ - create each nested directory in the pathname specified as the argument.  ex.  this creates three directories nested within eachother - mkdir foo/bar/baz 
</div>
</section>

<section markdown="block">
### Some Special Symbols for Paths

__Name some special symbols that we know for paths... like current directory or home. &rarr;__

<div class="incremental" markdown="block">
<pre>
 . (dot) - the current directory
 ..  (dot dot) - up one directory (parent directory)
 ../..  (dot dot slash dot dot)  - up two directories
 /  (slash) - root directory
 ~ (tilde) - home directory
 - (dash) - directory you were previously in
</pre>
</div>
</section>


<section markdown="block">
### Making Things Easier...

__Name some special keys that we use to reduce the amount of typing that we have to do. &rarr;__

<div class="incremental" markdown="block">
* &lt;TAB&gt; - autocomplete
* &lt;TAB&gt;&lt;TAB&gt; -autocomplete
* &lt;UP&gt; - previous commend
* &lt;DOWN&gt; - next command
</div>
</section>

<section markdown="block">
### __Activity__: Drills!

Entering commands _flash cards_ x 3 (use set 1)

We'll do this together, then try downloading it yourself:

1. Download [drills.py](drills.py) to the home directory
2. Type python drills.py
3. When prompted for a number, enter 1
4. CTRL-C quits
</section>



<section markdown="block">
### More About Paths

root

* represented by /
* the 'parent' directory

</section>

<section markdown="block">
### Absolute Paths

__Absolute paths__ are paths expressed as starting from root.

* /Users/professor/Desktop
* /Volumes

__You can reference an absolute path regardless of what directory you're in__.
</section>

<section markdown="block">
## You can reference an absolute path regardless of what directory you're in
</section>

<section markdown="block">
### Relative Paths

__Relative paths__ are paths expressed as relative from the current working directory.

For example... if you're in /Users

* to get to home: cd student
* to get to Desktop: cd student/Desktop

You have to be in the directory that you're assuming to be current for this to work.
</section>

<section markdown="block">
## Remember - at the _prompt_, you're running _commands_ in the context of some location (think folder/directory) on your computer
</section>

<section markdown="block">
### What Was That Again? 

* when you're at the prompt
* and you type in a command
* you're doing so while you're in a particular folder/directory
* you're always _located_ somewhere on your file system

</section>

<section markdown="block">
### Absolute vs Relative Paths

* image that you're at a prompt.  
* you type __pwd__ to determine where you are; it says that you're in __/Volumes__.  
* you type __ls__ to see what's in the directory that you're in, and you see:

{% highlight bash %}
Macintosh HD			USBDRIVE1			USBDRIVE2		
{% endhighlight %}

__How would you change directory so that you're in USBDRIVE1 by using an absolute path?  What about relative?__ &rarr;

<div class="incremental" markdown="block">
* absolute - cd /Volumes/USBDRIVE1
* relative - cd USBDRIVE1
</div>
</section>

<section markdown="block">
### Absolute vs Relative Paths

* assume the same folder structure exists as the previous slide - /Volumes contains three directories: USBDRIVE1, USBDRIVE2 and Macintosh HD
* you type __pwd__ to determine where you are; now it says that you're in __/Volumes/USBDRIVE1__.  

__How would you change directory so that you're in USBDRIVE2 instead?  Do this with an absolute path, and again with a relative path.__ &rarr;

<div class="incremental" markdown="block">
* absolute - cd /Volumes/USBDRIVE2
* relative - cd ../USBDRIVE2
</div>
</section>

<section markdown="block">
### Absolute vs Relative Paths

* you type __pwd__ to determine where you are; you're in your Desktop - /Users/student/Desktop  

__List as many different ways to get to your Downloads folder with one command.__ &rarr;

<div class="incremental" markdown="block">
* absolute - cd /Users/student/Downloads
* absolute - cd ~/Downloads
* relative - cd ../Downloads
</div>
</section>

<section markdown="block">
### __Lab__

[Paths and Review](lab-02-part-01-paths-review.txt)

* Type each command (with arguments and flags) exactly
* Only press &lt;ENTER&gt; when instructed...
* &lt;TAB&gt;, &lt;ENTER&gt;, &lt;UP&gt;, &lt;DOWN&gt; are the actual keys!
* Paste answer or output below the dashed line (------------)

</section>

<section markdown="block">
## [Output, Download and Uncompress](output-download-uncompress.html)
</section>
