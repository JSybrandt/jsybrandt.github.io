+++ 
draft = false
date = 2021-07-06T11:20:00-05:00
title = "CBAG: Conditional Biomedical Abstract Generation"
slug = "" 
aliases = [
  "/2020/cbag/",
  "/2021/cbag/"
]
authors = [
  "Justin Sybrandt",
  "Ilya Safro",
]
venue = "PLOS ONE"
# Add these to specify external content
[[links]]
  name = "PLOS ONE"
  url = "https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0253905"
  weight = 5
[[links]]
  name = "PDF"
  url = "/documents/cbag_2020.pdf"
  weight = 10
[[links]]
  name = "Code"
  url = "https://github.com/JSybrandt/agatha/tree/master/agatha/ml/abstract_generator"
  weight = 20
[[links]]
  name = "Pretrained Model"
  url = "https://drive.google.com/open?id=19645oQA6MSnmV8tV2J_meF3iI2Puj41A"
  weight = 30
[[links]]
  name = "Result Data"
  url = "https://drive.google.com/open?id=1O327cWOkDGUR5p-TSNwyTyrA9mhUJ0kn"
  weight = 40
+++

## Abstract:

Biomedical research papers often combine disjoint concepts in novel ways, such
as when describing a newly discovered relationship between an understudied gene
with an important disease. These concepts are often explicitly encoded as
metadata keywords, such as the author-provided terms included with many
documents in the MEDLINE database. While substantial recent work has addressed
the problem of text generation in a more general context, applications, such as
scientific writing assistants, or hypothesis generation systems, could benefit
from the capacity to select the specific set of concepts that underpin a
generated biomedical text. We propose a conditional language model following the
transformer architecture. This model uses the “encoder stack” to encode concepts
that a user wishes to discuss in the generated text. The “decoder stack” then
follows the masked self-attention pattern to perform text generation, using both
prior tokens as well as the encoded condition. We demonstrate that this approach
provides significant control, while still producing reasonable biomedical text.
