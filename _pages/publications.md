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

  <h3>Most Relative</h3>
  {% bibliography -f papers -q @*[cat=relative] %}

  <h3>Others</h3>
  {% bibliography -f papers -q @*[cat=others] %}


</div>


