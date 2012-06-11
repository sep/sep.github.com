---
layout: post
title: "input-pipe"
category: shell
tags: [shell, pipe, stdin]
date_parsed: 2012-06-11 10:00:00
author: jonfuller
---
{% include JB/setup %}

Shell (~bash) - OS X, Windows, Linux

Disclaimer: These pipes are to be used for tobacco only.

Most of the programs I use at the command line consume and/or produce text.  If you want to feed a program text that accepts input on `stdin`, I'll either pipe it in from the previous program, or pipe it in directly from file.

For example, if I'm `gzipping` up an xml file:

    gzip -c < thexmlfile.xml
    
This dumps the contents of `thexmlfile.xml` directly into the gzip program.  Alternatively, sometimes I need to feed gzip the output of some other program:

    cat thexmlfile.xml | gzip -c

This is functionally equivalent, but the `cat` part could really be any program that generates output, possibly an xml cleaning tool like `xmllint`.  The `|` passes any output from the previous command as input to the next command.
