---
layout: page
title: Blog
permalink: /blog/
section_number: "06"
---

<div class="page-layout blog-page">

<header class="page-header page-grid"> <div class="page-label"> <span class="meta">06</span> <h1>Blog</h1> </div> <div class="page-content page-intro"> <p>Notes, news and updates from the lab.</p> </div> </header>

<div class="blog-list"> {% for post in site.posts %} <article class="blog-item page-grid"> <div class="blog-date page-label"> <time class="meta" datetime="{{ post.date | datetoxmlschema }}"> {{ post.date | date: "%b %-d, %Y" }} </time> </div> <div class="blog-title page-content"> <h2><a href="{{ post.url | relativeurl }}">{{ post.title | escape }}</a></h2> {% if post.excerpt %} <div class="blog-excerpt"> {{ post.excerpt | markdownify | striphtml | truncate: 220 }} </div> {% endif %} </div> </article> {% else %} <p>No blog posts yet.</p> {% endfor %} </div>
