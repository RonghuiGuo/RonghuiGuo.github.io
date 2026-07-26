---
title: "Effective Hybrid Graph and Hypergraph Convolution Network for Collaborative Filtering"
collection: publications
category: manuscripts
permalink: /publication/2022-hybrid-graph-cf
excerpt: 'An interpretable hybrid framework combining graph and hypergraph convolution networks for collaborative filtering, with optimized dense information flow.'
date: 2022-09-03
venue: 'Neural Computing and Applications (NCA), Vol. 35, No. 3'
paperurl: 'https://doi.org/10.1007/s00521-022-07735-y'
citation: 'Xunkai Li, Ronghui Guo, Jianwen Chen, Youpeng Hu, Meixia Qu, and Bin Jiang. (2022). "Effective Hybrid Graph and Hypergraph Convolution Network for Collaborative Filtering." <i>Neural Computing and Applications (NCA)</i>, Vol. 35, No. 3, pp. 2633–2646.'
---
In recent years, graph convolution networks and hypergraph convolution networks have become a research hotspot in collaborative filtering (CF) because of their information extraction ability in dealing with user-item interaction information. In particular, hypergraphs can model high-order correlation of users and items to achieve better performance. However, existing graph-based CF methods for mining interactive information remain incomplete and limit model expressiveness. Moreover, they directly use low-order Chebyshev polynomials to fit the convolution kernel of graph and hypergraph without experimental proof or analysis, lacking interpretability.

We propose an **Effective Hybrid Graph and Hypergraph Convolutional Network (EHGCN)** for CF to obtain a capable and interpretable framework. In EHGCN, the graph and the hypergraph are used to model the correlation among nodes in the interaction graph for multilevel learning. EHGCN also optimizes the information flow framework (called DenseGCN) to match the improved convolution strategy of the graph and hypergraph. Extensive experiments on four real-world datasets show considerable improvements of EHGCN over state-of-the-art methods. Moreover, we analyze the graph and hypergraph convolution kernel in terms of the spectral domain to reveal the core of graph-based CF, which has a heuristic effect on future work.
