---
layout: page
title: Benefit Cliffs
description: Help people and policy makers navigate benefit cliffs.
img: assets/img/bfcliffs.png
importance: 1
# category: work
giscus_comments: true
---

This project aims to help people navigate benefit cliffs and supports the development of benefit cliff tools to which I contribute.

"People face a benefits cliff (also known as the “cliff effect”) when they receive public benefits from the government, earn a raise, and then discover that they make too much money to receive the benefits. But they are not making enough money to sustain themselves and their household."  -- [benefitscliff.com](https://www.benefitscliff.com/what-is-a-benefits-cliff)


In other words, people face benefit cliffs when their income grows, but they are worse off since they lose benefits. To quantify a benefit cliff, we would like to define it quantitively.

$$
\text{Benefit Cliff} = \int_{\text{income}} \text{Net Resource w/ cliffs} - \text{Net Resource w/o cliffs}
$$


<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:50%;">
        {% include figure.liquid loading="eager" path="assets/img/bfcliffs.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


To calculate net resources based on different income levels, we use the open-source [repository](https://github.com/Research-Division/policy-rules-database) that contains up-to-date rules and provisions for all major federal and state public assistance programs, taxes, and tax credits in a single easy-to-use database. Detailed calculation of benefits is also provided in the [technical mannual](https://github.com/Research-Division/policy-rules-database/blob/a806195682b7515f01b5739343b91201293dddb4/PRD%20Technical%20Manual.pdf).




To be finished ...