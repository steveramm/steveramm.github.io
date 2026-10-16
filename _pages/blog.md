---
layout: page
title: Blog
permalink: /blog/
section_number: "06"
---

<div class="page-grid research-intro"> <div class="page-label"></div>

<div class="page-content"> <p class="research-lead">News, views and updates from the lab.</p> </div> </div>

<div class="page-grid research-item"> <header class="page-label"> <p class="section-number">01.01</p> <h2>Climate change and fertility</h2> </header>

<div class="blog-list"> {% for post in site.posts %} <article class="blog-item page-grid"> <div class="blog-date page-label"> <time class="meta" datetime="{{ post.date | datetoxmlschema }}"> {{ post.date | date: "%b %-d, %Y" }} </time> </div> <div class="blog-title page-content"> <h2><a href="{{ post.url | relativeurl }}">{{ post.title | escape }}</a></h2> {% if post.excerpt %} <div class="blog-excerpt"> {{ post.excerpt | markdownify | striphtml | truncate: 220 }} </div> {% endif %} </div> </article> {% else %} <p>No blog posts yet.</p> {% endfor %} </div>
