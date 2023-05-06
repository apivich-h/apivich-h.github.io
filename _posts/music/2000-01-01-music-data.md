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

Here are some things I found about myself:

- I listen to way too much Coldplay and Keane. While there are some times when they dip a bit in terms of how much I listen to them, I still listen to them significantly enough all this time. I should get new music.

- You can really see when I started to get into Paramore and Radiohead, being two of the bands that entered my music library in 2019 and then continued to stay there. Also you can start to see that at around 2023, there seems to be a larger shift in what artists I listen to (or at least start to listen to according to the charts).

- My music taste isn't _that_ diverse, mainly shown by the fact that the data is since 2017 but only a handful of (mostly quite mainstream) artists seem to have significant numbers.

I don't think the insights are that interesting to other people, but they definitely are for me and maybe for other people who knows how my music taste is like.

## How monotone is my music taste?

Another thing I do suspect about myself is that I tend to listen to very few artists over and over again. This is the sense of the word _monotone_ I will use - that I just stick with listening to a few artists with little variety. I wanted to visualise that statistic about my listening habit.

For the plot, I use `plotly`, which allows for various interactive plots. Specifically, I used a stacked bar chart where I highlight the top 5 artists I listened to over each 4 month period. Each bar just shows how many times I listen to those artists as a proportion of all music plays I did over that period, with the top 5 artists being highlighted in the chart[^4].

{% include ext/music_data/chart.html %}

Based on the plot, I can see that (as of 2023) my music choices are becoming less diverse. During pandemic time (2020-2021ish) I started to explore more music a bit so was stuck less with the same artists. However, since around 2021 I have just found a few artists and stuck them on repeat. This also seems to be around when I entered grad school, so I'm not sure if there's anything to do with that or not (would be a reach to say otherwise to be honest).

---

[^1]: If you never tried downloading the collected data from some popular online websites or services you have an account at, you should. It is very interesting and also slightly disturbing to see what kind of things these services are tracking and how much data they have about you.

[^2]: Name omitted since I'm not being sponsored by these guys. Although if you dig around here enough you might be able to figure out who they are.

[^3]: I did some normalising and smoothing of the data. Basically, the height of the histograms is number of listens for a certain artist divided by the maximum number of listens for any one artist at that timestep. Given this I then then apply a convolution to smooth the curve a bit.

[^4]: I used a hacky trick where each of the Others bar are actually made up of multiple smaller bars, so that only the artists who are in my top-5 most listened to in that time period having a non-white colour (which matches the stacked histograms from the previous chart).
