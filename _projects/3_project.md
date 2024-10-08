---
layout: page
title: Benefit Cliffs
description: Help people and policy makers navigate benefit cliffs.
img: assets/img/bfcliffs.png
importance: 1
# category: work
giscus_comments: true
---

## Introduction

This project aims to help people navigate benefit cliffs and supports the development of benefit cliff tools to which I contribute.

"People face a benefits cliff (also known as the “cliff effect”) when they receive public benefits from the government, earn a raise, and then discover that they make too much money to receive the benefits. But they are not making enough money to sustain themselves and their household."  -- [benefitscliff.com](https://www.benefitscliff.com/what-is-a-benefits-cliff)


In other words, people face benefit cliffs when their income grows, but they are worse off since they lose benefits. To quantify a benefit cliff, we would like to define it quantitively.

$$
\text{Benefit Cliff} = \int_{\text{income}} \text{Net Resource w/ cliffs} - \text{Net Resource w/o cliffs}
$$

where $$\text{Net Resource} = \text{Income} + \text{Benefits} - \text{Expenses}$$.

<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:50%;">
        {% include figure.liquid loading="eager" path="assets/img/bfcliffs.png" title="bf_def" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


It is a complex process to calculate net resources based on different income levels and family profiles since different states/locations might have different policies or eligibility rules. Therefore, we use the open-source [repository](https://github.com/Research-Division/policy-rules-database) that contains up-to-date rules and provisions for all major federal and state public assistance programs, taxes, and tax credits in a single easy-to-use database. Detailed calculation of benefits is also provided in the [technical mannual](https://github.com/Research-Division/policy-rules-database/blob/a806195682b7515f01b5739343b91201293dddb4/PRD%20Technical%20Manual.pdf).

## Factors that Impact Benefit Cliffs
As said, there are multiple factors that impact how benefit cliffs happen, such as location and family profile.
<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:80%;">
        {% include figure.liquid loading="eager" path="assets/img/bf_places.png" title="bf_example1" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   Benefit Cliffs by Family Size in Kent County, Delaware.
</div>
<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:80%;">
        {% include figure.liquid loading="eager" path="assets/img/bf_age.png" title="bf_example2" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   Benefit Cliffs by Age in Kent County, Delaware.
</div>
<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:80%;">
        {% include figure.liquid loading="eager" path="assets/img/bf_married.png" title="bf_example3" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Benefit Cliffs by Marital status in Kent County, Delaware.
</div>

## How Many People are Potentially Impacted by Benefit Cliffs?
Knowing the effect of benefit cliffs, it is important to learn how impactful benefit cliffs are. That is, how many people could potentially face benefit cliffs. To answer this question, we have to estimate the population based on family profiles. We adopt the [American Community Survey 5-Year Data (ACS5)](https://www.census.gov/data/developers/data-sets/acs-5year.html) to estimate population. 

<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:70%;">
        {% include figure.liquid loading="eager" path="assets/img/impactedpop_julia.png" title="impacted_pop" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Benefit Cliffs and Population by Income (Kent County, Delaware).
</div>

You can also make [Tableau](https://www.tableau.com/) Dashboards with these population and geospatial data like [this](https://public.tableau.com/shared/MCCH6PXBF?:display_count=n&:origin=viz_share_link) I made eariler for another project.

## Benefit Cliffs Viz Tool [^1]
To help people and policy makers better understand benefit cliffs and navigate through benefit cliffs, I built the following Viz, which is hosted on [Hugging Face Spaces](https://huggingface.co/spaces) and powered by [Gradio](https://www.gradio.app/). 

<iframe
	src="https://fm-chen-bc-viz.hf.space"
	frameborder="0"
	width="110%"
	height="800"
    style="margin-left: -5%;"
></iframe>

[^1]: **\*Disclaimer**: This is not the official tool we build at work, which is currently in private.