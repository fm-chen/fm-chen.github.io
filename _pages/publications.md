---
layout: page
permalink: /readings/
title: readings
description: Relative readings
# years: [1967, 1956, 1950, 1935, 1905]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->

<div class="publications">

  <h3>Most Relevant</h3>
  {% bibliography -f papers -q @*[cat=relative] %}

  <h3>Others Relative</h3>
  {% bibliography -f papers -q @*[cat=others] %}

  <h3>Interesting Publications in Fair Ranking</h3>
  {% bibliography -f papers -q @*[cat=interest] %}

</div>


