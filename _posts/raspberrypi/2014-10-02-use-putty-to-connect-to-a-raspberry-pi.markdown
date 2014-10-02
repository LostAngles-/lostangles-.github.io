---
layout: post
title: "Use Putty to connect to a Raspberry Pi"
date: 2014-10-02 09:00
categories: rasbperrypi
meta: Use Putty on Windows to connect remotely to your Raspberry Pi. This is a good method to use if you want to use your Raspberry Pi as a headless server or media center. Use the Command Line/Terminal to add remote updates and new installations on your Raspberry Pi
author: LeeT
---

## Putty

[Putty][putty] is a very popular SSH connection application for Windows. Below is the _Putty_ interface:

![Putty]({{site.baseurl}}/img/ssh/putty.png) 

To Connect to you [Raspberry Pi](http://www.raspberrypi.org/) you would enter the **Host Name** (1) (either its name or its IP Address), the **Port** (2) (default for _SSH_ is 22), make sure the **Connection Type** (3) is _SSH_ and then once that is done click on the **Open** button (4)

You will get a prompt to accept the Remote Server, click **Yes**

### Putty Shell

Once you have done that, you will get the below Command Line Interface:

![Putty Shell]({{site.baseurl}}/img/ssh/putty-shell.png)

Now enter your Username (_Pi_ by default) then your Password. When you type in your password you wont see anything, dont worry this is normal, press the _Enter_ key once finished. If all has gone well you will get the below:

![Putty Log On]( {{ site.baseurl }}/img/ssh/putty-shell-log-on.png) 

Congratulations, you are Remotely Connected onto your [Raspberry Pi](http://www.raspberrypi.org/). Using SSH you can use the Server _Headless_, which basically means using it without a monitor.

To save your connection, simply enter a name into the **Saved Sessions** field and click **Save**. This will then drop your session into the box below it. Then next time simply highlight and click the **Load** button (or double click on the Saved Session name)


### Next time 

I will be doing a follow up to this tutorial, in which I will describe how to use a SSH Key instead of a password to connect to your [Raspberry Pi](http://www.raspberrypi.org/)...



[git]: http://git-scm.com/
[putty]: http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html