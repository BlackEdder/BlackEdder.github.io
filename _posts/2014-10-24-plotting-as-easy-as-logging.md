---
layout: post
title: "Plotting as easy as logging"
description: ""
category: programming 
tags: [plotcli,dlang,D]
---
{% include JB/setup %}

I've been frustrated with plotting for a number of years now. I mainly use plotting during simulations and it always feels to me like it should be as easy as logging some numbers to the command line. This frustration first let me to develop [RealTimePlot](https://gitorious.org/realtimeplot/), which is a C++ library that makes it straightforward to plot data with only a couple of lines if code. Still this left me slightly frustrated. Mostly because it was still easier to log some values to the console than to plot them because the console is always there. This was not helped by the fact that I undertook a major refactoring of the code and never finished that.

Recently I've gotten very interested in the D programming language so naturally I thought about writing another plotting library. This has resulted in [plotcli](https://github.com/BlackEdder/plotd). Plotcli is the result of many years of frustration and I hope to have finally cracked it by adhering to the unix philosophy. Instead of a library, plotcli is a standalone command line program that you feed data into. It will then try to plot this data in a sensible way. You can also provide it with information on the structure of your data either via command line switches or commands in the data file. See the [wiki](https://github.com/BlackEdder/plotd/wiki) for some examples.

Some pros of using a standalone program vs library:

- On multi core machines you automatically gain parallelism
- Data is still around, making it easy to (re)plot it in different ways without rerunning the simulation
- No need to create bindings for different languages

Plotcli is still in quite early stages of development, but it is shaping up well and bug reports/fixes and feature requests would be highly appreciated.
