---
title: "Blog"
layout: page
permalink: /blog/
section_number: "06"
---

<div class="page-grid research-intro">
  <div class="page-label"></div>
  <div class="page-content">
    <p class="research-lead">Notes, news and updates from the lab.</p>
  </div>
</div>

{% for post in site.posts %}
<div class="page-grid research-item blog-item">
  <div class="page-label">
    <p class="section-number">
      <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: "%b %-d, %Y" }}</time>
    </p>
  </div>

  <div class="page-content">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>
    <div class="blog-preview">
      {{ post.excerpt | markdownify | strip_html | truncatewords: 32 }}
    </div>
  </div>
</div>
{% endfor %}
