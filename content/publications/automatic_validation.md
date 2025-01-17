+++ 
draft = false
date = 2018-10-18T22:43:39-04:00
title = """
  Large-Scale Validation of Hypothesis Generation Systems via Candidate Ranking
"""
slug = "" 
aliases = [
	"/2018/validation",
  "/publication/validation-and-topic-driven-ranking/",
]
authors = [
  "Justin Sybrandt",
  "Micheal Shtutman",
  "Ilya Safro"
]
venue = "BigData"
# Add these to specify external content
[[links]]
  name = "PDF"
  url = "https://arxiv.org/pdf/1802.03793.pdf"
  weight = 10
[[links]]
  name = "Code"
  url = "https://github.com/JSybrandt/MOLIERE"
  weight = 20
[[links]]
  name = "Dataset"
  url = "https://github.com/JSybrandt/Moliere_Validation_Data"
  weight = 30
[[links]]
  name = "Slides"
  url = "/documents/big_data_2018_slides.pdf"
  weight = 40
+++

## Abstract:


The first step of many research projects is to define and rank a short list of
candidates for study. In the modern rapidity of scientific progress, some turn
to automated hypothesis generation (HG) systems to aid this process. These
systems can identify implicit or overlooked connections within a large
scientific corpus, and while their importance grows alongside the pace of
science, they lack thorough validation. Without any standard numerical
evaluation method, many validate general-purpose HG systems by rediscovering a
handful of historical findings, and some wishing to be more thorough may run
laboratory experiments based on automatic suggestions. These methods are
expensive, time consuming, and cannot scale. Thus, we present a numerical
evaluation framework for the purpose of validating HG systems that leverages
thousands of validation hypotheses. This method evaluates a HG system by its
ability to rank hypotheses by plausibility; a process reminiscent of human
candidate selection. Because HG systems do not produce a ranking criteria,
specifically those that produce topic models, we additionally present novel
metrics to quantify the plausibility of hypotheses given topic model system
output. Finally, we demonstrate that our proposed validation method aligns with
real-world research goals by deploying our method within Moliere, our recent
topic-driven HG system, in order to automatically generate a set of candidate
genes related to HIV-associated neurodegenerative disease (HAND). By performing
laboratory experiments based on this candidate set, we discover a new connection
between HAND and Dead Box RNA Helicase 3 (DDX3).
