---
layout: page
title: Benefit Cliffs
description: Data analysis for benefit cliffs.
img: assets/img/bfcliffs.jpg
importance: 1
category: work
giscus_comments: true
---

This project aims to help people navigate benefit cliffs and supports the development of benefit cliff tools to which I contribute.

"People face a benefits cliff (also known as the “cliff effect”) when they receive public benefits from the government, earn a raise, and then discover that they make too much money to receive the benefits. But they are not making enough money to sustain themselves and their household."  -- [benefitscliff.com](https://www.benefitscliff.com/what-is-a-benefits-cliff)


In other words, people face benefit cliffs when their income grows, but they are worse off since they lose benefits. To quantify a benefit cliff, we would like to define it quantitively.

$$
\text{Benefit Cliff} = \int_{\text{income}} \text{Net Resource w/ cliffs} - \text{Net Resource w/o cliffs}
$$


<div class="row justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bfcliffs.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


To calculate net resources based on different income levels, we use the open-source [repository](https://github.com/Research-Division/policy-rules-database) that contains up-to-date rules and provisions for all major federal and state public assistance programs, taxes, and tax credits in a single easy-to-use database.










You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
