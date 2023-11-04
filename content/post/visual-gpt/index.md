---
title: "VisualGPT: Data-efficient Adaptation of Pretrained Language Models for Image Captioning." 
summary: "A summary of the same paper published in `2022 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)`."
date: 2023-09-01
math: true
featured: false
authors: 
 - admin
tags: 
 - VisualGPT
 - large language models
 - vision encoding
 - image captioning
 - language models
 - data efficiency

categories: 
 - Paper Reviews 
---
## Introduction

**What is the main research question or hypothesis and why it is important ?**

- How can we efficiently adapt a large pre-trained language model to new domains of image captioning with small quantities of multimodal data?
- It tackles the challenge of limited annotated data availability in real-world applications of machine learning, specifically in the context of generating accurate and contextually relevant captions for images.

## Literature Review

**Which previous studies and what gaps are highlighted ?**

- Focused on filling templates with extracted objects, attributes, and relationships - not NLP.
- Feng et al. propose unsupervised captioning without using paired
image-caption supervision

## Methodology

**How was the study designed, and why was this design chosen?**

- Designed to adapt a pretrained language model (PLM), specifically GPT-2, for the task of image captioning.
- Design aimed to exploit this existing knowledge to generate coherent and contextually relevant captions without having to train a model from scratch.
- Encoder-decoder attention, which allows the integration of visual information from the image encoder with the linguistic knowledge of the PLM.
- **Self-Resurrecting Activation Unit (SRAU)**: SRAUs were introduced to control the balance between visual information and linguistic knowledge during caption generation. This design choice was made to ensure that the model refers to the visual input when necessary while primarily relying on its linguistic knowledge.
- Designed to harness the power of PLMs for image captioning while carefully balancing visual and linguistic information, using innovative mechanisms like SRAUs and meshed connections, and optimizing for human-like caption quality through reinforcement learning.

## Experiments and Results

**What were the main findings of the study and what were the limitations ?**

- The paper evaluates the model on three datasets:  **MS COCO, Conceptual Captions, IU X-ray**
- The performance is measured using metrics like BLEU, METEOR, ROUGE, and CIDEr.
- The paper compares the model with several state-of-the-art transformer-based models:
- **Plain Transformer**: A basic transformer model.
- **AoA Transformer**: Integrates an attention-on-attention module.
- **M2 Transformer**: Introduces a meshed connection between encoder and decoder.
- **X-Transformer**: Uses bilinear pooling for visual information.
- **OSCAR**: Finetunes BERT initialization on image-language datasets.
- The paper also creates variants of these models using GPT as the decoder for a fair comparison. For the VisualGPT model, a hyperparameter τ is set to 0.2, which helps control sparsity. All models are trained in a reinforcement learning setting, and the hyperparameters are tuned on the validation set of MS COCO.
- VisualGPT outperforms all baselines in various training data scenarios:
- On MS COCO, it outperforms the best baseline by 4.1 CIDEr (0.1% data), 6.4 CIDEr (0.5% data), and 2.5 CIDEr (1% data).
- On Conceptual Captions, it surpasses the best baseline by 4.2 CIDEr (0.1% data), 3.5 CIDEr (0.5% data), and 0.3 CIDEr (1% data).
- **Comparison with BERT-based model**: VisualGPT is compared with OSCAR, a BERT-based model, and shows better performance on both datasets. This validates the choice of using GPT as a decoder, given its autoregressive nature aligning more closely with image captioning objectives.

## Conclusion

**How do the findings address the initial research question or hypothesis and are there recommendations for future research?**

- VisualGPT can effectively generate image captions with limited training data, making it ideal for low-resource languages and specialized fields
- Explore different pre-training methods for performance improvement.

## References
- [VisualGPT: Data-efficient Adaptation of Pretrained Language Models for Image Captioning.](https://doi.org/10.48550/arXiv.2102.10407)