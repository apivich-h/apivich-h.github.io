---
layout: page
title: Posts
permalink: /posts/
---

On this page I collate some of the posts I have published to the website.

<br>

## Posts with Dates

The following posts have got a date[^1] attached to them.

<ul class="listing">
<!-- <li class="listing-seperator">Posts with Dates</li> -->
{% for post in site.posts %}
  {% if post.is_dated %}
    {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
    <li class="listing-item">
      <time datetime="{{ post.date | date:"%Y-%m-%d" }}">[{{ post.date | date:"%Y-%m-%d" }}]</time>
      <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}

<!-- <li class="listing-seperator">Undated</li>
{% for post in site.posts reversed %}
  {% if post.is_dated != true %}
    <li class="listing-item">
      <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %} -->
</ul>

<br>

## Selected Posts By Category

The following are posts from some selected categories.

{% assign sorted_cats = site.highlight_categories | sort %}
<ul class="listing">
{% for category_name in sorted_cats %}
    <!-- {% capture category_name %}{{ category | first }}{% endcapture %} -->

    <li class="listing-seperator">{{ category_name | capitalize }}</li>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] reversed %}
        <li class="listing-item">
          <a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a>
        </li>
    {% endfor %}
{% endfor %}
</ul>

<br>

For the list of all posts (including other non-academic ones not listed here), see <a href="/posts/categories">here</a>.

<br>

---

<br>

[^1]: As in _day, month and year_ date and not _I have an appointment with someone_ kind of date.