---
layout: post
title: "Terminal - Part 1 - Directories & Content"
date: 2014-09-11 18:00:00
categories: random
meta: Terminal - Part 1 - Directories and Content. Learn how to find where you currently are, directory wise. Learn how to list directors to find out what content you have inside them.
---

The **Terminal** also known as **Command Line Interface** (**CLI**) can be a scary place if you dont know what you are doing. Once you get used to it, it starts to be logical and will become second nature.

Below is the **LXTerminal** from the [Raspbian Distribution](http://www.raspbian.org/)

![Terminal]({{ site.baseurl }}/img/terminal.png) 

When you first start the **Terminal** you are presented with the following:

	pi@rpi-two ~ $ 
	
The first part `pi` is your username you are logged on with. The second part `rpi-two` (in my case) is the name of the computer

## First Steps

To ease you in gently, lets find something about ourselves

	who am i

As the command suggests, it queries what user you are logged in as:	

	pi@rpi-two ~ $ who am i
	pi       pts/2        2014-09-13 21:44 (192.168.1.8)

This displays various information such as _Username_ `pi`, _Connection Type_ `pts/2` (0 is locally logged on, I am using ssh to connect remotely), _Date/Time_ `2014-09-13 21:44` and _IP Address_ `(192.168.1.8)`. 

## Directory Navigation

Whether you call them _Folders_ of _Directories_ they are the same thing:- basically a box that contains stuff. So lets figure how to navigate around.

### Where Am I ?

To find out where you are, type the following:

	pwd
	
**pwd** stands for **P**rint **W**orking **D**irectory. It will tell you which directory you are currently in

	pi@rpi-two ~ $ pwd
	/home/pi
	
By default when you log in, you log into the root of your user. In this case `/home/pi`

### Listing Directories

Great, now we know where we are, but is there any content inside of this directory ? To do this we will use the _List Directory Contents_ command `ls`. In the _Terminal_ type the following:

	ls
	
This will _list_ you the contents of your current directory

	pi@rpi-two ~ $ ls
	Desktop    Downloads  npm-debug.log  python        Scratch
	Documents  indiecity  ocr_pi.png     python_games  wwwroot
	
(I have a couple of extra directories, so dont worry if yours doesnt match exactly)

The `ls` command has some _options_	which changes the way the content is displayed:

	pi@rpi-two ~ $ ls -l
	total 44
	drwxr-xr-x 2 pi pi 4096 Sep  3 22:09 Desktop
	drwxr-xr-x 3 pi pi 4096 Aug  1 19:48 Documents
	drwx------ 2 pi pi 4096 Sep  6 20:01 Downloads
	drwxr-xr-x 3 pi pi 4096 Aug  9 19:50 indiecity
	-rw-r--r-- 1 pi pi 2153 Jun 29 09:41 npm-debug.log
	-rw-r--r-- 1 pi pi 5781 Feb  3  2013 ocr_pi.png
	drwxr-xr-x 2 pi pi 4096 Aug  9 08:41 python
	drwxrwxr-x 2 pi pi 4096 Jan  1  1970 python_games
	drwxr-xr-x 2 pi pi 4096 Aug  1 19:48 Scratch
	drwxr-xr-x 3 pi pi 4096 Jun 28 15:41 wwwroot
	
The `-l` switch, displays the content in a _long list_. Don't worry about the information displayed, we will discuss that later

Using the `-t` switch, puts them in _Date_ order, latest _Date_ at the top

	pi@rpi-two ~ $ ls -t
	Downloads  indiecity  Documents  npm-debug.log  ocr_pi.png
	Desktop    python     Scratch    wwwroot        python_games

So, if we combine both `l` & `t`, we get a _long list_ in _date_ order !

	pi@rpi-two ~ $ ls -lt
	total 44
	drwx------ 2 pi pi 4096 Sep  6 20:01 Downloads
	drwxr-xr-x 2 pi pi 4096 Sep  3 22:09 Desktop
	drwxr-xr-x 3 pi pi 4096 Aug  9 19:50 indiecity
	drwxr-xr-x 2 pi pi 4096 Aug  9 08:41 python
	drwxr-xr-x 3 pi pi 4096 Aug  1 19:48 Documents
	drwxr-xr-x 2 pi pi 4096 Aug  1 19:48 Scratch
	-rw-r--r-- 1 pi pi 2153 Jun 29 09:41 npm-debug.log
	drwxr-xr-x 3 pi pi 4096 Jun 28 15:41 wwwroot
	-rw-r--r-- 1 pi pi 5781 Feb  3  2013 ocr_pi.png
	drwxrwxr-x 2 pi pi 4096 Jan  1  1970 python_games
	
There are many more options, if you want to have a look, here are some websites:

+ [About.com](http://linux.about.com/od/commands/l/blcmdl1_ls.htm)
+ [Your Own Linux](http://www.yourownlinux.com/2014/01/linux-ls-command-tutorial-with-examples.html)




















