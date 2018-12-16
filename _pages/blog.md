---
layout: archive
title: "Blog Posts"
permalink: /blog/
author_profile: false
redirect_from:
  - /blog
---

## [1. How to train your MAML: A step by step approach](https://www.bayeswatch.com/2018/11/30/HTYM/)
{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != written_year %}
    <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
    {% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}