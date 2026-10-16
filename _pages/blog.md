---
layout: page
title: Blog
permalink: /blog/
section_number: "06"
---

<div class="page-grid research-intro"> <div class="page-label"></div>

<div class="page-content"> <p class="research-lead">News, views and updates from the lab.</p> </div> </div>



<article itemscope itemtype="http://schema.org/BlogPosting">
  <h1 itemprop="name headline">{{ page.title | escape }}</h1>
  <p class="text-muted" style="font-size: 0.875rem;">
    <time datetime="{{ page.date | date_to_xmlschema }}" itemprop="datePublished">{{ page.date | date: "%b %-d, %Y" }}</time>
    {% if page.author %} &middot; <span itemprop="author">{{ page.author }}</span>{% endif %}
  </p>
  <div itemprop="articleBody">
    {{ content }}
  </div>
</article>
