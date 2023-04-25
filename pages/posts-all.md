---
layout: page
title: List of All Posts
permalink: /posts/categories/
---

This page collates all of the posts on my website by category. A few of these are for purposes of sharing something interesting. Some others are just an excuse for me to write more non-academic things (to improve my writing in general).

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
