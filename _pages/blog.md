---
title: "Blog"
layout: page
permalink: /blog/
section_number: "06"
---

{% for post in site.posts %}
<div class="page-grid research-item blog-item">
  <div class="page-label">
    <p class="section-number">{{ post.date | date: "%b %-d, %Y" }}</p>
  </div>
  <div class="page-content">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>
    <p class="blog-preview">{{ post.excerpt | strip_html | truncatewords: 32 }}</p>
  </div>
</div>
{% else %}
<p>No blog posts found.</p>
{% endfor %}
