
+++ 
draft = false
date = 2019-09-09T01:34:08-04:00
title = "Hypergraph Partitioning with Embeddings"
slug = "" 
aliases = [
  "/2019/partition/",
]
authors = [
  "Justin Sybrandt",
  "Ruslan Shaydulin",
  "Ilya Safro"
]
venue = "TKDE"
# Add these to specify external content
[[links]]
  name = "PDF"
  url = "/documents/partitioning_2019.pdf"
  weight = 10
[[links]]
  name = "Result Data"
  url = "https://drive.google.com/file/d/13ZRMFf0_VULYqoQHabgejJlsv-MEgn95/view?usp=sharing"
  weight = 30
[[links]]
  name = "Supplemental Info"
  url = "/2019/supl/partition"
  weight = 40
+++

## Abstract:

The problem of placing circuits on a chip or distributing sparse matrix
operations can be modeled as the hypergraph partitioning problem.  A hypergraph
is a generalization of the traditional graph wherein each "hyperedge" may
connect any number of nodes.  Hypergraph partitioning, therefore, is the NP-Hard
problem of dividing nodes into $k$ similarly sized disjoint sets while
minimizing the number of hyperedges that span multiple partitions. Due to this
problem's complexity, many partitioners leverage the multilevel heuristic of
iteratively "coarsening" their input to a smaller approximation until an
inefficient algorithm becomes feasible. The initial solution is then propagated
back to the original hypergraph, which produces a reasonably accurate result
provided the coarse representation preserves structural properties of the
original.  The multilevel hypergraph partitioners are considered today as
state-of-the-art solvers that achieve an excellent quality/running time
trade-off on practical large-scale instances of different types.  In order to
improve the quality of multilevel hypergraph partitioners, we propose leveraging
graph embeddings to better capture structural properties during the coarsening
process. Our approach prioritizes dense subspaces found at the embedding, and
contracts nodes according to both traditional and embedding-based similarity
measures.  Reproducibility: All source code, plots and experimental data are
available at https://sybrandt.com/2019/partition.

