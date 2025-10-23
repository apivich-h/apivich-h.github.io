---
layout: page
title: Archive of Past Updates
permalink: /updates/
---
<ul class="listing">
{% for entry in site.data.notices %}
  <li class="listing-item">
    <time>[{{ entry.time }}]</time>
    {{ entry.text }}
  </li>
  <br/>
{% endfor %}
</ul>