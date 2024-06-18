---
layout: distill
title: Advancements in Language Models and Generative Adversarial Networks
description: A paper review on WGAN & Gopher
tags: LLM GAN Gopher WGAN
categories: take-aways
giscus_comments: true
date: 2024-05-29 09:00:00-0400
featured: false
related_publications: true

authors:
  - name: Yuetian Chen
    url: "https://stry233.github.io/"
    affiliations:
      name: TruSeLab, Purdue University
      url: https://www.cs.purdue.edu/truselab/
  - name: Yineng Chen
    url: "https://chernyn.github.io/"
    affiliations:
      name: Purdue University
      url: https://www.purdue.edu

bibliography: 2024-05-29-review.bib

toc:
  - name: Introduction 
  - name: Scaling Language Models
    subsections:
      - name: The Gopher Architecture
      - name: Key Insights from Gopher
  - name: Wasserstein GANs
    subsections:  
      - name: Overcoming Challenges in Standard GANs
      - name: The Wasserstein Distance
  - name: Conclusion

---

## Introduction

Recent years have seen tremendous progress in the fields of natural language processing (NLP) and generative modeling. Language models like GPT-3 {% cite brown2020language %} and PaLM {% cite chowdhery2022palm %} have demonstrated remarkable capabilities in understanding and generating human-like text. Meanwhile, generative adversarial networks (GANs) have enabled the creation of strikingly realistic images, videos, and other media. 

In this blog post, we dive into two significant papers that have advanced these domains: {% reference rae2022scaling %} and {% reference arjovsky2017wasserstein %}. We discuss the key ideas, methodologies, and implications of these works.

## Scaling Language Models

Language models form the backbone of modern NLP systems. By learning from vast corpora of text data, these models acquire a broad understanding of language that can be applied to diverse downstream tasks. The Gopher model {% cite rae2022scaling %}, developed by DeepMind, represents an important milestone in the scaling of language models.

### The Gopher Architecture

Gopher is a large-scale transformer-based language model. It follows the decoder-only architecture that has become standard for models like GPT-3. However, the Gopher architecture incorporates a few notable modifications:

1. **RMSNorm instead of LayerNorm**: Gopher uses RMSNorm {% cite zhang2019root %} in place of the more common LayerNorm. RMSNorm is computationally simpler and may promote more stable gradients in deep networks.

2. **Relative Positional Encodings**: Instead of absolute positional encodings, Gopher employs relative encodings. This allows the model to better capture the relative distances between tokens in the input sequence.

### Key Insights from Gopher

The Gopher paper provides several valuable insights into the behavior of large language models:

{% quote rae2022scaling %}
The benefits of scale are most pronounced on tasks like reading comprehension, fact-checking, and toxicity detection. Logical and mathematical reasoning see more modest improvements.
{% endquote %}

This discrepancy may be attributed to the distribution of the training data, underscoring the importance of dataset curation.

Overall, Gopher demonstrates the immense potential of scaling up language models in terms of both parameter count and data size.

## Wasserstein GANs

GANs {% cite goodfellow2014generative %} have emerged as a powerful framework for generative modeling, especially in the image domain. However, training GANs is notoriously challenging, with issues like mode collapse and unstable dynamics plaguing many variants. The Wasserstein GAN (WGAN) {% cite arjovsky2017wasserstein %} introduces a novel approach that mitigates these problems.

### Overcoming Challenges in Standard GANs

In a standard GAN, the generator and discriminator are trained in an adversarial game. The generator tries to produce samples that fool the discriminator, while the discriminator learns to distinguish real from generated data. This setup can lead to several pathologies {% reference arjovsky2017wasserstein %}:

- If the discriminator becomes too strong, it may perfectly reject all generator samples, leading to vanishing gradients and stalled training.
- The generator may collapse onto a narrow distribution, sacrificing diversity in an effort to exploit the discriminator.

WGAN proposes a principled solution to these challenges, rooted in the theory of optimal transport.

### The Wasserstein Distance

The Wasserstein distance, also known as the Earth Mover's distance, is a metric that quantifies the dissimilarity between two probability distributions. In the context of GANs, it measures the distance between the generated distribution $P_g$ and the real data distribution $P_r$. The Wasserstein distance is defined as:

$$
\label{eq:wasserstein}
W(P_r, P_g) = \inf_{\gamma \in \Pi(P_r, P_g)} \mathbb{E}_{(x, y) \sim \gamma}[\|x - y\|]
$$

where $\Pi(P_r, P_g)$ denotes the set of all joint distributions $\gamma(x, y)$ whose marginals are $P_r$ and $P_g$, respectively. In other words, the Wasserstein distance is the minimum cost of transporting mass from $P_r$ to $P_g$, where the cost is given by the expectation of the Euclidean distance between points.

The key advantage of the Wasserstein distance is that it is continuous and differentiable almost everywhere, even when the supports of $P_r$ and $P_g$ do not overlap. This is in contrast to other commonly used metrics like the Jensen-Shannon divergence, which can lead to vanishing gradients in such scenarios {% cite arjovsky2017wasserstein %}.

To make the Wasserstein distance tractable to compute, the Kantorovich-Rubinstein duality {% cite villani2009optimal %} is employed:

$$
\label{eq:kantorovich}
W(P_r, P_g) = \sup_{\|f\|_L \leq 1} \mathbb{E}_{x \sim P_r}[f(x)] - \mathbb{E}_{x \sim P_g}[f(x)]
$$

where the supremum is taken over all 1-Lipschitz functions $f$. In practice, the discriminator in WGAN is trained to approximate the optimal $f$, while the generator is trained to minimize the Wasserstein distance.

The Lipschitz constraint on the discriminator is enforced through gradient penalty {% cite gulrajani2017improved %}:

$$
\label{eq:gradient_penalty}
\mathcal{L}_{\text{GP}} = \lambda \mathbb{E}_{\hat{x} \sim P_{\hat{x}}}[(\|\nabla_{\hat{x}} D(\hat{x})\|_2 - 1)^2]
$$

where $P_{\hat{x}}$ is the distribution of points along straight lines between pairs of points sampled from $P_r$ and $P_g$. This gradient penalty term is added to the discriminator loss to encourage 1-Lipschitzness.

By minimizing the Wasserstein distance through this dual formulation, WGAN achieves more stable training and generates higher quality samples compared to standard GANs. The theoretical grounding in optimal transport theory provides a principled foundation for the WGAN framework.

## Conclusion

The Gopher and WGAN papers exemplify the rapid progress happening in language modeling and generative AI. As we scale up our models and refine our training objectives, we unlock new frontiers in machine intelligence. Gopher points towards a future where language models serve as flexible, general-purpose tools for a wide range of applications. WGAN, meanwhile, brings us closer to generating high-fidelity content with deep neural networks.

Moving forward, it will be exciting to see how these ideas are extended and combined. The union of powerful language models and advanced generative techniques could lead to transformative breakthroughs, reshaping how we interact with AI systems. As always, however, it is crucial that we approach these developments thoughtfully, considering the broader societal implications alongside the technical innovations.

