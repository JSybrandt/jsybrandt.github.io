+++ 
draft = false
date = 2020-04-01T11:19:52-05:00
title = "Unsupervised Hierarchical Graph Representation Learning by Mutual Information Maximization"
slug = "" 
aliases = [
  "/2020/unsupervised/"
]
authors = [
  "Fei Ding",
  "Xiaohong Zhang",
  "Justin Sybrandt",
  "Ilya Safro",
]
venue = "MLG2020"
# Add these to specify external content
[[links]]
  name = "PDF"
  url = "https://arxiv.org/abs/2003.08420"
  weight = 10
+++

## Abstract:

Graph representation learning based on graph neural networks (GNNs) can greatly
improve the performance of downstream tasks, such as node and graph
classification. However, the general GNN models do not aggregate node
information in a hierarchical manner, and can miss key higher-order structural
features of many graphs. The hierarchical aggregation also enables the graph
representations to be explainable. In addition, supervised graph representation
learning requires labeled data, which is expensive and error-prone. To address
these issues, we present an unsupervised graph representation learning method,
Unsupervised Hierarchical Graph Representation (UHGR), which can generate
hierarchical representations of graphs. Our method focuses on maximizing mutual
information between "local" and high-level "global" representations, which
enables us to learn the node embeddings and graph embeddings without any labeled
data. To demonstrate the effectiveness of the proposed method, we perform the
node and graph classification using the learned node and graph embeddings. The
results show that the proposed method achieves comparable results to
state-of-the-art supervised methods on several benchmarks.  In addition, our
visualization of hierarchical representations indicates that our method can
capture meaningful and interpretable clusters.
