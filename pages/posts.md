---
layout: page
title: List of All Posts
permalink: /posts/categories/
redirect_from:
  - /posts/
---

This page lists all of the other random posts on this site.

<br>

---

<br>

## Posts with Dates

The following posts have got a date attached to them.

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

---

<br>

## Posts Sorted by Categories

The following are posts that have been tagged with a certain category.

{% assign sorted_cats = site.categories | sort %}
<ul class="listing">
{% for category in sorted_cats %}
    {% capture category_name %}{{ category | first }}{% endcapture %}
    
    <li class="listing-seperator">{{ category_name | capitalize }}</li>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] reversed %}
        <li class="listing-item">
          <a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a>
        </li>
    {% endfor %}
{% endfor %}
</ul>
