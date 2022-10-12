---
title: "ICT balie"
---

# ICT-balie

<ul>
{% for tutorial in site.tutorials %}
    <li>
        <h3>
            <a href="{{ tutorial.url }}">{{ tutorial.title }}</a>
        </h3>
        <article>{{ tutorial.excerpt }}</article>
    </li>
{% endfor %}
</ul>