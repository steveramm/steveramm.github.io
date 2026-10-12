---
title: "Team"
layout: page
permalink: /team/
---

{% comment %} PI {% endcomment %} <div class="team-page-grid">

<div class="team-member"> <div class="team-member-copy"> <h2>{{ site.name }}</h2> <p class="team-member-role">{{ site.title }}, {{ site.institution }}</p>

<div class="team-links"> {% if site.email %} <a href="mailto:{{ site.email }}" class="icon-link" title="Email" aria-label="Email">{% include icon.html name="envelope" %}</a> {% endif %} {% if site.links.googlescholar and site.links.googlescholar != "" %} <a href="{{ site.links.googlescholar }}" class="icon-link" title="Google Scholar" aria-label="Google Scholar">{% include icon.html name="google-scholar" %}</a> {% endif %} {% if site.links.cv and site.links.cv != "" %} <a href="{{ site.links.cv | prepend: '/' | relativeurl }}" class="icon-link" title="CV" aria-label="CV">{% include icon.html name="cv" %}</a> {% endif %} </div>

{% if site.data.pi[0].education %} <ul> {% for education in site.data.pi[0].education %} <li>{{ education | replace: "-", "–" }}</li> {% endfor %} </ul> {% endif %} </div>

<img src="{{ site.photo | prepend: '/images/' | relative_url }}" class="team-member-photo" alt="{{ site.name }}" width="240" loading="lazy"> </div>

{% comment %} Add individual profiles and group photos here, in the desired order. {% endcomment %}

{% for item in site.data.team_page %} {% if item.type == "member" %} <div class="team-member"> <div class="team-member-copy"> <h2>{{ item.name }}</h2> <p class="team-member-role">{{ item.info }}</p>

<div class="team-links"> {% if item.email %} <a href="mailto:{{ item.email }}" class="icon-link" title="Email" aria-label="Email">{% include icon.html name="envelope" %}</a> {% endif %} {% if item.website %} <a href="{{ item.website }}" class="icon-link" title="Website" aria-label="Website">{% include icon.html name="house" %}</a> {% endif %} {% if item.scholar %} <a href="{{ item.scholar }}" class="icon-link" title="Google Scholar" aria-label="Google Scholar">{% include icon.html name="google-scholar" %}</a> {% endif %} {% if item.github %} <a href="{{ item.github }}" class="icon-link" title="GitHub" aria-label="GitHub">{% include icon.html name="github" %}</a> {% endif %} </div>

{% if item.description %} <div>{{ item.description | markdownify }}</div> {% endif %} </div>

<img src="{{ item.photo | prepend: '/images/' | relative_url }}" class="team-member-photo" alt="{{ item.name }}" loading="lazy"> </div>

{% elsif item.type == "groupphoto" %} <figure class="team-group-photo"> <img src="{{ item.photo | prepend: '/images/' | relativeurl }}" alt="{{ item.alt | default: item.caption }}" loading="lazy"> <figcaption>{{ item.caption }}</figcaption> </figure> {% endif %} {% endfor %}

</div>

{% if site.data.alumni.size > 0 %} <section class="team-alumni"> <h2>Alumni</h2> <ul> {% for member in site.data.alumni %} <li> <strong>{{ member.name }}</strong> {% if member.duration %} — {{ member.duration }}{% endif %} {% if member.info %} — {{ member.info }}{% endif %} </li> {% endfor %} </ul> </section> {% endif %}

<section class="team-administration"> <h2>Administrative support</h2> <p><a href="mailto:exampleemail@gmail.com">Example staff</a> provides administrative support for our group and others.</p> </section>
