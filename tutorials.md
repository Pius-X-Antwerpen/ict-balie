---
title: "ICT balie"
layout: tutorial
activity: tutorials
---

# ICT-balie

<ul id="tutorials-overview">
    {% for tutorial in site.tutorials %}
    <li class="bg-complement elevated-low rounded">
        <a href="{{site.baseurl}}{{ tutorial.url }}">{{ tutorial.title }}</a>
        <p>{{ tutorial.excerpt }}</p>
    </li>
    {% endfor %}
</ul>