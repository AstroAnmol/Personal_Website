---
layout: page
permalink: /publications/
title: publications
description: publications by categories in reversed chronological order.
years: [2023]
conferenceyears: [2024,2023,2022,2021,2020,2019]
nav: true
---
<!-- _pages/publications.md -->
<div class="publications">

<h3> journal articles </h3>
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @article[year={{y}}]* %}
{% endfor %}

<h3> conference proceedings </h3>
{%- for yr in page.conferenceyears %}
  <h2 class="year">{{yr}}</h2>
  {% bibliography -f papers -q @inproceedings[year={{yr}}]* %}
{% endfor %}

</div>
