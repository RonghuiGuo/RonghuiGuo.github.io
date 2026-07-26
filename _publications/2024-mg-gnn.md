---
title: "MG-GNN: Enhancing GNNs for Anomaly Detection via Minority Class Sample Generation"
collection: publications
category: conferences
permalink: /publication/2024-mg-gnn
excerpt: 'A method that generates minority class samples in the hidden space to address class imbalance in graph anomaly detection, using BWGNN backbone and SMOTE-based interpolation.'
date: 2024-11-11
venue: 'ISWC 2024 Posters, Demos and Industry Tracks'
paperurl: 'https://ceur-ws.org/Vol-3828/paper5.pdf'
citation: 'Ronghui Guo, Minghui Zou, Sai Zhang, Xiaowang Zhang, and Zhiyong Feng. (2024). "MG-GNN: Enhancing GNNs for Anomaly Detection via Minority Class Sample Generation." <i>ISWC 2024 Posters, Demos and Industry Tracks</i>, CEUR Workshop Proceedings, Vol. 3828.'
---
In graph anomaly detection, the number of anomalous nodes is typically far fewer than that of normal nodes. To address the issue of class imbalance, existing Graph Neural Networks (GNNs) tend to overlook anomalous (minority class) node samples, resulting in suboptimal performance.

To solve this, we propose **MG-GNN**, which generates minority class samples for GNNs in the hidden space, thereby improving the classification performance for anomalous nodes. MG-GNN consists of three main components: (1) a GNN encoder (specifically BWGNN, chosen for its ability to handle heterophily in anomaly graphs) that maps node features and structural information into hidden space; (2) a Synthetic Node Generator that uses a SMOTE-based interpolation approach in the hidden space to generate synthetic minority (anomalous) class nodes, achieving a more balanced class distribution; and (3) a classifier (MLP) that performs final prediction on the balanced representations.

Experiments on the YelpChi and Amazon datasets demonstrate that MG-GNN outperforms the baseline BWGNN across all metrics (F1-macro, AUC, and GMean), confirming that generating minority class samples in hidden space effectively mitigates class imbalance and improves anomaly detection performance.
