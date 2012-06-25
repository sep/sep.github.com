---
layout: post
title: "head to tail"
category: shell
tags: [shell, head, tail]
date: 2012-06-25 07:00:00
author: jonfuller
---
{% include JB/setup %}

Shell (~bash) - OS X, Windows, Linux

Use `head` or `tail` to dump the beginning, or end of a file, respectively, to `STDOUT`.

The default number of lines to show for both `head` and `tail` is 10.

For example, say you've got a log file and you'd like to see the first five entries, to make sure it's from the session you're trying to debug:

     head -5 /path/to/log.txt

     > 2012-06-07 05:45:23 Application Started
     > 2012-06-07 05:45:25 Database Service Started
     > 2012-06-07 05:45:25 Login Service Started
     > 2012-06-07 05:45:26 HTTP Server Started
     > 2012-06-07 05:45:26 Waiting for HTTP Client Connections

Now, to look at the last 50, so we can see everything that led up to the event we care about:

    tail -50 /path/to/log.txt

     > -snip-
     > 2012-06-07 05:55:16 log log log... log log
     > 2012-06-07 05:55:19 more log stuff
     > 2012-06-07 05:55:19 KABOOM!
    
I use `head` and `tail` quite a bit to look at the beginnings and ends of files (particularly long XML files) so I can make the right data is being sent at the beginning and end of the file.
