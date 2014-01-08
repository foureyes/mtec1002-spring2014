---
layout: default
title: Media Tech Skill 2 - MTEC 1002 - Spring 2014
nav-state: index
---
<a name="contact-info"></a>

Course Information
====
* __Course Number:__ {{site.course_number}}
* __Semester:__ {{site.course_semester}}
* __Section:__ 931

<a name="contact-info"></a>

Contact Information
====
* __Instructor:__ Joe Versoza
* __Email:__ jversoza at citytech.cuny.edu
* __Course Schedule:__ Wednesdays 6:00 to 8:30
* __Room:__ Voorhees 321


<!--

<a name="grading"></a>

Grading
====
Each __lab__ is worth 6 points:

* 4 points for lab work
	* 1 point - submitting anything / compiles (where applicable)
	* 2 points - less than half work
	* 3 points - 3/4 work
	* 4 points - all work
	* 5 points
* 1 point for lab quiz
	* 
	* 
	* 

Structure
====
* follow along 
* do on your own
* review
* follow along 
* do on your own
* review
* quiz  - (10 questions?)

* onboarding
	* create git account
	* give thumb drive
	* add key to test server
* thumb drives 
	* contain ssh key
	* maybe vm
	* given out on ???
	* check generated key by sshing to known server
* ssh and keys?
* use encrypted keys?
* you can use your own key
* http://macnugget.org/projects/publickeys/
* what's a text file?
* folders / tree structure on fs
* javscript
	* interpreted vs compiled
	* how programming languages "work"
	* how does processing work?
* vms
	* what's a vm?
-->

<a name="topics"></a>

Topics
====

<h4 class='module-title'>Module 1 - Command Line</h4>

* __Week 1 - January 29th__ - File System, Folders, Command Line Basics
* __Week 2 - February 5th__ - Output, Download, Compress/Archive, Uncompress/Unarchive
* __Week 3 - February 19th__ - Working with Files

<h4 class='module-title'>Module 2 - Source Code Management, Collaboration</h4>

* __Week 4 - February 26th__ -  Version Control Basics: init, add, commit, status, diff (assumes some knowledge of Processing)
* __Week 5 - March 5th__ - Review of Basic git Commands, Remote Repositories
* __Week 6 - March 12th__ - Branching and Merging

<h4 class='module-title'>Module 3 - JavaScript</h4>

* __Week 7 - March 19th__ - JavaScript Basics 1
* __Week 8 - March 26th__ - JavaScript Basics 2
* __Week 9 - April 2nd__ - JavaScript Basics 3

<h4 class='module-title'>Module 4 - JavasScript</h4>

* __Week 10 - April 9th__ - JavaScript Basics 4
* __Week 11 - April 23rd__ - JavaScript Basics 5
* __Week 12 - April 30th__ - JavaScript Basics 6

<h4 class='module-title'>Module 5 - Publishing on the Web</h4>

* __Week 13 - May 8th__ - Communicating with a remote server / publishing to the web (assumes some knowledge of HTML/CSS)
* __week 14 - May 14th__ - Github Pages
* __week 15 - May 7th__ - Administering a Server 

<a name="resources"></a>

Resources
====
* [Command Line Crash Course](http://cli.learncodethehardway.org/book/)
* [LinuxCommand.org](http://linuxcommand.org/lc3_resources.php)
* [Pro Git](http://git-scm.com/book)
* [Eloquent JavaScript](http://eloquentjavascript.net/)

<a name="lab"></a>

Lab Policy
====
1. No food or beverages at any time.
2. Do not modify desktop settings and do not leave any files on the desktop.
3. Locate all of your work in the assigned student folder.
4. No installation of software unless working with an instructor.
5. You are responsible for keeping all of your files on portable storage media. We cannot promise your files will remain from one class to the next.
6. Lab is reserved for students enrolled in MTEC or ENT courses.
7. Open lab hours are posted and subject to change.




<script>
$(document).ready(function() {
	var m = $('.module-title')
	$('.module-title + ul li').click(function () {
		var m = $(this).find('>ul');
		m.toggle();
		return false;
	});
});
 
</script>


