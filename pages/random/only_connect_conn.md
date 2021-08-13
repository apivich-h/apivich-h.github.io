---
layout: page
title: Only Connect - What's The Connection?
permalink: /random/only_connect_conn
---

Do you know _Only Connect_? It's a TV show hosted by Victoria Coren Mitchell that I watch even though I can answer less than 10% of the questions asked. I enjoy the show so much I made two pages on this site dedicated to the quiz format. 

This page is the _What's The Connection_ format - what's the connection between the four clues given?
- All four clues have a common connection, and your goal is to figure out what it is.
- To play, click on each clue one by one, starting from Clue 1. After each clue you clicked, see if you can figure out the connection amongst the clues.
- You can guess the connection before seeing all the four clues. The less clues you have seen when you correctly guess the connection, the better.
- If you have clicked all clues and still don't know, click on Category for a bit of a hint, or click on the answer for the connection of all the clues. 
- See Question 1 for an example.

You can also check out the other page for the _Fourth In The Sequence_ round <a href="/random/only_connect_seq">here</a>.

<br>

<table style="width:100%" id="ques-nav">

    <tr>
            <td colspan="10">
            Question Navigator - Click on a question number to go there
            </td>
    </tr>

    {% for q in site.data.only_connect_conn %}

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

{% for q in site.data.only_connect_conn %}

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

<table style="width:100%">
    <col width="25%" />
    <col width="25%" />
    <col width="25%" />
    <col width="25%" />
    <tr height="100px">
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
        <td>
            <details> 
            <summary>Clue 4</summary>
            {{q["Clue 4"]}}
            </details>
        </td>
    </tr>
    <tr height="100px">
        <td>
            <details> 
            <summary>Category</summary>
            <b>{{q["Category"]}}</b>
            </details>
        </td>
        <td colspan="3">
            <details> 
            <summary>The Connection (Answer)</summary>
            <b>{{q["Connection"]}}</b>
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
