---
layout: post
title: "Public transport planning and uncertainty"
description: ""
category: 
tags: ["public transport","uncertainty"]
---
{% include JB/setup %}

There are a plethora of public transport route planning apps available for every platform. They often do a good job of providing you with the fastest route, and/or with the route with the least stops. There is one feature that I have always missed though and that is an indication of the risk of taking a route. For example if I miss a connection what will my delay be like? Will I be stuck somewhere for at least half an hour? I plan on posting a series of blog posts exploring this question in more detail. Hopefully starting of with some simulation, theory and then applying it to some actual data on public transport.

## Background

I live in London and these posts will all be based on the situation in London. London has its own set of public transport and its own particulars. London has three main types of public transport:

Trains 
  ~ Reasonable regular time intervals. If you miss one you often have to wait for half an hour. Quite often delayed, but mostly a couple of minutes

Underground
  ~ Every 4-8 of minutes, missing one should only delay you for a bit.

Bus
  ~ Every 10-12 minutes. Officially on a schedule, but in London they don't really follow the schedule. Missing one won't cost you that much time, but the speed with which you get somewhere is very traffic dependent and so can't really be counted upon to get you somewhere within a specified amount of time.

As one can see these forms of transport have quite different types of uncertainty associated with them. For example bus and then train is quite risky, because the bus might be unexpectedly delayed due to heavy traffic and then you might miss your train, causing you to have to wait for a long time. In the next blog posts I will try to explore these different situations and hopefully devise a way to take this risk into account when planning your journey.
