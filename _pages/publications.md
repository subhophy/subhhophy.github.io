---
layout: page
permalink: /publications/
title: Preprints and publications
description: 
years: [2024]
nav: true
nav_order: 1
published: true
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

{% if entry.doi %}
  <a href="https://doi.org/{{ entry.doi }}" target="_blank">DOI: {{ entry.doi }}</a>
{% endif %}

</div>
