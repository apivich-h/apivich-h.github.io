---
layout: page
title: Others
permalink: /others/
---
There are more interesting things I want to share, but I cannot fit them all in the navigation bar. So instead, I grouped them all together under the "Others" section. These pages are listed below.

{% for menu_item in site.data.menu %}
{% if menu_item.title == "Others" %}
{% for subcategory in menu_item.subcategories %}
<li><a href="{{ site.baseurl }}{{ subcategory.subhref }}">{{ subcategory.subtitle }}</a></li>
{% endfor %}
{% endif %}
{% endfor %}
