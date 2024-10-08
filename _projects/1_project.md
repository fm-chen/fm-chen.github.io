---
layout: page
title: CoachGPT
description: A GenAI powered academic writing assistant ChatBot.
img: assets/img/chatbot.png
importance: 1
# category: fun
giscus_comments: true
---

This is a project that I am currently participating in and collaborating with the people from the School of Education at the University of Delaware. We want to develop an AI-based chatbot called "CoachGPT" to assist academic writing in English and help students complete their assignments step by step. The high-level goal of this project is to (1) make writing/learning fun and effective, (2) support self-regulative learning for everyone, everywhere, regardless of what resources they have, and (3) check the impact of the projects on users to understand the project, limitations, and areas of improvements.

We leverage the software development lifecycle (SDLC) methodology to guide our system development. We first spend time on planning to gather user requirements, allocate resources, set up budgets, schedule meetings, estimate implementation timelines, and clarify deliverables at later stages. 

<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:50%;">
        {% include figure.liquid loading="eager" path="assets/img/coachgpt_structure.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   CoachGPT's System Implementation Structure.
</div>

Chatbot core is powered by [ChatGPT](https://openai.com/) implemented by [LangChain](https://python.langchain.com/v0.1/docs/use_cases/chatbots/). Full implementation code and development documents are currently in private, but you can check out our:

**Live [Demo](https://infochain.ece.udel.edu/coachgpt/)** and **User Video Tutorial**.

    ---
    user: test@gmail.com 
    password: password
    ---


<div class="row d-flex justify-content-center">
    <div class="col-sm-auto mt-3 mt-md-0" style="width:50%;">
        {% include video.liquid path="https://www.youtube.com/embed/cIZnCm1awMc" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Example code from [LangServe](https://python.langchain.com/docs/langserve/) to build a similar chatbot app:

```html
#!/usr/bin/env python
from fastapi import FastAPI
from langchain.prompts import ChatPromptTemplate
from langchain.chat_models import ChatAnthropic, ChatOpenAI
from langserve import add_routes

app = FastAPI(
    title="LangChain Server",
    version="1.0",
    description="A simple api server using Langchain's Runnable interfaces",
)

add_routes(
    app,
    ChatOpenAI(model="gpt-3.5-turbo-0125"),
    path="/openai",
)

add_routes(
    app,
    ChatAnthropic(model="claude-3-haiku-20240307"),
    path="/anthropic",
)

model = ChatAnthropic(model="claude-3-haiku-20240307")
prompt = ChatPromptTemplate.from_template("tell me a joke about {topic}")
add_routes(
    app,
    prompt | model,
    path="/joke",
)

if __name__ == "__main__":
    import uvicorn

    uvicorn.run(app, host="localhost", port=8000)
```


