---
layout: post
title:  "Vim Color Broke on Tmux"
date:   2017-02-21 15:03:31 +0700
categories: vim
---

I've been wanting to use tmux on my daily job for quite some time ago since my job is heavily playing with terminal and moreover finally I'm a proud vim user now. I keep hearing from people that already using it that tmux is really helpful and it makes their day to day routine working with terminal better.

Fast forward, I managed to learn tmux using [this great tutorial](http://blog.hawkhost.com/2010/06/28/tmux-the-terminal-multiplexer/), thanks to the author. Everyhting was fine until I opened vim and these ugly colorscheme appeared.

![broke vim in tmux]({{site.url}}/assets/images/old.png)

Well maybe it's not that ugly but compared to my supposed to be vim as shown in screenshot below you can judge it that the later is better at least for my personal preference. As you can see, vim airline on the first image is crappy, the tab line is worse as I don't have any information on which buffer I'm working on just by seeing it. I have no clue which tab line is active. And it's not just that, by comparing those two images the color of vim is totally different.

![vim in tmux]({{site.url}}/assets/images/new.png)

To address this problem I went to goole and found this useful trick. Adding this single line to your `.bashrc` or `.zshrc` if you are using zsh shell will solve the problem.

{% highlight ruby %}
export TERM=screen-256color
{% endhighlight %}
