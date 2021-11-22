---
layout: page
title: Publications
permalink: /publications/
---

- #### UDIS: Unsupervised Discovery of Bias in Deep Visual Recognition Models
<span style="font-size:0.9em;"> Arvind Krishnakumar, Viraj Prabhu, Sruthi Sudhakar, Judy Hoffman. <em>British Machine Vision Conference (BMVC), 2021</em> <br/> 
Deep learning models have been shown to learn spurious correlations from data that sometimes lead to systematic failures for certain subpopulations. Prior work has typically diagnosed this by crowdsourcing annotations for various protected attributes and measuring performance, which is both expensive to acquire and difficult to scale. In this work, we propose UDIS, an unsupervised algorithm for surfacing and analyzing such failure modes. UDIS identifies subpopulations via hierarchical clustering of dataset embeddings and surfaces systematic failure modes by visualizing low performing clusters along with their gradient-weighted class-activation maps. We show the effectiveness of UDIS in identifying failure modes in models trained for image classification on the CelebA and MSCOCO datasets. <br />

[code](https://github.com/akrishna77/bias-discovery) | [paper](https://www.bmvc2021-virtualconference.com/conference/papers/paper_0362.html)

</span>

- #### Mitigating Bias in Visual Transformers via Targeted Alignment
<span style="font-size:0.9em;"> Sruthi Sudhakar, Viraj Prabhu, Arvind Krishnakumar, Judy Hoffman. <em>British Machine Vision Conference (BMVC), 2021</em> <br/> 
As transformer architectures become increasingly prevalent in computer vision, it is critical to understand their fairness implications. We perform the first study of the fairness of transformers applied to computer vision and benchmark several bias mitigation approaches from prior work. We visualize the feature space of the transformer self-attention modules and discover that a significant portion of the bias is encoded in the query matrix. With this knowledge, we propose TADeT, a targeted alignment strategy for debiasing transformers that aims to discover and remove bias primarily from query matrix features. We measure performance using Balanced Accuracy and Standard Accuracy, and fairness using Equalized Odds and Balanced Accuracy Difference. TADeT consistently leads to improved fairness over prior work on multiple attribute prediction tasks on the CelebA dataset, without compromising performance. <br />

[paper](https://www.bmvc2021-virtualconference.com/conference/papers/paper_0282.html)

</span>