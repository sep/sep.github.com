---
layout: post
title: "clipboard"
category: shell
tags: [shell, clipboard]
date: 2012-06-21 07:00:00
author: jonfuller
---
{% include JB/setup %}

Shell/cmd - OS X, Windows

Place text or program output onto the clipboard from your shell!

For OS X (the _pb_ stands for _pasteboard_):

    echo "hello world" | pbcopy

For Windows:

    echo "hello world" | clip

It works the same for both platforms with [input redirection](shell/2012/06/18/i-lied-redirection/) as well.  The following drops the contents of a file onto the clipboard:

    pbcopy < src/LICENSE.txt

You'll need to snag the Microsoft(tm) `clip` utility here: [http://www.petri.co.il/software/clip.zip](http://www.petri.co.il/software/clip.zip).

Another example?  Sure!  Glad you asked.  Want a list of all the files in the current directory that start with the letter 'A' and put that on the clipboard?

    ls | grep '^A' | pbcopy

This is way easier than having to go pick up the mouse and highlight + copy.

I'm sure there are ways to do this in Linux too, I'd be glad for you to tell me.  Have I mentioned that not only are contributions accepted, they're encouraged? (this is me encouraging you to contribute)

Happy clipboarding and contributing!
