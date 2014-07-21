---
layout: page
title: Search
permalink: /search/
---

<div class="search">
  <form action="/search" method="get">
  <input
    type="text"
    id="search-query"
    name="q"
    placeholder="Search..."
    autocomplete="off">
  </form>
</div>

<section id="search-results" style="display: none;">
  <div class="entries">
  </div>
</section>

{% raw %}
<script id="search-results-template" type="text/mustache">
  {{#entries}}
    <div>
      {{#date}}
        <time datetime="{{pubdate}}" pubdate>{{displaydate}}</time>
      {{/date}}
      <span><a href="{{url}}">{{title}}</a></span>
    </div>
  {{/entries}}
</script>
{% endraw %}
