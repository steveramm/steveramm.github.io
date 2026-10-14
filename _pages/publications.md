---
title: "Publications"
layout: page
permalink: /publications/
section_number: "03"
---


<div class="page-layout publications-page">

<header class="page-grid page-header"> <div class="page-label"> <p class="section-number">03</p> <h1>Publications</h1> </div>

<div class="page-content page-intro"> <p> Selected publications and preprints. </p> </div> </header>

<div class="publications-search"> <input type="text" class="pub-search" id="pubSearch" placeholder="Filter by title, author, or year..." aria-label="Filter publications"

</div>

<section class="page-grid research-item publication-section"> <header class="page-label"> <h2>Preprints</h2> </header>

<div class="page-content publication-list"> {% bibliography --query @unpublished %} </div> </section>

<section class="page-grid research-item publication-section"> <header class="page-label"> <h2>Published articles</h2> </header>

<div class="page-content publication-list"> {% bibliography --query @article %} </div> </section>

</div>
