---
layout: post
title: "output pipe"
category: shell
tags: [shell, pipe, stdout]
date: 2012-06-13 10:00:00
author: jonfuller
---
{% include JB/setup %}

Shell (~bash) - OS X, Windows, Linux

As mentioned [last time](http://sep.github.com/shell/2012/06/11/input-pipe), many command line tools consume and/or produce text.

Even more useful than piping things into a program from a file, is piping things out of a program; either into another program, or into a file.

Take the previous example of gzipping an xml document.

    gzip -c < thexmlfile.xml

Looking at the output of that, is going to be pretty unfriendly (actually, gzip tries to protect you from doing this to yourself, because it will likely start doing all sorts of wacky stuff to your terminal).  What to do?

Output it to a file:

    gzip -c < thexmlfile.xml > thexmlfile.gz

Now you've got a gzipped version of that xml file.

The `>` operator is the key there.  That operator takes anything that is output from a program on `stdout` and puts it into the specified file.  If that file exists already, it'll be overwritten.  I use this constantly when doing builds from the command line because I always want to be able to go back and search through the build output for any errors or warnings that happened.

Use `>>` if you'd like to append instead of overwrite.

What about `stderr`?  Try using `2>`.
