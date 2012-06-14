---
layout: post
title: "windows shell"
category: shell
tags: [windows]
date_parsed: 2012-06-14 10:00:00
author: jonfuller
---
{% include JB/setup %}

Shell (~bash) - Windows

Every post so far has been a shell trick, and they all say they work on Windows.  What am I smoking?

There are several ways to get a decent (though still not first class) shell on Windows.  You owe it to yourself to use at least one of them.

## git-bash

Install yourself some [msysgit](http://code.google.com/p/msysgit/downloads/list), or better yet, [github for windows](http://windows.github.com/) or even [git extensions](http://code.google.com/p/gitextensions/).

Any of these will get you a pretty full-featured bash.  The latter two also come with a pretty nice [git](http://git-scm.com/) gui.

## cygwin

[Cygwin](http://www.cygwin.com/): Get that linux feeling on Windows. 

A layer on top of Windows that can act as a linux API.

If you're a linux geek and you're stuck on Windows, check this thing out.  You can buy me beer later.  You're welcome.

## gow

[Gnu-On-Windows](https://github.com/bmatzelle/gow).

The (not-so) new kid on the block.

A lightweight version of cygwin.  Really, just a bunch of the gnu binaries (think ls, find, grep, gzip, etc.) in a simple installer.



Yes, there are others, and oh yeah, [powershell](http://en.wikipedia.org/wiki/Windows_PowerShell), but I'm not going to talk about those.  If you'd like to, [just let me know](mailto:fullerjc+bitsandbytes@gmail.com).
