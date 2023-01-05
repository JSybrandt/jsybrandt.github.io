+++ 
draft = false
date = "2018-02-28T14:18:52-04:00"
title = "Moliere Software Overhaul"
slug = "" 
description = """
  Having just completed a major rewrite to Moliere, this documents new features
  and changes. Key points: new query interface and addition of SemMedDB
  predicates.
"""
aliases = [
  "/posts/moliere-project-update-18-2-28/",
  "/updates/moliere_software_overhaul/"
]
+++

Over the last couple of days, I have retooled MOLIERE into a system that anyone[^1] can deploy it and run their own queries.
The code is over at the [default repo][moliere_repo][^2] and should be pretty straightforward, the code even downloads raw data itself!
Just run `build_network.py` and point it at a big parallel file systen --- in a few hours you'll have your very own knowledge network!

This project was a pretty crazy conglomeration of everything I've been up to.
To start, this implements a new stopword cleaning method (inspired by [this list from Swanson][stopword_list]).
We also use a new phrase mining tool, [AutoPhrase][autophrase_git_link], to replace ToPMine.

Overall, these improvements are qualitatively more interpretable than the previous method.
And, the changes in the codebase make it easier to add or remove new data sources.
For example, this network construction script can choose to include [UMLS][UMLS_link] based on whether the use has it installed.
I'm planning on extending this to incorporate [SemMedDB][semmeddb_link] and hopefully some gene-specific data.

Also, in the short-term, I'm hoping to redo my validation experiments, as presented in [this paper][validation_paper_link], to see how these changes may have improved our overall performance.


[^1]: With a big enough super computer.
[^2]: For anyone keeping up with the development, this code will look familiar to the MOLIERE\_QUERY\_RUNNER repo. This code is going to be phased out for the newly updated repo.
[stopword_list]:http://arrowsmith.psych.uic.edu/arrowsmith_uic/data/stopwords_pubmed
[autophrase_git_link]:https://github.com/shangjingbo1226/AutoPhrase
[UMLS_link]:https://www.nlm.nih.gov/research/umls/
[semmeddb_link]:https://skr3.nlm.nih.gov/SemMedDB/
[moliere_repo]:https://github.com/JSybrandt/MOLIERE
[validation_paper_link]:https://arxiv.org/abs/1802.03793
