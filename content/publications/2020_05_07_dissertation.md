+++ 
draft = false
date = 2020-05-07T01:01:01-01:00
title = "Exploiting Latent Features of Text and Graphs"
slug = "" 
aliases = [
  "/dissertation/"
]
authors = [
  "Justin Sybrandt",
]
venue = "Dissertation"
[[links]]
  name = "PDF"
  url = "/documents/dissertation.pdf"
  weight = 10
+++

## Introduction:

The fastest growing online data sources include unstructured text and large
graphs. These data are particularly prevalent in biomedical science, as large
databases of scientific papers and archives of experimentally derived
relationships entomb a vast amount of knowledge. While collections of text and
graphs may be useful for human readers to understand, their ever-expanding size
and scope creates a scalability challenge. To aid human researchers in
scientific explorations, we propose new techniques that enable machine
understanding of scientific text and graphs. To do so, we use
embeddings---semantically rich vectors of latent features---to convert human
constructs into mathematical representations.

In this dissertation we propose a range of new techniques and systems for
automatic hypothesis generation, the process of using existing scientific
information to anticipate fruitful new research directions. This exploration
includes the Moliere system, which uses text embeddings to construct a large
semantic graph containing associations between biomedical concepts. Through
graph and text analytics the Moliere system uncovers nontrivial implicit
connections within biomedical science. We augment this system to produce a novel
ranking criteria, which enables large-scale validation and massive real-world
experiments. We apply the Moliere system to the problem of HIV-associated
neurodegenerative disorder in order to automatically identify a new
gene-treatment target in DDX3. We confirm this mathematically derive
hypothesis in a laboratory setting.

Additionally, we propose a new graph-embedding technique suited for bipartite
graphs, such as the gene-disease or the drug-side effect graphs, and demonstrate
that it can better capture type-specific latent features. We further demonstrate
this new embeddings effectiveness by proposing an embedding-based solution
strategy to the NP-Hard algorithmic problem of hypergraph partitioning. By using
the global structural features of graph embeddings we substantially improve
partitioning result quality, which in real-world applications corresponds to a
significant decrease in communication overhead in large scientific workloads.

Using recent advances in deep learning and graph embedding, we construct a
next-generation hypothesis generation system, Agatha, which challenges a range
of assumptions present in Moliere. Using our proposed validation technique, we
demonstrate a substantial quality improvement in ranking plausible future
research directions. Furthermore, the Agatha system queries potential hypotheses
two orders of magnitude faster than its counterpart, enabling whole new
discovery paradigms.

To supplement our quantitative ranking criteria with more interpretable
information, we propose a text generation model that can author biomedical
summaries. We propose the conditional biomedical abstract generator, a
deep-learning language model that allows us to modify the content of
automatically generated text based on a set of desired elements of interest. As
a result, we gain the ability to generate human-understandable content that
could help describe automatically derived hypotheses.
