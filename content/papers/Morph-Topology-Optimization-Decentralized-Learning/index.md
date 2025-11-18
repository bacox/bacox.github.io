---
title: "Dynamic Topology Optimization for Non-IID Data in Decentralized Learning" 
date: 2025-11-06
url: /paper/Topology-Optimization-Decentralized-Learning
aliases: 
    - /old_url.html
tags: ["Decentralized Learning", "Heterogeneous Data Distribution", "Communication Graph"]
author: ["Bart Cox", "Antreas Ioannou", "<a target=\"_blank\" rel=\"noopener noreferrer\" href=\"https://sites.google.com/view/jdecouchant/accueil\">Jérémie Decouchant</a>"]
description: "Morph is a topology optimization method for decentralized learning that adapts peer selection to handle non-IID data, improving accuracy, stability, and convergence." 
summary: "Morph is a decentralized learning topology optimizer that adapts peer selection based on model dissimilarity to overcome non-IID data and static communication limits. By reshaping the graph through gossip-based discovery, it boosts robustness and performance. Experiments on CIFAR-10 and FEMNIST show Morph outperforming static and epidemic baselines, achieving higher accuracy, faster convergence, and more stable learning with fewer communication rounds."
draft: false
cover:
    image: "morph.png"
    alt: "Topology Update"
    relative: true
editPost:
    URL: "https://doi.org/paper_doi"
    Text: "IEEE Big Data"
buttons:
    code: https://github.com/bacox/Morph
---

---

##### Links:

<!-- - [Publication](paper.pdf)
- [Paper](appendix.pdf) -->
- [Code](https://github.com/bacox/morph)

---

##### Abstract:

Decentralized learning (DL) enables a set of nodes to train a model collaboratively without central coordination, offering benefits for privacy and scalability. However, DL struggles to train a high accuracy model when the data distribution is non-independent and identically distributed (non-IID) and when the communication topology is static. To address these issues, we propose Morph, a topology optimization algorithm for DL. In Morph, nodes adaptively choose peers for model exchange based on maximum model dissimilarity. Morph maintains a fixed in-degree while dynamically reshaping the communication graph through gossip-based peer discovery and diversity-driven neighbor selection, thereby improving robustness to data heterogeneity. Experiments on CIFAR-10 and FEMNIST with up to 100 nodes show that Morph consistently outperforms static and epidemic baselines, while closely tracking the fully connected upper bound. On CIFAR-10, Morph achieves a relative improvement of 1.12× in test accuracy compared to the state-of-the-art baselines. On FEMNIST, Morph achieves an accuracy that is 1.08× higher than Epidemic Learning. Similar trends hold for 50-node deployments, where Morph narrows the gap to the fully connected upper bound within 0.5 percentage points on CIFAR-10. These results demonstrate that Morph achieves higher final accuracy, faster convergence, and more stable learning as quantified by lower inter-node variance, while requiring fewer communication rounds than baseline.

---

##### Figure 1: Topology Upodate

![](morph.png)

---

<!-- ##### Citation

Author 1, Author 2. Year. "Title." *Journal* Volume (Issue): First page–Last page. https://doi.org/paper_doi.

```BibTeX
@article{AAYY,
author = {Author 1 and Author 2},
doi = {paper_doi},
journal = {Journal},
number = {Issue},
pages = {XXX--YYY},
title = {Title},
volume = {Volume},
year = {Year}}
``` -->

---