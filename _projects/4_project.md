---
layout: page
title: Fairness-aware IR
description: Exploring Fairness in Wikipedia Article Search 
img: assets/img/Picture1.png
importance: 1
# category: work
giscus_comments: true
---


{::nomarkdown}
{% assign jupyter_path = "assets/jupyter/Portfolio1.ipynb" | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/blog.ipynb %}{% endcapture %}
{% if notebook_exists == "true" %}
{% jupyter_notebook jupyter_path %}
{% else %}

<p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}