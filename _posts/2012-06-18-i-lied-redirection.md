---
layout: post
title: "I Lied: Redirection"
category: shell
tags: [shell, redirection, pipe, stdout, stdin, stderr]
date: 2012-06-18 09:00:00
author: jonfuller
---
{% include JB/setup %}

Shell - OS X, Windows, Linux

I lied.  Twice.  Well, probably more than that, but specifically about [input](shell/2012/06/11/input-pipe/) and [output](shell/2012/06/13/output-pipe/).

These are really instances of input or output redirection.

We already covered that `<` is input redirection (I previously called this piping in from a file).

We also covered output redirection:

* `>` - redirect output to a file
* `>>` - redirect output and append to a file
* `2>` - redirect standard error to a file

Sometimes I'd like both `STDOUT` and `STDERR` to end up in the same file... check this out!

    grep * > outfile 2>&1

The `> outfile` portion is just like from before.  The `2>&1` portion says take `STDERR` (2) and point it at `STDOUT` (1).


Redirecting to a black hole:  

Redirect to `/dev/null` to send output into a black hole.

I use this when I'm running a program with lots of output that I don't care about (outputting to the screen is slow!).  Redirect it to `/dev/null` and it will be much faster.

