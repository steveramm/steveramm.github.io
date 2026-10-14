---
title: "Publications"
layout: page
permalink: /publications/
section_number: "03"
---

<input type="text" class="pub-search" id="pubSearch" placeholder="Filter by title, author, or year...">



<div class="page-grid research-item"> <header class="page-label"> <p class="section-number"></p> <h2>Preprints</h2> </header>

{% bibliography --query @unpublished %}
</div> </div>

<h2>Refereed Journal Articles</h2>

{% bibliography --query @article %}

<h2>Refereed Conference Proceedings</h2>

{% bibliography --query @inproceedings %}
</div>
