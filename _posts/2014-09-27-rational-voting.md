---
layout: post
title: "Rational voting"
description: ""
category: 
tags: []
---
{% include JB/setup %}

In the [previous post]( {% post_url 2014-09-22-proportional-representation-vs-first-past-post-voting %} ) I gave a quick overview of the long term difference of proportional representation vs first past the post voting systems and I showed that first past the post voting systems result in less viable political parties in the long run. This is the because in first-past-the-post voting only the larger parties have any chance of getting any power. The way I incorporated that in the previous post was a bit of a hack, where I just assumed that this was the case, without any reasoning. Here I will look at why this is indeed the case for any rational voter.

## What does a rational voter want?

![Black points are the relative number of votes each party gets. Red points the number of votes weighted by the resulting power.]({{ site.url }}/assets/vote_power.png)

Naively one would think that what a voter wants is to vote for the party that most agrees with them, but ultimately a voter is interested in the power balance over all parties. Therefore, a rational voter should vote for the party that brings the balance of power most in line with his/hers viewpoint. This is also why people will vote for parties that wield more power, because those parties' influence on the balance of power is greater. The easiest way to define the balance of power is the average viewpoint of all parties weighted with their power.

![Number of viable parties over time under different voting systems.]({{ site.url }}/assets/post3_voting_history.png)

If we rerun the simulation using this measurement, we again get similar results in that proportional voting supports more parties than first past the post voting. One important factor though is how much people feel their vote is worth. If their vote is not worth much then also with proportional voting you only end up with two parties. Interestingly enough this is because people will only vote the fringe parties. This is because if the political power lies slightly to your right then the best way to influence it is to vote far left, because that will switch average power further to the left than voting for a party closer to you. 


![Number of viable parties dependent on the amount of influence a voter thinks he/she has.]({{ site.url }}/assets/post3_influence.png)

I have the feeling that this result is an artifact of only using one political axis. With more axes it become more difficult/impossible for this tug of war to happen, so we will have a closer look at this in the next post.
