---
layout: post
title: "while"
category: shell
tags: [shell, stdin, bash, pipe, echo, awk, while, ps, cut]
date_parsed: 2012-10-XX 10:00:00
author: trimble
---
[%include JB/setup %]

Shell (~bash)

I mentioned in my `cut` post that fancy things like reodering fields are beyond `cut`'s built-in capabilities and that `while` was one potential solution. So, let's explore that a bit. (Man, I hope it turns out to be true!)

For simplicity's sake, let's start out with the same test file we had before (only with spaces instead of commas):

    % echo "1 red grumpy monday\n2 orange sleepy tuesday\n \
    > 3 yellow doc wednesday" > test.txt

As a quick reminder, `cut` will split the fields but not reorder them:

    % cut -f2,4 test.txt
    red monday
    orange tuesday
    yellow wednesday
    
    % cut -f4,2 test.txt
    red monday
    orange tuesday
    yellow wednesday

Enter `while` (and secretly `read`, we can get into that later if you want):

    % while read one two three; do echo $one $two; done < "test.txt"
    1 red
    2 orange
    3 yellow

And now for the magic...`read` sets up variables that we can use pretty much any way we want in the body of our `while` loop:

    % while read one two three; do echo $two $one; done < "test.txt"
    red 1
    orange 2
    yellow 3

    % while read one two three four; do echo "On" $four "I wear my" $two "pants."; done < "test.txt"
    On monday I wear my red pants.
    On tuesday I wear my orange pants.
    On wednesday I wear my yellow pants.

Sometime today, if you're not busy, experiment with `while`. It does one rather predictable thing...and it does it really well.