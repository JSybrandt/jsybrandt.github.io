+++ 
draft = false
date = 2017-08-13T22:49:09-04:00
title = "MOLIERE: Automatic Biomedical Hypothesis Generation System"
slug = "" 
aliases = [
  "/2017/moliere/",
]
authors = [
  "Justin Sybrandt",
  "Michael Shtutman",
  "Ilya Safro"
]
venue = "KDD"
# Add these to specify external content
[[links]]
  name = "PDF"
  url = "/documents/moliere.pdf"
  weight = 10
[[links]]
  name = "Code"
  url = "https://github.com/JSybrandt/MOLIERE"
  weight = 20
[[links]]
  name = "Slides"
  url = "https://www.slideshare.net/JustinSybrandt/moliere-automatic-biomedical-hypothesis-generation-system"
  weight = 30
[[links]]
  name = "Video"
  url = "https://www.youtube.com/watch?v=ra77iJ7r_Ys"
  weight = 40
+++

## Abstract:

Hypothesis generation is becoming a crucial time-saving technique which allows
biomedical researchers to quickly discover implicit connections between
important concepts. Typically, these systems operate on domain-specific
fractions of public medical data. MOLIERE, in contrast, utilizes information
from over 24.5 million documents and does not limit the document vocabulary. At
the heart of our approach lies a multi-modal and multi-relational network of
biomedical objects extracted from several heterogeneous datasets from the
National Center for Biotechnology Information (NCBI). These objects include but
are not limited to scientific papers, keywords, genes, proteins, diseases, and
diagnoses. We model hypotheses using Latent Dirichlet Allocation applied on
abstracts found near shortest paths discovered within this network. We
demonstrate the effectiveness of MOLIERE by performing hypothesis generation on
historical data. Our network, implementation, and resulting data are all
publicly available for the broad scientific community.
