---
layout: post
title: "Piping to a plot"
description: ""
category: programming 
tags: [plotcli,dlang,D,pipe]
---
{% include JB/setup %}

In a [previous post]({% post_url 2014-10-24-plotting-as-easy-as-logging %}) I talked about an interesting new project I was working on that allowed one to pipe output from another program into a plotting program. The [plotting](https://github.com/BlackEdder/plotd) program will interpret the incoming data and plot it to a png file. This allows one to set up a permanent named pipe and listens to that as follows:
````
mkfifo /path/to/pipe
plotcli -f < /path/to/pipe
````
I find this very interesting, because in theory it would mean we can just throw any data at this pipe and have it plot it. Of course there are a number of practical problems with this, that make it not immediately practical. Mainly due to the fact that plots often need a lot of context. I.e. what kind of data is this. How should it be interpreted? Should this data start on a new plot or be part of the previous plot etcetera. Currently with [plotcli](https://github.com/BlackEdder/plotd) it is possible to provide this context using plotcli specific messages (i.e. #plotcli -d x,y). This is far from ideal though, because it largely defeats the object of making it very easy to plot any kind of data.

I wonder whether there are easier ways of doing this. It is probably possible to make educated guesses about what is meant most of the time. Still it is notoriously difficult to make a system that is both good at interpreting your meaning and easy to extend/improve. I'm open to suggestions :)



