+++ 
draft = false
date = 2020-12-10T01:01:01-01:00
title = "Accelerating Text Mining Using Domain-Specific Stop Word Lists"
slug = "" 
aliases = [
  "/2020/accelerating-text-mining/"
]
authors = [
  "Farah Alshanik",
  "Amy Apon",
  "Alexander Herzog",
  "Ilya Safro",
  "Justin Sybrandt"
]
venue = "Big Data 2020"
[[links]]
  name = "PDF"
  url = "/documents/2020_12_10_accelerating_text_mining.pdf"
  weight = 10
+++

## Abstract:

Text preprocessing is an essential step in text mining. Removing words that can
negatively impact the quality of prediction algorithms or are not informative
enough is a crucial storage-saving technique in text indexing and results in
improved computational efficiency. Typically, a generic stop word list is
applied to a dataset regardless of the domain. However, many common words are
different from one domain to another but have no significance within a
particular domain. Eliminating domain-specific common words in a corpus reduces
the dimensionality of the feature space, and improves the performance of text
mining tasks. In this paper, we present a novel mathematical approach for the
automatic extraction of domain-specific words called the hyperplane-based
approach. This new approach depends on the notion of low dimensional
representation of the word in vector space and its distance from hyperplane. The
hyperplane-based approach can significantly reduce text dimensionality by
eliminating irrelevant features. We compare the hyperplane-based approach with
other feature selection methods, namely \c{hi}2 and mutual information. An
experimental study is performed on three different datasets and five
classification algorithms, and measure the dimensionality reduction and the
increase in the classification performance. Results indicate that the
hyperplane-based approach can reduce the dimensionality of the corpus by 90% and
outperforms mutual information. The computational time to identify the
domain-specific words is significantly lower than mutual information.
