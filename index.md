---
title: "ICT balie"
---

# ICT-balie

<input id="searchbarInput" class="search-bar__input">

<script src="https://unpkg.com/simple-jekyll-search@latest/dest/simple-jekyll-search.min.js"></script>
<script>
    var sjs = SimpleJekyllSearch({
        searchInput: document.getElementById('searchbarInput'),
        resultsContainer: document.getElementById('searchbarOutput'),
        json: '/assets/data/search.json'
    });

    document.querySelectorAll("span.tag").forEach(el => {
        el.addEventListener("click", e => {
            let val = e.target.innerHTML;
            document.querySelector("#searchbarInput").value = val;
            console.log(e.target);

            let event = new Event('input', {
                bubbles: true,
                cancelable: true,
            });
            document.querySelector("#searchbarInput").dispatchEvent(event);
        });
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