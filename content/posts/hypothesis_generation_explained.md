+++ 
draft = false
date = "2017-09-15T23:18:26-04:00"
title = "Hypothesis Generation Explained"
slug = "" 
description = """
  A sizable write up that details the basics of hypothesis generation, and how
  the Moliere project fits in.
"""
aliases = [
  "/post/hypothesis-generation-explained/"
]
+++

# Undiscovered Public Knowledge

In the last couple of years, researchers worldwide have begun to develop a powerful new tool. By using data mining techniques, these scientists hope to one day put themselves out of a job.

It all began in the 80's with a man named Don Swanson. He was the first to notice something that he called undiscovered public knowledge. He saw that no human could possibly read all of the available information on a given topic, and he guessed that there were some truths that no one actually knows, but have already been published. 

Big ideas are often discovered when people from different backgrounds get together on the same team. These ideas crop up because cross-disciplinary collaboration brings in not only a new viewpoint, but people who entirely different sets of mental information. For example, the idea of DNA storage has been recently popularized by Harvard scientists as a way to keep massive amounts of digital data. This bioinformatic technology relies on the connection that DNA and SSD's are both solutions to the same core problem: information storage.

DNA was originally proposed as a means for data storage in 1964. Up until that point, there had been papers about DNA in medical journals, and there had been papers about hard drives in technical journals. Typically, doctors don't tend to meet many people from IBM at dinner parties, so it was not likely that many doctors knew how hard drives worked, or IBM employees who could describe DNA's storage capabilities. But without realizing it, both communities explored the same problem. This is an example of Don Swanson's undiscovered public knowledge.

Before 1964, no one was saying DNA had anything to do with hard drives, but there existed an implicit connection: both addressed information storage. If someone was capable of keeping all technical and medical literature in their head simultaneously, this connection might seem trivial. And now, looking back on it, the connection seems pretty clear to us. What we attempt to do with hypothesis generation is exactly this; we try to identify these implicit connections.
Current State of the Art

Right now, most hypothesis generation systems are beginning to become really powerful, and almost all of them stick to the field of medicine. This is for two main reasons:  Firstly there is a wealth of public information available about medicine. PubMed.gov is a service which allows anyone to search for medical papers, and we can download all of them! This dataset consists of over 24.5 million papers dating all the way back to the late 1800's.  Secondly, medicine is important! We are in the business of curing cancer with computers! Who doesn't want to say that at a dinner party?  All of these systems tend to have a similar structure. They start with paper data from PubMed and typically select a subset of the literature they think is relevant to some particular inquiry. They might also take in some keyword data, gene data, or other domain specific information to help make their decision. After this the team applies some statistical and/or machine learning techniques eventually resulting in a program which allows a user to request some information.

Right now, these systems are starting to be used in the real world. Drug companies use techniques like this to figure out what to do with their R&D budgets. Drug research is very costly and, like all research, results are not guaranteed. Hypothesis generation promises to give these companies a better return on their investments.That return can be even bigger when we start considering drug-repurposing.

When a scientist develops a new drug to treat some disease, they typically focus on a specific biological function which the drug is intended to change. For example, a specific protein might be responsible for a viral disease, so drugs will focus on changing how that protein interacts in the body. If we later discover that the same protein is responsible for certain types of cancer, it is likely that we can use the same anti-viral drugs to treat them. This sort of discovery is perfect for hypothesis generation.

Many current hypothesis generation systems require the user to specify two keywords, such as an anti-viral drug, and a protein for example. From this, the system could possibly discover types of cancer or the stages in cancer development. This discovery would imply to a human scientist that it is worthwhile to investigate this drug repurposing. 

# MOLIERE

In the last couple of months, I have worked on MOLIERE, a new hypothesis generation system that can find conceptual links within the entire PubMed data set. We built MOLIERE to be more generalized than other systems which limit their search to specific proteins or keywords. Instead, we process all 24.5 million medical papers and learn a whole lot about them. We still allow people to query for the links between two keywords, but we use some machine learning and natural language processing techniques to give that user a list of topics which we believe are connected to the search.

We found that we can detect a lot of really interesting relationships. We did some tests using historical data, meaning we only looked at papers published before anyone had actually found these relationships, and we saw that MOLIERE could identify them anyway!

One of our best results was around the gene DDX3. It has been known to be involved with the transmission of HIV, but more recently it has been found to be linked to cancer development. There exist viral drugs intended to help treat HIV by interacting with DDX3, and these have been prime repurposing candidates for cancer treatments. So to run our experiments, we went back to 2009 before any of this had been discovered.

We looked for the associations between DDX3 and certain cancer concepts, primarily those involved with the "wnt signaling pathway." Although I am not a biologist, it is my understanding that cancer cells spread to new parts of the body through this. The concepts which MOLIERE found all indicated that there is a strong relationship between DDX3 and the wnt signaling pathway. We even identify the types of interactions DDX3 has in this process.
