---
layout: post
title: "Typical public transport times"
description: ""
category: 
tags: ["public transport","uncertainty"]
---
{% include JB/setup %}

As mentioned in the [previous post]( {% post_url 2015-02-24-public-transport-planning-and-uncertainty %} ) I wanted to spend some time exploring the different trade offs involved with chosing a route by public transport (in London). In that post I highlighted the differences in expected time of arrival, travel time and uncertainty around those times for the train, underground and bus. I have now performed some simulations combining the modes of transports to explore how these differences influence your total travel time.

![Combined transit times of different forms of transport. On the x axis are different combinations, with the 1st row the first type of transport and 2nd the following transport. Y axis gives an overview of the median travel time and the variance around the travel time, with the box indicating the first to third quartile of the data. The lines are the 2 and 98 percent confidence levels.]({{ site.url }}/assets/ov_time_examples.svg)

Looking at the figure the most interesting part is the difference in uncertainty. Clearly taking the tube is the most reliable way to get there in a certain time. Bus bus can be faster, but can also be much slower. As a result when choosing a route it is not only important to consider the average time it will take, but also the associated risk of being delayed.
