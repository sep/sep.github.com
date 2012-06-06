---
layout: post
title : "history | grep"
description: ""
category: shell
tags: [shell, history, grep]
---
{% include JB/setup %}

Shell (~bash) - OS X, Windows, Linux

Pipe `history` into `grep` to search your past commands in a shell

    > history | grep unicorn
    > ... <snip>
    > 976  bundle exec unicorn -c config/unicorn/production.rb -E production -D
    > ... </snip>