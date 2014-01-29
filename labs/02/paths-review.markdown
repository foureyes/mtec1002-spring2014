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

</section>

<section markdown="block">
### Navigating the File System

__List all of the commands that we know as well as what they do... &rarr;__ 

<div class="incremental" markdown="block">
* pwd - print working directory
* hostname - display name of computer
* mkdir - make a directory 
* cd - change directory
* ls - list contents of current directory
* rmdir - remove a directory
* pushd - save current directory
* popd -  go to most recent saved directory
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

Entering commands _flash cards_ x 10 (use set 1)

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

You can reference an absolute path regardless of what directory you're in
</section>

<section markdown="block">
### Relative Paths

__Relative paths__ are paths expressed as relative from the current working directory.

For example... if you're in /Users

* to get to home: professor
* to get to Desktop: professor/Desktop

You have to be in the directory that you're assuming to be current for this to work.
</section>

<section markdown="block">
### __Lab__

[Paths and Review](paths-review.txt)

* Type each command (with arguments and flags) exactly
* Only press &lt;ENTER&gt; when instructed...
* &lt;TAB&gt;, &lt;ENTER&gt;, &lt;UP&gt;, &lt;DOWN&gt; are the actual keys!
* Paste answer or output below the dashed line (------------)

</section>

<section markdown="block">
## [Output, Download and Uncompress](output-download-uncompress.html)
</section>
