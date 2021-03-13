---
layout: page
title: Matemáticas
menu: main
permalink: /math/
---

<ul>
    {% for p in site.pages %}
        {% if p.menu == 'math' %}
            <li><a href="{{ p.url }}">{{ p.title }}.</a> {{p.description}}</li>
        {% endif %}
    {% endfor %}
</ul>