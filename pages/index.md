---
layout: page
title: Hello!
permalink: /
last_updated: 2026-10-01
---

## Recent Updates

<ul class="listing">
{% for entry in site.data.notices limit:5 %}
  <li class="listing-item">
    <time>[{{ entry.time }}]</time>
    {{ entry.text }}
  </li>
  <br/>
{% endfor %}
</ul>
For archive of all past updates, see <a href="updates">here</a>.

For more details about my current progress see <a href="works">my academic works</a> and <a href="/cv/cv.pdf">my CV</a>.

<!-- Also see [here](#social) for other updates from Twitter. -->

<br/>

---

<br/>

## About Myself

{% include image.html url="/images/profile.jpg" caption="Photo of myself (10 points if you know where this is)" width="320px" align="right" %}

Hello. I am Apivich Hemachandra (in Thai: อภิวิชญ์ ​เหมะจันทร), although I also go by my nickname[^1] "Kaotoo" (in Thai: ข้าวตู).

I am currently a Postdoctoral Associate at Singapore-MIT Alliance for Research and Technology (SMART), under the M3S IRG. Previously, I was a PhD student at the School of Computing at National University of Singapore (NUS), under the supervision of <a href="https://www.comp.nus.edu.sg/~ngsk/">See-Kiong Ng</a> and <a href="https://www.comp.nus.edu.sg/~lowkh/">Bryan Low Kian Hsiang</a>.

My general research interest is on data-efficient ML, especially on active learning (AL) and black-box optimisation (BBO). In particular, I am interested in two directions:

1. How **AL and BBO can be used to improve the efficiency of NN training**, particularly through the lens of training data, NN architecture, prior knowledge, and compute. These training components may also have inter-dependencies, making the optimal choice for them more difficult to determine. Because it's expensive to try out many potential NN training setup, we need to be a bit clever with what training setup we may want to try out.

2. How **we can evolve AL and BBO to be more efficient** through the use of existing prior knowledge and/or LLMs. This is particularly relevant in scientific domains, where we may have additional information which can be used to reduce how many experiments/simulations we need for AL or BBO. Because of the different form the prior knowledge can take up, and with the different choices we can make during experimentation/simulation, we may want to use cleverer systems to make these decisions for us rather than doing it manually.

Prior to my PhD, I completed my Bachelor's degree from Mahidol University International College (MUIC) in Thailand. I majored in Physics, however I also completed minors in Computer Science and Mathematics. My Bachelor's Thesis was related to <a href="/projects/thesis-u">data diversification and submodular maximisation</a>[^2]. I have also worked on different computer science-related projects with researchers in Thailand and in collaboration with local firms as a data analyst.

<br/>

___

<br/>

### Personal Life

{% include image.html url="/images/homepic.JPG" caption="A view of Chiang Mai from a rooftop" width="pw" align="top" enlarge=1 %}

<!-- <details>  -->
<!-- <summary><small>(Click to expand)</small></summary> -->
<!-- <br/> -->
I was born in Bangkok, however spent pretty much all of my childhood in Chiang Mai. I lived in Chiang Mai until I completed high school, before moving to Bangkok/Nakhon Pathom to complete my undergraduate degree. I have only been in Singapore since the start of my PhD (in 2021).
<!-- <br/><br/> -->

When I am not busy doing work, I enjoy playing and listening to music. I am a mediocre drummer, bassist and vocalist, and have been playing varying amounts of music since high school. My music taste isn't that varied (generally alternative, indie or some genres of pop), but I do discuss them somewhere on this website (you'll have to find it yourself though). If you meet me in person, feel free to discuss music or recent live gigs you've been to with me.
<!-- <br/><br/> -->

I enjoy watching football (or soccer as some may call it), and am a fan of Nottingham Forest (who <s>will hopefully be</s> <i>are now</i> in the Premier League <s>soon</s>).
<!-- <br/><br/> -->

<a href="/youtube">I also make maths videos whenever I have enough free time</a>.

<br/>

<!-- </details> -->

<!-- <br/> -->

---

<br/>

[^1]: _Apivich Hemachandra_ is my legal name, whereas _Kaotoo_ is my nickname (and not really legally recognised). You can check out the Thai naming convention <a href="https://en.wikipedia.org/wiki/Thai_name">here</a>, but in brief, _Apivich Hemachandra_ is for formal documents and more formal events, whereas _Kaotoo_ is what people would usually refer to me as in more casual settings. Both names were given to me by my parents at birth.

[^2]: I asked my physics department nicely enough and he allowed me to do a thesis on a topic related to computer science.
