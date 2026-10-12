---
header:
  teaser: research/agentic-systems.svg
title: "Agentic AI"
excerpt: "Agents that do real work and whose work can be checked: fine-tuning for agentic orchestration of visual search, and verification-first agents for IC physical design, the idea I'm now pursuing as a founder."
collection: research
order: 3
redirect_from:
  - /portfolio/agentic-visual-search/
---

I'm interested in agents whose work can be checked. I first worked on agents at Amazon Visual Search, and now build them for chip design, pursuing my own idea as a founder.

Agentic orchestration of visual search
======

At Amazon Visual Search (A9), I did supervised fine-tuning with LoRA for agentic orchestration of visual search.

* **Role:** model fine-tuning
* **Team:** Amazon Visual Search (A9)

{% comment %}
TODO: add what you can share:
- when this was, and whether it shipped (then add a Status line like the other sections)
- what the agent orchestrates, and which model you fine-tuned
- how you built the training data and how you evaluated the result
{% endcomment %}

Agentic AI for IC physical design
======

As a founder, I'm building agentic AI for IC physical design, the backend flow that takes a chip from a netlist to a manufacturable layout: placement, routing, timing closure and verification. I'm starting with an AI copilot built on [OpenROAD](https://github.com/The-OpenROAD-Project/OpenROAD), the open-source RTL-to-GDSII flow.

The approach is verification first. Before an agent is trusted to generate, deterministic EDA tool outputs act as the oracle for its work: the agent proposes a change, OpenROAD runs it, and the tool's output decides whether it passed.

* **Role:** founder
* **Built on:** OpenROAD

{% include research-publications.html %}
