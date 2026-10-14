---
title: "Publications"
layout: page
permalink: /publications/
section_number: "03"
---

<input type="text" class="pub-search" id="pubSearch" placeholder="Filter by title, author, or year...">

<div id="pubList">

<section class="page-grid research-item"> <header class="page-label"> <h2>Preprints</h2> </header> <div class="page-content"> {% bibliography --query @unpublished %} </div> </section>

<section class="page-grid research-item"> <header class="page-label"> <h2>Refereed Journal Articles</h2> </header> <div class="page-content"> {% bibliography --query @article %} </div> </section>

<section class="page-grid research-item"> <header class="page-label"> <h2>Refereed Conference Proceedings</h2> </header> <div class="page-content"> {% bibliography --query @inproceedings %} </div> </section>

</div>
