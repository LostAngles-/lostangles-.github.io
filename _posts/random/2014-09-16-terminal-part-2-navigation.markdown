---
layout: post
title: "Terminal - Part 2 - Navigation"
date: 2014-09-16 18:00:00
categories: random
meta: Terminal - Part 2 - Navigation. Learning how to navigate through directories/folders and how to move around
author: LeeT
---

The next part in our **Terminal** series is _Navigation_. Last time we viewed the data and learnt how to List the data in various different ways. Now we are going to learn how to Navigate between _Directories_

## Changing Directories

When you first log in, your location is `/home/pi`, we found out where we are using the `pwd` command. Lets first do a _Long List_ to see what we have

	pi@rpi-two ~ $ ls -l
	total 44
	drwxr-xr-x 2 pi pi 4096 Sep 17 08:50 Desktop
	drwxr-xr-x 3 pi pi 4096 Aug  1 19:48 Documents
	drwx------ 2 pi pi 4096 Sep  6 20:01 Downloads
	drwxr-xr-x 3 pi pi 4096 Aug  9 19:50 indiecity
	-rw-r--r-- 1 pi pi 2153 Jun 29 09:41 npm-debug.log
	-rw-r--r-- 1 pi pi 5781 Feb  3  2013 ocr_pi.png
	drwxr-xr-x 2 pi pi 4096 Aug  9 08:41 python
	drwxrwxr-x 2 pi pi 4096 Jan  1  1970 python_games
	drwxr-xr-x 2 pi pi 4096 Aug  1 19:48 Scratch
	drwxr-xr-x 3 pi pi 4096 Jun 28 15:41 wwwroot

The first column of the list, details what the data type is and permission levels

	drwxr-xr-x
	
The `d` tells us that it is a _Directory_, if there is a `-` this means it is just a file

	rwxr-xr-x
	
This is the permissions for the _Owner, Group and Others_, no need to worry about this right now

So we want to _Change Directory_ into the _Documents Directory_

	pi@rpi-two ~ $ cd Documents/
	pi@rpi-two ~/Documents $ 
	
So **cd** stands for **C**hange **D**irectory, then you type out the name of the _directory_ that you want to change into. UNIX/Linux is type sensitive:- so _Documents_ and _documents_ are 2 different things. One thing that you can use  is _Tab Completion_. So what you can do is type `cd Doc` and press the `TAB` key and it auto completes it for you. The File/Directory has to have a unique name though.

If I typed `cd D`, it would list me all of the Files/Directories that start with the letter D

	pi@rpi-two ~ $ cd D
	Desktop/   Documents/ Downloads/ 

When you  hange into a _directory_, you will notice that the _command prompt_ changes to show your new directory

	pi@rpi-two ~/Documents $
	
Then just do a quick `ls -t` to see what is inside of the Directory

	pi@rpi-two ~/Documents $ ls -l
	total 4
	drwxr-xr-x 2 pi pi 4096 Aug  1 19:48 Scratch Projects

So that was _navigating_ into a _directory_, there are a few things we can input after the `cd` command

| Command | Description |
| :---: | :--- |
|   ..   | Navigates up one directory |
|   ~    | The tilde navigates you to your home directory |
|   /    | Forward slash is the _root directory_, the highest directory |

So to navigate up one level we do the following

	pi@rpi-two ~/Documents $ cd ..
	pi@rpi-two ~ $ 

Notice that the prompt looses the word `Documents` as we have moved back up to our home directory. 

So if you wanted to _navigate_ to your **Documents** _directory_ from anywhere on you _Pi_, you would type

	pi@rpi-two ~ $ cd ~/Documents/
	pi@rpi-two ~/Documents $
	
This changes to the `~` _home_ of the current user, then into the `Documents` _directory_

So that is how easy it is to navigate in and out of _Directories_.





