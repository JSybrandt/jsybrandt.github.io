+++ 
draft = false
date = 2019-07-16T22:59:55-04:00
title = "FOBE and HOBE: First- and High-Order Bipartite Embeddings"
slug = "" 
aliases = [
  "/2019/fobe_hobe/",
  "/2020/fobe_hobe/"
]
authors = [
  "Justin Sybrandt",
  "Ilya Safro",
]
venue = "MLG2020"
# Add these to specify external content
[[links]]
  name = "PDF"
  url = "/documents/fobe_hobe.pdf"
  weight = 10
[[links]]
  name = "Code"
  url = "https://github.com/JSybrandt/HypergraphEmbedding"
  weight = 20
+++

## Abstract:

Typical graph embeddings may not capture type-specific bipartite graph features
that arise in such areas as recommender systems, data visualization, and drug
discovery. Machine learning methods utilized in these applications would be
better served with specialized embedding techniques. We propose two embeddings
for bipartite graphs that decompose edges into sets of indirect relationships
between node neighborhoods. When sampling higher-order relationships, we
reinforce similarities through algebraic distance on graphs. We also introduce
ensemble embeddings to combine both into a best of both worlds embedding. The
proposed methods are evaluated on link prediction and recommendation tasks and
compared with other state-of-the-art embeddings. While being all highly
beneficial in applications, we demonstrate that none of the considered
embeddings is clearly superior (in contrast to what is claimed in many papers),
and discuss the trade offs present among them.
