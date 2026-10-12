---
title: "Team"
layout: page
permalink: /team/
---

<div class="page-layout">

<!-- Page introduction --> <div class="page-grid page-header"> <header class="page-label"> <h1>Team</h1> </header>

<div class="page-content page-intro"> <p>Our research group investigates the evolutionary ecology of reproduction, adaptation, and mating systems.</p> </div> </div>

<!-- Team members and group photographs --> <div class="team-page-grid">

{% comment %} Principal investigator {% endcomment %} <article class="page-grid team-member">

<div class="team-member-photo-wrap"> {% if site.photo %} <img src="{{ site.photo | prepend: '/images/' | relative_url }}" class="team-member-photo" alt="Portrait of {{ site.name }}" loading="lazy" > {% endif %} </div>

<div class="team-member-copy"> <h2>{{ site.name }}</h2>

<p class="team-member-role"> {{ site.title }}{% if site.institution %}, {{ site.institution }}{% endif %} </p>

<div class="team-links"> {% if site.email %} <a href="mailto:{{ site.email }}">Email</a> {% endif %}

{% if site.links.googlescholar and site.links.googlescholar != "" %} <a href="{{ site.links.googlescholar }}">Google Scholar</a> {% endif %}

{% if site.links.cv and site.links.cv != "" %} <a href="{{ site.links.cv | prepend: '/' | relative_url }}">CV</a> {% endif %} </div>

{% if site.data.pi[0].education %} <ul class="team-education"> {% for education in site.data.pi[0].education %} <li>{{ education | replace: "-", "–" }}</li> {% endfor %} </ul> {% endif %} </div>

</article>

{% comment %} Current students and postdocs {% endcomment %} {% for member in site.data.team_members %}

<article class="page-grid team-member">

<div class="team-member-photo-wrap"> {% if member.photo %} <img src="{{ member.photo | prepend: '/images/' | relative_url }}" class="team-member-photo" alt="Portrait of {{ member.name }}" loading="lazy" > {% endif %} </div>

<div class="team-member-copy"> <h2>{{ member.name }}</h2>

{% if member.info %} <p class="team-member-role">{{ member.info }}</p> {% endif %}

<div class="team-links"> {% if member.email %} <a href="mailto:{{ member.email }}">Email</a> {% endif %}

{% if member.website %} <a href="{{ member.website }}">Website</a> {% endif %}

{% if member.scholar %} <a href="{{ member.scholar }}">Google Scholar</a> {% endif %}

{% if member.github %} <a href="{{ member.github }}">GitHub</a> {% endif %} </div>

{% if member.description %} <div class="team-member-description"> {{ member.description | markdownify }} </div> {% endif %} </div>

</article>

{% endfor %}

{% comment %} Group photographs can be placed anywhere in this grid, between profiles or after all team members. {% endcomment %}

<figure class="team-group-photo"> <img src="{{ '/images/team/teamgroup.jpg' | relativeurl }}" alt="Members of the research group" loading="lazy" > <figcaption> The research group at [event or location]. </figcaption> </figure>

</div>

<!-- Alumni --> {% if site.data.alumni.size > 0 %} <section class="page-section team-alumni"> <div class="page-grid">

<header class="page-label"> <h2>Alumni</h2> </header>

<div class="page-content"> <ul> {% for member in site.data.alumni %} <li> <strong>{{ member.name }}</strong> {% if member.duration %} — {{ member.duration }}{% endif %} {% if member.info %} — {{ member.info }}{% endif %} </li> {% endfor %} </ul> </div>

</div> </section> {% endif %}

<!-- Administrative support --> <section class="page-section team-administration"> <div class="page-grid">

<header class="page-label"> <h2>Administrative support</h2> </header>

<div class="page-content"> <p> <a href="mailto:exampleemail@gmail.com">Example staff</a> provides administrative support for our group and others. </p> </div>

</div> </section>

</div>
