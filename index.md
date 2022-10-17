---
title: "ICT balie"
layout: tutorial
---

# ICT-balie

<ul id="blog-overview">
    {% for tutorial in site.tutorials %}
    <li class="bg-complement elevated-low rounded">
        <a href="{{ tutorial.url }}">{{ tutorial.title }}</a>
        <p>{{ tutorial.excerpt }}</p>
    </li>
    {% endfor %}
</ul>