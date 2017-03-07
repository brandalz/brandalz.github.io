---
layout: post
title:  "TIL Vim Set Toggle"
date:   2017-03-07 17:10:31 +0700
categories: vim
---
I have been using vim for about 9 months now and I'm very happy with it. At this point I can say that I'm proficient in using vim but this doesn't make me to stop learning. Lately I bought two vim books, one is [Practical Vim](https://pragprog.com/book/dnvim2/practical-vim-second-edition) and the other one is [Painless Vim](https://leanpub.com/painless_vim). The first one is for advanced user I think and the later is for beginner.

I'm still reading Painless Vim even though this book is for new comer but I want to make sure that there is no basic knwoledge that I don't know. And in fact there is.

Went through several pages and I already found a basic trick using set command that I don't know before. If you vim user then you already know that we can use command in vim using `:` followed by the command itself, for instance `:set number`. This command will give you a line number on the editor. Usually a set command has its counterpart, if `:set number` will give us line number then what if we want to get rid of it? The answer is we use `:set nonumber` to dismiss the line number.

This is perfectly okay but what if (again) we want to be able to toggle between line number and no line number using only key binding?

Maybe if you know how to do some programming in vim using vimscript, which in this case I don't, you can use conditional to check which current condition is about the line number. If there is line number than change to no line number and if there is no line number change so that it appears on the editor.

For this case, I found a simple yet powerful solution in Painless Vim book. Just by adding a `!` on the command, it will toggle.

`:set number!`

How cool and simple is that?

One more thing I learned from that book regarding `set` command. If we append a question mark, it will echo the current setting.

`:set number?`

This will give us `number` if number line is shown and `nonumber` if it doesn't.
