+++ 
draft = false
date = 2020-02-13T11:19:52-05:00
title = """
AGATHA: Automatic Graph-mining And Transformer based Hypothesis generation
Approach
"""
slug = "" 
aliases = [
  "/2020/agatha/"
]
authors = [
  "Justin Sybrandt",
  "Ilya Tyagin",
  "Michael Shtutman",
  "Ilya Safro",
]
venue = "CIKM2020"
# Add these to specify external content
[[links]]
  name = "PDF"
  url = "/documents/agatha_2020.pdf"
  weight = 10
[[links]]
  name = "Code"
  url = "https://github.com/JSybrandt/agatha"
  weight = 20
[[links]]
  name = "Pretrained Model"
  url = "https://drive.google.com/open?id=1Tka7zPF0PdG7yvGOGOXuEsAtRLLimXmP"
  weight = 30
+++

## Abstract:

Medical research is risky and expensive. Drug discovery, as an example, requires
that researchers efficiently winnow thousands of potential targets to a small
candidate set for more thorough evaluation. However, research groups spend
significant time and money to perform the experiments necessary to determine
this candidate set long before seeing intermediate results.  Hypothesis
generation systems address this challenge by mining the wealth of publicly
available scientific information to predict plausible research directions.  We
present AGATHA, a deep-learning hypothesis generation system that can introduce
data-driven insights earlier in the discovery process.  Through a learned
ranking criteria, this system quickly prioritizes plausible term-pairs among
entity sets, allowing us to recommend new research directions.  We massively
validate our system with a temporal holdout wherein we predict connections first
introduced after 2015 using data published beforehand.  We additionally explore
biomedical sub-domains, and demonstrate AGATHA's predictive capacity across the
twenty most popular relationship types.  This system achieves best-in-class
performance on an established benchmark, and demonstrates high recommendation
scores across subdomains.
