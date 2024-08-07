---
layout: post
title: Plotting My Music Listening Data
last_updated: 2023-04-14
category: music
---
I got bored enough to download all my music streaming data and plotting the data out[^1]. I started to use a certain music streaming platform[^2] regularly to listen to my music since around 2018 (previously I would go on a few places that didn't record my listening data in as much of a detail), so much of the data analysed are since then.

Because people may be expecting my blog to be somewhat educational (I don't know why you would though), I will also describe briefly how each of the charts are made. If you are interested in data visualisation (like I somewhat am), these may inspire you.

## Who did I listen to in the past?

{% include image.html url="/images/blog/music_data/pop.png" caption="Music chart" width="25%" align="right" enlarge=1 %}

I used a wonderful package called `joypy` (named after the band Joy Division who are partially known for <a href="https://en.wikipedia.org/wiki/Unknown_Pleasures">their famous album cover</a>), which specialises in making stacked histogram plots.

The height of each histogram roughly represents how much I listen to the artist in question [^3]. I only select some artists to plot, mainly the ones who I have a significant enough number of plays at some time period in the past.

The plot is shown on the right (or at least so on desktop). You can click on the chart to enlarge it.

## How monotone is my music taste?

Another thing I do suspect about myself is that I tend to listen to very few artists over and over again. This is the sense of the word _monotone_ I will use - that I just stick with listening to a few artists with little variety. I wanted to visualise that statistic about my listening habit.

For the plot, I use `plotly`, which allows for various interactive plots. Specifically, I used a stacked bar chart where I highlight the top 5 artists I listened to over each 4 month period. Each bar just shows how many times I listen to those artists as a proportion of all music plays I did over that period, with the top 5 artists being highlighted in the chart[^4].

{% include ext/music_data/chart.html %}

---

[^1]: If you never tried downloading the collected data from some popular online websites or services you have an account at, you should. It is very interesting and also slightly disturbing to see what kind of things these services are tracking and how much data they have about you.

[^2]: Name omitted since I'm not being sponsored by these guys. Although if you dig around here enough you might be able to figure out who they are.

[^3]: I did some normalising and smoothing of the data. Basically, the height of the histograms is number of listens for a certain artist divided by the maximum number of listens for any one artist at that timestep. Given this I then then apply a convolution to smooth the curve a bit.

[^4]: I used a hacky trick where each of the Others bar are actually made up of multiple smaller bars, so that only the artists who are in my top-5 most listened to in that time period having a non-white colour (which matches the stacked histograms from the previous chart).
