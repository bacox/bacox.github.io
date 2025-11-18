---
title: "Go With The Flow: Churn-Tolerant Decentralized Training of Large Language Models" 
date: 2025-11-08
url: /paper/Go-With-The-Flow:-Churn-Tolerant-Decentralized-Training-of-Large-Language-Models
aliases: 
    - /old_url.html
tags: ["Large Language Model", "Decentralized learning", "Crash-tolerance", "Flow optimization"]
author: ["Nikolay Blagoev", "Bart Cox", "Jérémie Decouchant", "Lydia Y. Chen"]
description: "GWTF is a crash-tolerant decentralized LLM training framework that handles churn and instability, optimizing microbatch routing and cutting training time by up to 45%." 
summary: "GWTF is the first practical, crash-tolerant decentralized framework for collaboratively training LLMs on heterogeneous volunteer clients. It handles node churn and unstable networks through a novel decentralized flow algorithm that optimizes microbatch routing. Evaluations on GPT- and LLaMa-like models show that GWTF reduces training time by up to 45% in challenging, geographically distributed settings."
draft: false
cover:
    image: "gwtf.png"
    alt: "Crash-recovery during decentralized training of an LLM"
    relative: true
editPost:
    URL: "https://doi.org/10.48550/arXiv.2509.21221"
    Text: "IEEE Big Data"

---

---

##### Links:

- [Publication](https://doi.org/10.48550/arXiv.2509.21221)
- [Paper](https://arxiv.org/pdf/2509.21221)
- [Code](https://github.com/paper_repo)

---

##### Abstract:

Motivated by the emergence of large language models (LLMs) and the importance of democratizing their training, we propose GWTF, the first crash tolerant practical decentralized training framework for LLMs. Differently from existing distributed and federated training frameworks, GWTF enables the efficient collaborative training of a LLM on heterogeneous clients that volunteer their resources. In addition, GWTF addresses node churn, i.e., clients joining or leaving the system at any time, and network instabilities, i.e., network links becoming unstable or unreliable. The core of GWTF is a novel decentralized flow algorithm that finds the most effective routing that maximizes the number of microbatches trained with the lowest possible delay. We extensively evaluate GWTF on GPT-like and LLaMa-like models and compare it against the prior art. Our results indicate that GWTF reduces the training time by up to 45% in realistic and challenging scenarios that involve heterogeneous client nodes distributed over 10 different geographic locations with a high node churn rate. 

---

##### Figure 1:  Crash-recovery during decentralized training of an LLM

![](gwtf.png)

---

##### Citation

Blagoev, N., Cox, B., Decouchant, J., & Chen, L. Y. (2025). Go With The Flow: Churn-Tolerant Decentralized Training of Large Language Models. arXiv preprint arXiv:2509.21221. https://doi.org/10.48550/arXiv.2509.21221.

```BibTeX
@misc{blagoev2025flowchurntolerantdecentralizedtraining,
      title={Go With The Flow: Churn-Tolerant Decentralized Training of Large Language Models}, 
      author={Nikolay Blagoev and Bart Cox and Jérémie Decouchant and Lydia Y. Chen},
      year={2025},
      eprint={2509.21221},
      archivePrefix={arXiv},
      primaryClass={cs.LG},
      url={https://arxiv.org/abs/2509.21221}, 
}
```

---