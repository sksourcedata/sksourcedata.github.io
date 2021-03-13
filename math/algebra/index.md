---
layout: page
title: Álgebra
menu: math
permalink: /math/algebra/
---

<ul>
    {% for p in site.pages %}
        {% if p.menu == 'algebra' %}
            <li><a href="{{ p.url }}">{{ p.title }}.</a> {{p.description}}</li>
        {% endif %}
    {% endfor %}
</ul>