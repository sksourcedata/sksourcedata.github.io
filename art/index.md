---
layout: page
title: Arte
menu: main
permalink: /art/
---

<ul>
    {% for p in site.pages %}
        {% if p.menu == 'art' %}
            <li><a href="{{ p.url }}">{{ p.title }}.</a> {{p.description}}</li>
        {% endif %}
    {% endfor %}
</ul>