---
layout: post
title: My First Week of Metis
---

## First week of bootcamp

After a couple months of anticipation, my data science bootcamp started a week ago. A week has felt like a month. The cohort has been put to task with our first project, which was due this last Friday.


## First Data Science Project
**The Project Premise**
The cohort was divided into groups to tackle a challenge. We were tasked with helping a fictional nonprofit in New York. "Women Tech Women Yes" was planning their annual fundraising gala. A key part of their outreach for promoting the event was sending teams to canvass at subways stations. WTWY wanted our help them more effectively place their teams.

**Where to start?**
We decided that it would be helpful if we could know which stations had the most people entering and exiting. With that we would know which stations to suggest to send the canvassing teams.

**Data Collection**
With a quick google search we were able to find [MTA turnstile data](http://web.mta.info/developers/turnstile.html). However, the easy part was over. We needed to get the numbers and letters to speak and tell us a story. With some deciphering, the turnstile code system became clear. An electronic counter was recorded every fours. The data entries would have numbers like the following:
```00:00:00 24355643  
04:00:00 24355654```
The difference in time recordings is easy to see. However the other column doesn't record how many people passed through the turnstile, but rather the number on the counter. A little more math is needed; we would just need to take the difference. It's easy enough to do one of these calculations by hand or by calculator :grin:. We needed to hundreds of thousands of these. Luckily we would write some code to do this.

**Analysis**
After looking at the data we found some interesting findings. Let's take a look at the total usage at Penn Station over 12 weeks. Each of these lines represents a week.

![PennStation12weeks]({{ site.url }}/images/pennstation.svg)

As one would expect the traffic drops on weekends.

![PennStationholidays]({{ site.url }}/images/pennstationaberations.svg)

There are two weeks that have slightly different curves. They are the weeks of Good Friday and Memorial Day.


We found the average daily usage for all the stations and the following graph is the top 15.

![TopStations]({{ site.url }}/images/topstation.svg)
