---
layout: page
title: Interpretable ML with RAG
description: A RAG powered ChatBot for better ML interpretablility via Q&A. 
img: assets/img/Figure_3_RAG_workflow.png
importance: 2
category: fun
giscus_comments: true
---

**TL;DR**: *[Live Demo](https://515ed13cc82234667a.gradio.live)*

### Background
OpenAI o1 ranks in the **89th** percentile on competitive programming questions (Codeforces), places among the top 500 students in the US in a qualifier for the USA Math Olympiad (AIME), and exceeds human **PhD-level** accuracy on a benchmark of physics, biology, and chemistry problems (GPQA). 

<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:80%;">
        {% include figure.liquid loading="eager" path="assets/img/gpt_performance.png" title="gpt-perform" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   Recent development of LLMs (GPT-o1) shows a promising capability of reasoning.
</div>

Unlike the previous LLMs which suffer from mathematical reasoning, this significant advancement inspired use to re-think the application of LLMs on machine learning interpretability, especially with the emergence of **retrieval augmented generation (RAG)** that addresses the issue of hallucination.


### The RAG Workflow
As the name suggested, a RAG process contains three major steps, *retrieval*, *augmentation*, and *generation*. RAG uses two components to achieve these steps, *retriever* and *generator*. Retriever retrieves relevant information from knowledge bases and feed to generator. Generator then uses the information as context for a better generation.
<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:100%;">
        {% include figure.liquid loading="eager" path="assets/img/Figure_3_RAG_workflow.png" title="rag-workflow" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   The typical RAG workflow.
</div>

### Preliminary Implementation
To build a RAG system, we need to build its retriever and generator. There are AI frameworks, like [LlamaIndex](https://www.llamaindex.ai/) that can help us build RAG piplines but we still need to choose our storage (Vector DB). This work builds the RAG-powered LLM application with [Milvus](https://milvus.io/) and [LlamaIndex](https://www.llamaindex.ai/).
<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:80%;">
        {% include figure.liquid loading="eager" path="assets/img/rag_implement.png" title="rag-implement" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

We use [Ollama](https://ollama.com/) to run open-sourced LLMs locally. Use LlamaIndex to process pdfs, handle chunking/chunking overlap, index documents into our Milvus Vector DB, and finally set query engine (retriever).


### \*Monitoring, Fine-tuning and Improvement (under construction)
These sections involve monitoring/improving the performance of RAG. Different retrieval methods including hybrid search, retrieval evaluation metrics, and LLMs will be tested. Useful tools: [ragas](https://docs.ragas.io/en/stable/)

### [Live Demo](https://515ed13cc82234667a.gradio.live)

Knowledge base in demo: [pdf](/assets/pdf/lime_paper.pdf)
<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:100%;">
        {% include figure.liquid loading="eager" path="assets/img/rag_demo.png" title="rag-demo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Reference
[Building RAG with Milvus Lite, Llama3, and LlamaIndex](https://zilliz.com/learn/build-rag-with-milvus-lite-llama3-and-llamaindex)


