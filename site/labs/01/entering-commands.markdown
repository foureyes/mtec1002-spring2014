---
layout: slides
title: MTEC1002 - Entering Commands
---

<section markdown="block" class="title-slide">
# Entering Commands
{% include title-slide-footer.html %}
</section>

<section markdown="block">
### Commands

__Commands__ are __verbs__; they tell the computer to do something.
</section>

<section markdown="block">
### Entering a Command 

Once you have Terminal open, you should see a string of characters that ends with a dollar sign.  This is called the __command prompt__.  A __prompt__ looks something like this.

{% highlight bash %} walsh-9:~ joe$
{% endhighlight %}

Whenever you see a line in these slides prefixed with a $, that means that we're typing something in at the __prompt__.
</section>

<section markdown="block">
### Executing a Command

In terminal, type in the name of the command, and press &lt;ENTER&gt;.  __Let's trying using ls, a command to list files and directories__ &rarr; 

* open Terminal (Applications &rarr; Utilities &rarr; Terminal
* type __ls__
* press &lt;ENTER&gt;

{% highlight bash %}
$ ls
{% endhighlight %}
</section>

<section markdown="block">
### Where Are You?

Note that when you're at the prompt, you're always running commands in the context of some location on your computer.  

* This location corresponds to an actual directory.  
* You can change _where you are_ using various commands.  We'll see that later.
</section>

<section markdown="block">
## Let's Repeat That: At the prompt, you're running commands in the context of some location (think folder/directory) on your computer

</section>

<section markdown="block">
### What Was That Again? 

* when you're at the prompt
* and you type in a command
* you're doing so while you're in a particular folder/directory
* you're always _located_ somewhere on your file system

</section>

<section markdown="block">
### Arguments

__Arguments__ are the thing or things that a command acts on; they're like __nouns__ (or more formally, __direct objects__).
</section>

<section markdown="block">
### Commands and Arguments

Some commands can optionally have __arguments__:  

* they go after the command name
* a command may potentially be able to take 0 or more arguments

__Try this (list files in Desktop):__

{% highlight bash %}
$ ls Desktop
{% endhighlight %}
</section>

<section markdown="block">
### Flags

__Flags__ are like __adverbs__.  They specify how a command is run.

(sometimes they're also called _options_)
</section>

<section markdown="block">
### Commands and Flags

__Commands__ can optionally have __flags__.  

* they go after the command name, but usually before arguments
* they are specified with either - or --
* commands may have 0 or more flags.  

__Try this (list all, including hidden, files in Desktop):&rarr;__

{% highlight bash %}
$ ls -a Desktop
{% endhighlight %}
</section>

<section markdown="block">
### &lt;TAB&gt; Completion

You can use the &lt;TAB&gt; key to complete commands or file names.  __Try typing the following:&rarr;__

* ls Desk&lt;TAB&gt;
* __What happens? &rarr;__

<div class="incremental" markdown="block">
The argument, Desktop, is automatically completed for you!  __Go ahead and run the command by pressing &lt;ENTER&gt; &rarr;__


</div>
</section>

<section markdown="block">
### &lt;TAB&gt;&lt;TAB&gt;

What if there are multiple matches?  __Type the letter l and then &lt;TAB&gt;. What happens? &rarr;__

<div class="incremental" markdown="block">
Nothing.  Now try hitting &lt;TAB&gt; one more time.  __What happens? &rarr;__

All of the possible commands that start with the letter l are shown.
</div>
</section>

<section markdown="block">
### Next and Previous Commands

You can use the &lt;UP&gt; or &lt;DOWN&gt; keys to go through previous and next commands.  __Try pressing &lt;UP&gt; twice, and &lt;DOWN&gt; once.  What command is shown?__

{% highlight bash %}
$ ls Desktop
{% endhighlight %}
</section>

<section markdown="block">
### Errors

Type the letter l and press &lt;ENTER&gt;. 

{% highlight bash %}
$ l
{% endhighlight %}  

__What happens? &rarr;__

<div class="incremental" markdown="block">
{% highlight bash %}
-bash: l: command not found
{% endhighlight %}
</div>
</section>

<section markdown="block">
### More Errors

Type ls foo and press &lt;ENTER&gt;. 

{% highlight bash %}
$ ls foo
{% endhighlight %}  

__What happens? &rarr;__

<div class="incremental" markdown="block">
{% highlight bash %}
ls: foo: No such file or directory
{% endhighlight %}
</div>
</section>

<section markdown="block">
### __Activity__: Drills!

__Entering commands__ _flash cards_ x 5 (use set 1)

We'll do this together, then try downloading it yourself:

1. Download [drills.py](drills.py) to the home directory
2. Type python drills.py
3. When prompted for a number, enter 1
4. CTRL-C quits
</section>

<section markdown="block">
### __Lab__

[Entering Commands](lab-entering-commands.txt)

* Type each command (with arguments and flags) exactly
* Only press &lt;ENTER&gt; when instructed...
* &lt;TAB&gt;, &lt;ENTER&gt;, &lt;UP&gt;, &lt;DOWN&gt; are the actual keys!
* Paste answer or output below the dashed line (------------)

</section>

<section markdown="block">
### __Activity__: Drills!

...Aaaand... again!

__Entering commands__ _flash cards_ x 5 (use set 1)

We'll do this together, then try downloading it yourself:

1. Download [drills.py](drills.py) to the home directory
2. Type python drills.py
3. When prompted for a number, enter 1
4. CTRL-C quits
</section>

<section markdown="block">
## [Navigating the File System](file-system.html)
</section>
