---
layout: post
title: "follow your tail"
category: shell
tags: [tail, shell]
date: 2012-06-26 07:00:00
author: jonfuller
---
{% include JB/setup %}

Shell (~bash) - OS X, Windows, Linux

Riding the coat-tails of yesterday's [head and tail](http://sep.github.com/shell/2012/06/25/head-to-tail) post... is another `tail` trick.

Just like [Toucan Sam](http://en.wikipedia.org/wiki/Toucan_Sam) never said:

> Follow Your Tail

- Not Toucan Sam

Anyways, `tail -f` (the `f` is for _follow_) _follows_ a file as it is updated.

For example, say your application writes to a log file, and you'd like to watch the log as it gets appended to, without having to constantly hit _refresh_ in your editor.  Just pop open a terminal (or bash) and `tail -f /path/to/log.txt` and watch the log entries start rolling in!

Pretty slick if you ask me.  I'll even do this for unit test runs or builds that I [redirect](http://sep.github.com/shell/2012/06/18/i-lied-redirection/) their output to a file.  This way  the test or build runs faster since it doesn't have to output to the screen, but I can still watch the output in another terminal or tab window.
