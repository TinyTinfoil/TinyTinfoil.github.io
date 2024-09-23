---
layout: page
title: Catagories
permalink: /tags/
---
{% for item in site.tags %}

<div>
<h1>Articles tagged with "{{ item[0] }}"</h1>
<ul style='padding-top: 16px;'>

{% for post in item[1] %}
    <li><a href="{{ post.url }}">{{ post.title }}</a>, published {{ post.date | date: "%Y-%m-%d" }}</li>
{% endfor %}
</ul>
</div>
{% endfor %}