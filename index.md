---
layout: page
title: Index
---

{% for category in site.categories %}
#{{ category.first }}
<ul>
    {% for post in site.posts %}
        {% if post.category == category.first %}
            <li><a href="{{post.url}}">{{ post.title }} - {{ post.date | date: "%B %-d, %Y" }}</a></li>
         {% endif %}
    {% endfor %}
</ul>
{% endfor %}
