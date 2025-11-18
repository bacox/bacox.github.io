---
title: "Parameterizing federated continual learning for reproducible research" 
date: 2025-01-01
url: /paper/parameterizing-federated-continual-learning-for-reproducible-research
aliases: 
    - /old_url.html
tags: ["Federated Continual Learning","Resource and Data Heterogeneity","Reproducible Research", "Continual Learning"]
author: ["Bart Cox", "Jeroen Galjaard", "Aditya Shankar", "Jérémie Decouchant","Lydia Y. Chen"]
description: "We present a fully configurable framework for Federated Continual Learning, enabling reproducible, large-scale experiments and revealing key performance challenges." 
summary: "We present the first fully configurable framework for Federated Continual Learning, designed to reproduce complex, evolving learning scenarios. It supports large-scale deployments via containerization and Kubernetes, enabling precise experimentation. Demonstrations on CIFAR-100 and heterogeneous task sequences show Freddie’s effectiveness and uncover persistent performance challenges in real FCL settings."
draft: false
cover:
    image: "freddie.png"
    alt: "Reduced catastrophic forgetting effect (preferably 1280x720 pixels)"
    relative: true
editPost:
    URL: "https://doi.org/10.1007/978-3-031-74643-7_35"
    Text: "Machine Learning and Principles and Practice of Knowledge Discovery in Databases. ECML PKDD 2023"

---

---

##### Links:

- [Publication](https://link.springer.com/chapter/10.1007/978-3-031-74643-7_35)
- [Paper](https://arxiv.org/pdf/2406.02015)
- [Code](https://gitlab.ewi.tudelft.nl/dmls/publications/freddie)

---

##### Abstract:

Federated Learning (FL) systems evolve in heterogeneous and ever-evolving environments that challenge their performance. Under real deployments, the learning tasks of clients can also evolve with time, which calls for the integration of methodologies such as Continual Learning. To enable research reproducibility, we propose a set of experimental best practices that precisely capture and emulate complex learning scenarios. Our framework, Freddie, is the first entirely configurable framework for Federated Continual Learning (FCL), and it can be seamlessly deployed on a large number of machines thanks to the use of Kubernetes and containerization. We demonstrate the effectiveness of Freddie on two use cases, (i) large-scale FL on CIFAR100 and (ii) heterogeneous task sequence on FCL, which highlight unaddressed performance challenges in FCL scenarios.

---

##### Figure 4:  Reduced catastrophic forgetting effect

![](freddie.png)

---

##### Citation

Cox, B., Galjaard, J., Shankar, A., Decouchant, J., Chen, L.Y. (2025). Parameterizing Federated Continual Learning for Reproducible Research. In: Meo, R., Silvestri, F. (eds) Machine Learning and Principles and Practice of Knowledge Discovery in Databases. ECML PKDD 2023. Communications in Computer and Information Science, vol 2137. Springer, Cham. https://doi.org/10.1007/978-3-031-74643-7_35
```BibTeX
@InProceedings{10.1007/978-3-031-74643-7_35,
author="Cox, Bart
and Galjaard, Jeroen
and Shankar, Aditya
and Decouchant, J{\'e}r{\'e}mie
and Chen, Lydia Y.",
title="Parameterizing Federated Continual Learning for Reproducible Research",
booktitle="Machine Learning and Principles and Practice of Knowledge Discovery in Databases",
year="2025",
publisher="Springer Nature Switzerland",
address="Cham",
pages="478--486",
isbn="978-3-031-74643-7"
}
```

---