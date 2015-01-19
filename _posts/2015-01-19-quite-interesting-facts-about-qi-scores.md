---
layout: post
title: "Quite Interesting facts about QI scores"
description: ""
category: 
tags: []
---
{% include JB/setup %}

The game show QI has a very interesting [(and well documented)](http://qi.com/behind-the-scenes/bts-scoring/) scoring system, but I've always felt QI could easily be "gamed". For those of you who don't know QI, it is a popular game show with Stephen Fry and Alan Davies. The whole show revolves around quite interesting facts and doesn't take itself seriously (it does take the facts seriously though). Because players lose points when they say the wrong thing I have always had the sneaking suspicion that the game could easily be "gamed" by not saying anything, so let's take a closer look at the scores.

## Relation between scoring and talking

First, let's explore whether saying more really results in lower scores. For this I needed the amount people were talking (represented by total number of characters in their sentences) and their scores. Luckily I found [this](http://qitranscripts.com) website with transcripts and [another](http://qiscoreboard.com/) website with all QI scores from all the episodes. I am afraid the transcripts only cover the first 8 series though, so I don't have all the data. If we plot these and perform a linear regression (with R) we get the following picture:

![Scores as dependent on amount the contestants say. Results from linear regression is shown as a red line]({{ site.url }}/assets/post5_regression.png)

Although the relationship is fairly weak, it is (statistically) highly significant, showing that saying less and having a higher score are correlated.

<div id="contentBox" style="margin:0px auto; width:100%" class="clearfix">
<div id="column1" style="float:left; margin:0; width:60%;">
Next up is my theory that, given that most people score negative points, saying nothing is a winning strategy. For this we only need the data from the scores, so I can use data from all the seasons. The table shows what place you would end up in if you were the silent 5th player. As we can see the percentage of winning is actually quite small (13.8%); most probably you would end up in 2nd or 3rd place. The probability of losing completely is also tiny though, because there have been only a handful of shows where everyone ended up with a positive score. All in all it appears that I was actually wrong. While gaming the system by saying nothing would ensure you wouldn't end in last place, you would also not win that often. 
</div>
<div id="column2" style="float:left; margin:0; width:10%;"></div>
<div id="column5" style="float:right; margin:0; width:30%;">

+------+------------+
| Rank | Silent |
+======+============+
| 1    | 13.8%      |
+------+------------+
| 2    | 35.2%      |
+------+------------+
| 3    | 35.2%      |
+------+------------+
| 4    | 13.1%      |
+------+------------+
| 5    | 2.7%       |
+------+------------+

</div>
</div>
<!--Below solves layout issues-->
<div class="container">
  <div class="row">
    <div class="col-md-4"></div>
    <div class="col-md-4"></div>
    <div class="col-md-4"></div>
  </div>
</div>

## Alan Davies (permanent panel member)

![]({{ site.url }}/assets/post5_alan.png)

Finally, lets take a look at Alan's performance over time. Since Alan is a permanent member we have his scoring data over time. On the left hand side we have his actually scores, with a running average (black line) and the right hand side the running average of the actual position he ended up in (lower is better). From the scores we can see that he started out quite good, then the scores got lower and slowly started rising again from show 40 onward. If we look at his rank every game there seems to be clear improvement over time. The apparent discrepancy of higher scores in the beginning but worse rankings is presumably because all other players also scored higher in the beginning.

This leads us to a frightening conclusion: if Alan keeps going like this he might end up winning every week :)

Hope you found this short overview quite interesting! If people have suggestion on other possible interesting facts in the data feel free let me know :).


