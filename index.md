---
title: "ICT balie"
---

# ICT-balie

<input id="searchbarInput" class="search-bar__input">
<div id="searchbarOutput></div>

<script src="https://unpkg.com/simple-jekyll-search@latest/dest/simple-jekyll-search.min.js"></script>
<script>
    var sjs = SimpleJekyllSearch({
        searchInput: document.getElementById('searchbarInput'),
        resultsContainer: document.getElementById('searchbarOutput'),
        json: '/assets/data/search.json'
    });
</script>

<ul>
{% for tutorial in site.tutorials %}
    <li>
        <h3>
            <a href="{{site.baseurl}}/{{ tutorial.url }}">{{ tutorial.title }}</a>
        </h3>
        <article>{{ tutorial.excerpt }}</article>
    </li>

    <hr>

{% endfor %}
</ul>