+++ 
draft = false
date = 2018-10-18T22:34:08-04:00
title = "Are Abstracts Enough for Hypothesis Generation?"
slug = "" 
aliases = [
	"/2018/abstracts",
  "/publication/are-abstracts-enough-for-hg/",
]
authors = [
  "Justin Sybrandt",
  "Angelo Carrabba",
  "Alexander Herzog",
  "Ilya Safro"
]
venue = "BigData"
# Add these to specify external content
[[links]]
  name = "PDF"
  url = "https://arxiv.org/pdf/1804.05942.pdf"
  weight = 10
[[links]]
  name = "Code"
  url = "https://github.com/JSybrandt/MOLIERE"
  weight = 20
[[links]]
  name = "Dataset"
  url = "https://drive.google.com/drive/folders/11Nr4yPdkEUfg2LNsDRH-kTBL0Yghsgzi?usp=sharing"
  weight = 30
[[links]]
  name = "Slides"
  url = "/documents/big_data_2018_slides.pdf"
  weight = 40
+++

## Abstract:


The potential for automatic hypothesis generation (HG) systems to improve
research productivity keeps pace with the growing set of publicly available
scientific information. But as data becomes easier to acquire, we must
understand the effect different textual data sources have on our resulting
hypotheses. Are abstracts enough for HG, or does it need full-text papers? How
many papers does an HG system need to make valuable predictions? How sensitive
is a general-purpose HG system to hyperparameter values or input quality? What
effect does corpus size and document length have on HG results? To answer these
questions we train multiple versions of knowledge network-based HG system,
Moliere, on varying corpora in order to compare challenges and trade offs in
terms of result quality and computational requirements. Moliere generalizes main
principles of similar knowledge network-based HG systems and reinforces them
with topic modeling components. The corpora include the abstract and full-text
versions of PubMed Central, as well as iterative halves of MEDLINE, which allows
us to compare the effect document length and count has on the results. We find
that, quantitatively, corpora with a higher median document length result in
marginally higher quality results, yet require substantially longer to process.
However, qualitatively, full-length papers introduce a significant number of
intruder terms to the resulting topics, which decreases human interpretability.
Additionally, we find that the effect of document length is greater than that of
document count, even if both sets contain only paper abstracts.
