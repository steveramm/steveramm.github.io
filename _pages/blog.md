---
layout: page
title: Blog
permalink: /blog/
section_number: "06"
---

<div class="page-grid research-intro"> <div class="page-label"></div> <div class="page-content"> <p class="research-lead">Notes, news and updates from the lab.</p> </div> </div>

{% for post in site.posts %}
<div class="page-grid research-item blog-item">
<div class="page-label">
<p class="section-number"><time datetime="{{ post.date | datetoxmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time></p>
</div>
<div class="page-content">
<h2><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>
<div class="blog-preview">
<p>{{ post.excerpt | strip_html | truncatewords: 35 }}</p>
</div>
</div>
</div>
{% endfor %}
