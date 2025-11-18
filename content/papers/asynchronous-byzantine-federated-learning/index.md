---
title: "Asynchronous Byzantine Federated Learning" 
date: 2024-06-20
url: /paper/asynchronous-byzantine-federated-learning
aliases: 
    - /old_url.html
tags: ["Byzantine Learning", "Asynchronous Learning", "Re-source Heterogeneity"]
author: ["Bart Cox", "Abele Mălan", "Lydia Y. Chen", "Jérémie Decouchant"]
description: "An asynchronous, Byzantine-resilient FL algorithm that needs no server dataset, avoids stragglers, and outperforms prior methods in speed and accuracy under attacks." 
summary: "We propose an asynchronous, Byzantine-resilient FL algorithm that avoids straggler delays and requires no server dataset. By updating after a safe number of client contributions, it outperforms state-of-the-art methods, achieving faster training and higher accuracy under multiple attack types."
draft: false
cover:
    image: "paper_figure.png"
    alt: ""
    relative: true
editPost:
    URL: "https://doi.org/10.48550/arXiv.2406.01438"
    Text: "Arxiv"

---

---

##### Links:

- [Publication](https://arxiv.org/abs/2406.01438)
- [Paper](https://arxiv.org/pdf/2406.01438)
- [Code](https://github.com/bacox/Catalyst)

---

##### Abstract:

Federated learning (FL) enables a set of geographically distributed clients to collectively train a model through a server. Classically, the training process is synchronous, but can be made asynchronous to maintain its speed in presence of slow clients and in heterogeneous networks. The vast majority of Byzantine fault-tolerant FL systems however rely on a synchronous training process. Our solution is one of the first Byzantine-resilient and asynchronous FL algorithms that does not require an auxiliary server dataset and is not delayed by stragglers, which are shortcomings of previous works. Intuitively, the server in our solution waits to receive a minimum number of updates from clients on its latest model to safely update it, and is later able to safely leverage the updates that late clients might send. We compare the performance of our solution with state-of-the-art algorithms on both image and text datasets under gradient inversion, perturbation, and backdoor attacks. Our results indicate that our solution trains a model faster than previous synchronous FL solution, and maintains a higher accuracy, up to 1.54x and up to 1.75x for perturbation and gradient inversion attacks respectively, in the presence of Byzantine clients than previous asynchronous FL solutions. 

---

<!-- ##### Figure X:  Figure title

![](figurex.png) -->

---

##### Citation

Cox, B., Mălan, A., Chen, L. Y., & Decouchant, J. (2024). Asynchronous byzantine federated learning. arXiv preprint arXiv:2406.01438. https://doi.org/10.48550/arXiv.2406.01438.

```BibTeX
@misc{cox2024asynchronousbyzantinefederatedlearning,
      title={Asynchronous Byzantine Federated Learning}, 
      author={Bart Cox and Abele Mălan and Lydia Y. Chen and Jérémie Decouchant},
      year={2024},
      eprint={2406.01438},
      archivePrefix={arXiv},
      primaryClass={cs.LG},
      url={https://arxiv.org/abs/2406.01438}, 
}
```

---