---
permalink: /
title: "ML researcher and engineer"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I train and ship large multimodal models. For about four years at Amazon Visual Search (A9), I led training of the team's CLIP model, which shipped worldwide in multiple Amazon production features, and of a general-purpose embedding model built on a vision-language model.

I'm now pursuing my own idea as a founder: agentic AI for IC physical design. My background is in electrical engineering, and I'm as comfortable in the RTL-to-GDSII flow as in the training stack.

{% comment %}
TODO (optional): one line on what you're looking for, if you want it public.
For example: "I'm open to research scientist and research engineer roles."
{% endcomment %}

Research
======

* **[Multimodal representation learning](/research/multimodal-representation-learning/).** Led training of Amazon Visual Search's internal CLIP model, shipped worldwide in multiple production features, and of a general-purpose embedding model built on a vision-language model.
* **[Training at scale](/research/large-scale-training/).** Worked on an internal distributed training platform on Ray that delivered two generations of VLM-based models.
* **[Agentic AI](/research/agentic-systems/).** Supervised fine-tuning with LoRA for agentic orchestration of visual search, and now verification-first agents for chip design.

{% if site.publications.size > 0 %}My papers are listed on the [Publications](/publications/) page.{% endif %}

Current work
======

As a founder, I'm building agentic AI for IC physical design: placement, routing, timing closure and verification. I'm starting with an AI copilot built on OpenROAD, and the approach is verification first. Deterministic EDA tool outputs act as the oracle for an agent's work.

Background
======

I'm based in San Francisco and work in English and Traditional Chinese.

{% comment %}
TODO: add your degree and school to the line above, for example:
"I studied electrical engineering at [school] ([degree], [year])."
{% endcomment %}

{% if site.author.email %}
Contact
======

Email is the best way to reach me: [{{ site.author.email }}](mailto:{{ site.author.email }}).
{% endif %}
