---
title: "Domain adaptation and scene understanding"
excerpt: "Earlier computer vision work: GAN-based image-to-image translation that generates training data for a new domain, such as day to night for vehicle detection, and real-time indoor layout estimation from a single image."
collection: research
order: 4
---

Before working on multimodal models, I worked on computer vision for domains where labelled training data is scarce.

GAN-based data augmentation across domains
======

Detectors trained on one domain, such as daytime driving scenes, often fail on another, such as night. AugGAN is a structure-aware image-to-image translation network that transforms images to the target domain while preserving the objects in them, so the translated images can be used as training data. We applied it to day-to-night style transfer for nighttime vehicle detection.

Indoor scene layout estimation
======

A real-time approach to estimating the layout of an indoor scene from a single image, built on a fully convolutional network with a layout-degeneration augmentation method.

{% include research-publications.html %}
