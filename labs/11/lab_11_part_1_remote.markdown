---
layout: lab
title: Lab 11, Part 1 - Remote Server
prefix: ../../
---
# Lab 11, Part 1 - Remote 

## Overview

* create three files to upload to a remote server  
* connect to a remote server
* run commands on remote server
* upload files to remote server using scp and sftp

## Instructions

### Cleaning Up

* close terminal

### Prep Work

* if it's not already created, make a directory on your desktop with your first initial and last name
	* it should be __~/Desktop/username/__
	* do this using terminal
* in terminal change to your __~/Desktop/username/__ folder
* use pwd to verify that you're in the correct folder
	* you should be in __~/Desktop/username/__
	* if you're not, cd into it

### Fork and Clone

__Fork__

* log in to github.com
* open this url: https://github.com/MTEC1002/lab\_11\_part\_1.git
* click on fork
![fork](../../resources/img/github-fork.png)
* wait for it...
* you should now have a repository url that you can copy


__Clone__

* copy the url from __your__ newly forked repository
* it should look something like: __https://github.com/yourusername/lab\_11\_part\_1.git__
* if you don't see your repository url...
	* click on your user name on the upper right corner
	* click on the repositories tab in the center of the page
* click on the repository named lab\_11\_part\_1
* open terminal
* use __pwd__ to make sure that you're in __~/Desktop/username__ 
	* if you're already in this folder, then you're fine!
	* otherwise, you may be one folder in; if you are, __cd ..__ 
* clone this repository 
{% highlight bash %}
git clone https://github.com/yourusername/lab_11_part_1.git
{% endhighlight %}

__Configuration__

* cd into the directory that you just cloned
{% highlight bash %}
cd lab_11_part_1
{% endhighlight %}
* use __pwd__ to make sure that you're in __~/Desktop/username/lab\_11\_part\_1__ 
* use git config to set the name and email that you want displayed on your commits
{% highlight bash %}
git config user.name  "your name!"
git config user.email your@email.address
{% endhighlight %}


### Create Four Text Files

* using TextWrangler, create the following files:
	* one.txt
	* two.txt
	* three.txt
	* proof.txt
* in one.txt, type in, without quotes: "uploaded with scp"
* in two.txt, type in, without quotes: "uploaded with commandline sftp client"
* in three.txt, type in, without quotes: "uploaded with graphical sftp client"
* in proof.txt, type in, without quotes: "Directory Listing on Remote Server"
* use git to check the __status__, __add__ to staging, and __commit__ ... don't forget the __-m 'message'__ part (don't worry about using git push until the end)


### Running Commands on a Remote Server

* open terminal
* use ssh to connect to a remote server using your username and your ip address as the host
{% highlight bash %}
ssh yourusername@your.ip.address
{% endhighlight %}
* you'll be asked for a password... and once you're authenticated, you will have a prompt on the remote server
* use ls to list all of the files (there should be none!)
* try running the following commands on the remote server:
	* whoami
	* who
* keep this terminal open type CONTROL+D to log out

### Using scp to Upload a File

* open a __new__ terminal
* change your directory to your lab directory: __~/Desktop/username/lab\_11\_part\_1__ 
* use __pwd__ to make sure that you're in __~/Desktop/username/lab\_11\_part\_1__ 
* use ls to show that all of your text files are present
{% highlight bash %}
{% endhighlight %}
walsh-9:jversoza joe$ ls -l
total 8
-rw-r--r--  1 joe  staff  4 Apr 17 08:10 one.txt
-rw-r--r--  1 joe  staff  0 Apr 24 08:58 proof.txt
-rw-r--r--  1 joe  staff  0 Apr 24 08:58 three.txt
-rw-r--r--  1 joe  staff  0 Apr 24 08:58 two.txt
* upload one.txt to your remote server using __scp__
{% highlight bash %}
# scp [/path/to/local/file] [remote-username]@[remote-hostname]:[/path/to/remote/file]
scp one.txt yourusername@your.ip.address:~
{% endhighlight %}
* in the terminal window that's logged in to your remote server, type ls to show that the file is present on your remote server
	* you should have a single file: one.txt

### Use a Commandline SFTP Client to Transfer Files

* switch back to the terminal window that's __local__
* use __pwd__ to make sure that you're in __~/Desktop/username/lab\_11\_part\_1__; if you're not, cd into it 
* type in __sftp__ with your username@remotehost to start up the commandline sftp client; it will give you a prompt that's waiting for commands
{% highlight bash %}
# sftp [username]@[remote host]
sftp root@your.ip.address
{% endhighlight %}
* type in __lpwd__ after the prompt to determine what __local directory__ you're in
{% highlight bash %}
sftp> lpwd
{% endhighlight %}
* you should be in lab_11_part_1:
{% highlight bash %}
Local working directory: /Users/student/Desktop/yourusername/lab_11_part_1
{% endhighlight %}
* type in __pwd__ after the prompt to determine what __remote directory__ you're in
{% highlight bash %}
sftp> pwd
{% endhighlight %}
* you should get something like
{% highlight bash %}
Remote working directory: /root
{% endhighlight %}
* use __lls__ to list the files that you have locally 
{% highlight bash %}
sftp> lls
{% endhighlight %}
* you should see your three text files
* use __put__ to upload one of your local files to your remote server
{% highlight bash %}
sftp> put two.txt
{% endhighlight %}
* you should get feedback similar to the following:
{% highlight bash %}
Uploading two.txt to /root/two.txt
two.txt   
{% endhighlight %}
* in the terminal window that's logged in to your remote server, type ls to show that the files are present on your remote server
	* you should have two files: one.txt and two.txt

### Use a Graphical SFTP Client to Transfer Files

* on your local workstation...
* download this SFTP client: [http://cyberduck.ch/Cyberduck-4.2.1.zip](http://cyberduck.ch/Cyberduck-4.2.1.zip)
* unzip it (it might automatically be extracted for you)
* move the CyberDuck up to the desktop
* double click on it to run it
* click on open connection
![sftp-open.png](../../resources/img/sftp-open.png)
* look for the drop down that says __FTP__
![sftp-ftp.png](../../resources/img/sftp-ftp.png)
* change it so that it is __SFTP__
![sftp-sftp.png](../../resources/img/sftp-sftp.png)
* uncheck add to keychain
![sftp-keychain.png](../../resources/img/sftp-keychain.png)
* put in the domain (your ip address!), username and password
* once you've contected, you should see the two files that you've already created
* open finder and browse to your lab directory
* drag and drop both three.txt into CyberDuck to upload your file
* in the terminal window that's logged in to your remote server, type ls to show that the file is present on your remote server
	* you should have three files: one.txt, two.txt, three.txt
* in the same terminal window, type in hostname
* copy (use your mouse to highlight, command-C)  everything from ls through to the output of hostname
* using TextWrangler, open proof.txt
* paste your commands and their output
* save your work
* use git to check the __status__, __add__ to staging, and __commit__ ... don't forget the __-m 'message'__ part 
* finally, use git push origin master to send to remote repository
