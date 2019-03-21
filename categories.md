---
layout: page
title: Categories
permalink: /categories/
---

<section>
{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
<h3>{{ category | first }}</h3>
<ul id="{{ category[0] }}">
{% for post in category.last %}
<li>
<span>{{ post.date | date:"%Y-%m-%d" }}</span>
<a href="{{ post.url | relative_url }}">{{ post.title }}</a>
</li>
{% endfor %}
</ul>
{% endfor %}
</section>

