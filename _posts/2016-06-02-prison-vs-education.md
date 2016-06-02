---
title: "States spend much more per prisoner than per K-12 student"
layout: post
---

Inspired by [this tweet](https://twitter.com/robreich/status/737714695042306048), I went looking for a graph of state spending on students and on prisoners. I found a [couple](http://www.huffingtonpost.com/2014/06/11/prison-spending-education-spending_n_5484787.html) [graphics](http://money.cnn.com/infographic/economy/education-vs-prison-costs) which I felt could have been done better, so I made my own version.

I found state-by-state data on correctional department spending per prison inmate from [vera.org](http://www.vera.org/sites/default/files/resources/downloads/price-of-prisons-updated-version-021914.pdf) (see figure 4). I found roughly corresponding data on per-pupil K-12 education department spending from [the U.S. Census](https://www.census.gov/content/dam/Census/library/publications/2015/econ/g13-aspef.pdf) (see table 8).

It is important to note that the prison spending data is from 2010 but the education spending data is from 2013. Comparing across years like this is somewhat dangerous, because the economic and political climates in each state might be very different in those time periods. However, this is the best I could find. Also, there is complete data for only 40 states.

Here is the resulting graph:

<iframe width="900" height="800" frameborder="0" scrolling="no" src="https://plot.ly/~jnaecker/0.embed"></iframe>

Here's how to interpret the graphs: Each data point is one state. The x-axis is the state's corrections department spending per prisoner, while the y-axis is the state's education departments spending per student. If you hover over the state's data point, you can see the exact numbers for per-prisoner and per-pupil spending, as well as the ratio. 

The grey dashed lines indicate where the ratio of per-prisoner to per-student spending would be 1:1, 2:1, 3:1, and 4:1. Note that every state spends more per prisoner than they spend per K-12 student.  The highest ratio actually belongs to California, at 5.14:1. 

The code and data for this graph can be found [here](https://github.com/jnaecker/prison-vs-education).

