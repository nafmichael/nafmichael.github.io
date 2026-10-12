---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

{% comment %}
TODO: this page is built only from facts that were already known, so it has no
dates, job title or education yet. Add them below. To offer a PDF as well, save
it as files/resume.pdf and the download link appears on its own.
{% endcomment %}

{% assign resume = site.static_files | where: "path", "/files/resume.pdf" | first %}
{% if resume %}
[Download this CV as a PDF]({{ base_path }}/files/resume.pdf)
{% endif %}

Experience
======
* **Founder**, pursuing my own idea
  * Agentic AI for IC physical design: placement, routing, timing closure and verification
  * Building an AI copilot for physical design on OpenROAD
  * Verification first: deterministic EDA tool outputs act as the oracle for an agent's work

* **Amazon Visual Search (A9)**, about four years
  * Led training of the team's internal CLIP model, which shipped worldwide in multiple Amazon production features
  * Led training of a general-purpose embedding model built on a vision-language model
  * Supervised fine-tuning with LoRA for agentic orchestration of visual search
  * Worked on an internal distributed training platform built on Ray, which delivered two generations of VLM-based models

{% comment %}
TODO: fill in and move out of this comment block.

Education
======
* [Degree] in Electrical Engineering, [School], [Year]
{% endcomment %}

Skills
======
* **Multimodal representation learning:** contrastive image-text models at CLIP scale, VLM-based embedding models, multimodal retrieval
* **Training at scale:** distributed training on Ray, supervised fine-tuning with LoRA
* **Agentic systems:** agentic orchestration, agent verification against deterministic tool outputs
* **IC physical design:** RTL-to-GDSII, floorplanning, timing closure, EDA tooling, OpenROAD

Languages
======
* English
* Traditional Chinese

{% if site.publications.size > 0 %}
Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
{% endif %}

{% if site.talks.size > 0 %}
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
{% endif %}
