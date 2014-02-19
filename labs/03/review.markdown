---
layout: slides
title: MTEC1002 - Review
---

<section markdown="block" class="title-slide">
# Review
{% include title-slide-footer.html %}
</section>

<section markdown="block">
### Last Week

__What did we go in our last class?__

<div class="incremental" markdown="block">
* paths - absolute and relative
* input and output, downloading files, archiving/compressing and extracting/uncompressing
</div>
</section>

<section markdown="block">
### Special Symbols for Paths

__What symbols represent the following directories? &rarr;__

* the current directory
* up one directory (parent directory)
* up two directories
* root directory
* home directory
* directory you were previously in

</section>

<section markdown="block">
### Special Symbols for Paths
* __.__ (dot) - the current directory
* __..__  (dot dot) - up one directory (parent directory)
* __../..__  (dot dot slash dot dot)  - up two directories
* __/__  (slash) - root directory
* __~__  (tilde) - home directory
* __-__ (dash) - directory you were previously in
</section>


<section markdown="block">
### Root

* __What's the root directory?__ &rarr;
* __What symbol represents it??__ &rarr;

<div class="incremental" markdown="block">
* the __root directory__ is the top most folder or directory in a file system
	* it contains all of the other directories and files
	* think "Macintosh HD" on OSX
	* or c: on Windows
* root is represented by "/"
	* __cd /__ will bring you to the root directory
</div>
</section>

<section markdown="block">
### BTDubs Abt Root

We didn't explicitly mention this in the last class (though some of you encountered it while working on the labs), but:

* the __root directory__ is not writable by the lab computer default user account
* consequently, if you're in root, commands like mkdir, touch, etc... should fail
* __let's try this out__ &rarr;
* __(how do I get to root again?)__ &rarr;
</section>

<section markdown="block">
### Absolute Paths

__What's an absolute path?__ 

<div class="incremental" markdown="block">
* __absolute paths__ are paths expressed as starting from root.
	* /Users/professor/Desktop
	* /Volumes
* you can get to an absolute path regardless of your current working directory
</div>
</section>

<section markdown="block">
### Relative Paths

__What's a relative path?__ 

<div class="incremental" markdown="block">
* __relative paths__ are paths expressed as relative from the current working directory.
	* current directory is /User; to get to home: professor
	* current directory is /User; to get to Desktop: professor/Desktop
* you have to be in the directory that you're assuming to be current for this to work.
</div>
</section>

<section markdown="block">
### Relative and Absolute

__Tell me how to create these directories in my home folder__ &rarr;

* a directory called myprojects
* within that, two directories called lab1 and lab2
* and finally, in lab1, create a directory called output

This should result in:

* myprojects
* myprojects/lab1
* myprojects/lab2
* myprojects/lab1/output
</section>

<section markdown="block">

### Relative and Absolute Path Questions

1. From /Volumes, change to the lab1 directory that was just created
2. From home directory, what's the __relative__ path to output?
3. From home directory, what's the __absolute__ path to output?
4. From output, what's the __relative__ path to lab2?
5. From output, what's the __absolute__ path to lab2?
6. From lab2, what's the relative path to output?
7. From lab2, what's the absolute path to output?
</section>

<section markdown="block">

### Relative and Absolute Path Questions

1. In /Volumes: __cd ~/myprojects/lab1__
2. In home: __myprojects/lab1/output__
3. In home: __/Users/professor/myprojects/lab1/output__
4. In myprojects/lab1/output: __../../lab2__
5. In myprojects/lab1/output: __/Users/professor/myprojects/lab2__
6. In lab2: __../lab1/output__
7. In lab2: __/Users/professor/myprojects/lab1/output__

</section>

<section markdown="block">
### Reviewing input/output Commands

* __How do I print/output text to the screen? &rarr;__
* __How do I clean up / remove the text from the screen? &rarr;__

<div class="incremental" markdown="block">
* echo hello
* clear
</div>
</section>

<section markdown="block">
### Downloading Files

* __How do I download a file and display its contents on my screen with one command? &rarr;__
* __How do I download a file and save it to a file with a specified name? &rarr;__

<div class="incremental" markdown="block">
* curl someurl.com
* curl -o filename.txt someurl.com
* what's the -o flag its following argument for?

...it specifies the name of the file to save your download to.
</div>
</section>

<section markdown="block">
### Archiving and Compressing Files

* __How do I archive an entire directory into a single file? &rarr;__
* __How do I compress a file? &rarr;__

<div class="incremental" markdown="block">
* tar -cvf archivename.tar dirname
* gzip filename
</div>
</section>

<section markdown="block">
### Extract and Uncompress

* __How do I uncompress a zip (.zip) file? &rarr;__
* __How do I extract files from a compressed archive (.tar.gz)? &rarr;__

<div class="incremental" markdown="block">
* unzip filename.zip
* tar -xvf filename
</div>
</section>

<section markdown="block">
### Extract and Uncompress (Again)

* __Again, what do I use to uncompress a zip (.zip) file? &rarr;__
* __...And how do I extract files from a compressed archive (.tar.gz)? &rarr;__

<div class="incremental" markdown="block">
* unzip filename.zip
* tar -xvf filename
</div>
</section>

<section markdown="block">
### __Activity__: Drills!

Entering commands _flash cards_ x 3 (use set 2)

We'll do this together, then try downloading it yourself:

1. Download [drills.py](drills.py) to the home directory
2. Type python drills.py
3. When prompted for a number, enter 2
4. CTRL-C quits
</section>

<section markdown="block">
### Summary Part 1

(brackets - []'s  - denote arguments that you must supply; __the brackets are not part of the command__, so don't type them out)

* echo [something to print to the screen]
* clear
* curl [url of file to downlaod]
* curl -o [name of file to download to] [url of file to download]	
* unzip [name of file to unzip]
* tar -xvf [name of file to extract and uncompress]
* tar -cvf [name of archive] [name of directory to archive]
* gzip [name of file to compress]
</section>

<section markdown="block">
### __Lab__

[Review](lab-03-part-01-review.txt)

* Type each command (with arguments and flags) exactly
* Only press &lt;ENTER&gt; when instructed...
* &lt;TAB&gt;, &lt;ENTER&gt;, &lt;UP&gt;, &lt;DOWN&gt; are the actual keys!
* Paste answer or output below the dashed line (------------)

</section>

<section markdown="block">
### __Activity__: Everything We've Learned So Far

Entering commands _flash cards_ x 3 (use sets 1 and 2)

We'll do this together, then try downloading it yourself:

1. Download [drills.py](drills.py) to the home directory
2. Type python drills.py
3. When prompted for a number, enter 12
4. CTRL-C quits
</section>

<section markdown="block">
## [Working With Files](working-with-files.html)
</section>

