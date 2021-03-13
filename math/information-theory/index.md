---
layout: page
title: Teoría de la información
menu: math
permalink: /math/information-theory/
---

<ul>
    {% for p in site.pages %}
        {% if p.menu == 'information-theory' %}
            <li><a href="{{ p.url }}">{{ p.title }}.</a> {{p.description}}</li>
        {% endif %}
    {% endfor %}
</ul>