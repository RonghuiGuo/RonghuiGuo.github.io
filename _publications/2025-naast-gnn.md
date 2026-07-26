---
title: "NAAST-GNN: Neighborhood Adaptive Aggregation and Spectral Tuning for Graph Anomaly Detection"
collection: publications
category: conferences
permalink: /publication/2025-naast-gnn
excerpt: 'A novel GNN model addressing heterophily in graph anomaly detection through neighborhood adaptive aggregation in the spatial domain and spectral tuning in the spectral domain.'
date: 2025-08-16
venue: 'Proceedings of the 34th International Joint Conference on Artificial Intelligence (IJCAI 2025)'
paperurl: 'https://doi.org/10.24963/ijcai.2025/317'
citation: 'Ronghui Guo, Xiaowang Zhang, Zhizhi Yu, Minghui Zou, Sai Zhang, and Zhiyong Feng. (2025). "NAAST-GNN: Neighborhood Adaptive Aggregation and Spectral Tuning for Graph Anomaly Detection." <i>Proceedings of the 34th International Joint Conference on Artificial Intelligence (IJCAI ''25)</i>, pp. 2847–2855.'
---
Heterophily emerges as a critical challenge in Graph Anomaly Detection (GAD). Recent studies reveal that neighborhood distributions, rather than heterophily itself, are the fundamental factor for the expressive power of Graph Neural Networks (GNNs). However, two key challenges remain unresolved. First, the overlap in neighborhood distributions between anomalous and normal nodes poses significant difficulties in distinguishing them effectively. Second, the dispersion in neighborhood distributions within the same class prevents the application of a fixed aggregation strategy to accommodate the diverse patterns within the class.

To tackle the aforementioned challenges, we propose a novel Graph Neural Network model called **Neighborhood Adaptive Aggregation and Spectral Tuning (NAAST-GNN)**. Specifically, we first design a neighborhood adaptive aggregation module that adjusts the message passing mechanism based on the predicted probabilities for different node classes, ensuring that nodes from distinct classes but with similar neighborhood distributions derive unique aggregated neighborhood information. We then present a spectral tuning module that dynamically selects and combines spectral filters based on the predicted neighborhood distribution, ensuring adaptability to the diverse neighborhood distributions of nodes within the same class. Comprehensive experimental results demonstrate that our method outperforms state-of-the-art baselines.
