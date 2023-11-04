---
title: "Visual Instruction Tuning." 
summary: "A summary of the same paper published in `37th Conference on Neural Information Processing Systems(NeurIPS'23)`."
date: 2023-10-01
math: true
featured: false
authors: 
 - admin
tags: 
 - large language models
 - multimodal learning
 - instruction tuning
 - LLaVA
 - vision encoder
 - language understanding

categories: 
 - Paper Reviews 
---

## Problem Statement:
The paper addresses the limitations of existing vision-language pretraining models by highlighting the need for aligning events and their associated arguments in images. The goal is to enable vision-language models to understand the semantics of images and the roles of objects within those images.

## Event Graph Alignment Loss:
The paper introduces an innovative evaluation metric, the "Event Graph Alignment Loss," to assess the alignment between vision and language in complex event-rich datasets.

## Pretraining with Large Event-Rich Datasets:
To enhance model understanding, the paper employs a large event-rich dataset for pretraining, offering more challenging benchmarks for image retrieval. This approach aims to promote a deeper comprehension of detailed, lengthy event descriptions.

## Zero-Shot Clip Event Model:
The paper utilizes the "ZeroShot Clip Event" model, achieving a 5% improvement in event extraction F-score compared to standard Multimedia Event Extraction methods.

## Detailed Approach:
The paper outlines its approach in detail, emphasizing the utilization of text information extraction techniques to extract event structures from images. Object detection is performed using R-CNN, and primary event detection focuses on identifying the key event, especially when multiple events are present.

## Experiments and Data:
The experiments involve a dataset of 100,000 images from news websites. The ViT-B/32 architecture initializes the model parameters, and the MME^2 framework is employed. Captions provide distant supervision to interpret images, and negative event descriptions are generated using prompt functions for contrasting. Event graph alignment is achieved through optimal transport methods.

## Incorporating Event Structure in Pretraining:
The paper emphasizes the incorporation of event-structured knowledge into vision-language pretraining, demonstrating a focus on zero-shot learning.

## Conclusion and Future Directions:
The paper underscores the significance of aligning events and their arguments in vision-language models. Future research may explore how this approach can be further enhanced and extended to other challenging vision-language tasks.

## References
- [Visual Instruction Tuning](https://doi.org/10.48550/arXiv.2304.08485)