---
title: "Multimodal representation learning"
excerpt: "Embedding models that put images and text in one space, from a CLIP model shipped worldwide in Amazon production features to a general-purpose embedding model built on a vision-language model."
collection: research
order: 1
redirect_from:
  - /portfolio/clip-visual-search/
  - /portfolio/vlm-embedding-model/
---

I work on models that map images and text into a shared embedding space, so that one can be used to search for the other. At Amazon Visual Search (A9) I led training of two generations of these models.

CLIP model for visual search
======

I led training of the team's internal CLIP model: contrastive image-text representation learning at CLIP scale, used for multimodal retrieval.

* **Role:** led model training
* **Team:** Amazon Visual Search (A9)
* **Status:** shipped worldwide, in multiple Amazon production features

{% comment %}
TODO: make this section worth reading. Things a hiring team looks for, as far
as you can share them publicly:
- when this was, and how long it took
- the problem: what the model replaced or made possible
- your own decisions: data, objective, architecture, training recipe, evaluation
- scale and results: any number you are allowed to state
- links: a paper, a blog post, a public feature that uses it
{% endcomment %}

General-purpose VLM embedding model
======

I led training of a general-purpose embedding model built on a vision-language model.

* **Role:** led model training
* **Team:** Amazon Visual Search (A9)
* **Status:** rolling out to production

{% comment %}
TODO: check the status line is still current, then add what you can share:
- when this was
- why a VLM-based embedding model, and what it does that the CLIP model did not
- your own decisions: backbone, training objective, data, evaluation
- scale and results: any number you are allowed to state
{% endcomment %}

{% include research-publications.html %}
