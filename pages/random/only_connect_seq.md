---
layout: page
title: Only Connect - Fourth In The Sequence
permalink: /random/only_connect_seq
last_updated: 2022-05-10
---

Do you know _Only Connect_? It's a TV show hosted by Victoria Coren Mitchell that I watch even though I can answer less than 10% of the questions asked. I enjoy the show so much I made two pages on this site dedicated to the quiz format. 

This page is the _Fourth In The Sequence_ format - given the first three clues, can you figure out the fourth clue in the sequence?
- Clues 1, 2, 3 and 4 forms some sequence. Your goal is to figure out what comes 4th.
- To play, click on Clue 1 first, and try to guess what might come 4th. 
- If you don't know, click on Clue 2, and again guess what might come 4th. 
- If you still don't know, then click on Clue 3. 
- If you still don't know, you can get a hint based on the Category it is in, or you give up you can click to see the answer. 
- See Question 1 for an example.

You can also check out the other page for the _What's The Connection_ round <a href="/random/only_connect_conn">here</a>.

<br>

<table style="width:100%" id="ques-nav">

    <tr>
            <td colspan="10">
            Question Navigator - Click on a question number to go there
            </td>
    </tr>

    {% for q in site.data.only_connect_seqs %}

    {% assign num_mod = forloop.index | modulo:10 %}

    {% if num_mod == 1 %}
    <tr>
    {% endif %}

    <td width="10%">
    <a href="#question-{{forloop.index}}">Q-{{forloop.index}}</a>
    </td>

    {% if num_mod == 0 or forloop.last%}
    </tr>
    {% endif %}

    {% endfor %}
</table>

<br>
<br>

---

{% for q in site.data.only_connect_seqs %}

<br>

<details> 
<summary>
<h2 id="question-{{forloop.index}}" style="display:inline">Question {{forloop.index}}</h2>
{% if forloop.first %}
<br>
[<i>This question is an example for the formatting of the quiz.</i>]
{% endif %}
</summary>
<br>

<table style="width:99%">
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    <tr height="80px">
        <td>
            <details> 
            <summary>Clue 1</summary>
            {{q["Clue 1"]}}
            </details>
        </td>
        <td>
            <details> 
            <summary>Clue 2</summary>
            {{q["Clue 2"]}}
            </details>
        </td>
        <td>
            <details> 
            <summary>Clue 3</summary>
            {{q["Clue 3"]}}
            </details>
        </td>
    </tr>
    <tr height="120px">
        <td>
            <details> 
            <summary>Category</summary>
            <b>{{q["Category"]}}</b>
            </details>
        </td>
        <td colspan="2">
            <details> 
            <summary>Clue 4 (Answer)</summary>
            <b>{{q["Clue 4"]}}</b>
            <br>
            Connection: {{q["Connection"]}}
            </details>
        </td>
    </tr>
</table>
</details> 
<br>
<a href="#ques-nav">Back to question navigator</a>

<br>

---

{% endfor %}
