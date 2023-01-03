+++ 
draft = false
date = 2015-11-16T22:54:47-04:00
title = "Rapid Replication of Multi-Petabyte File Systems"
slug = "" 
aliases = [
  "/publication/rapid-replication-of-multipetabyte-filesystems/"
]
authors = ["Justin Sybrandt", "Jason Hick"]
venue = "PDSW"
# Add these to specify external content
[[links]]
  name = "PDF"
  url = "http://www.pdsw.org/pdsw15/wips/wip-sybrandt.pdf"
  weight = 10
[[links]]
  name = "Code"
  url = "https://github.com/JSybrandt/DistSync"
  weight = 20
+++

## Abstract:


As  file  systems  grow  larger,  tools  which  were  once  industry standard
become  unsustainable  at  scale.   Today,  large  data sets containing hundreds
of millions of files often take longer to traverse than to copy.  The time
needed to replicate a file system  has  grown  from  hours  to  weeks,  an
unrealistic  wait for  a  backup.   Distsync  is  our  new  utility  that  can
quickly update  an  out-of-date  file  system  replica.  By  utilizing  General
Parallel File System (GPFS) policy scans, distsync finds changed  files  without
navigating  between  directories.  It  can then parallelize work across multiple
nodes, maximizing the performance of a GPFS. The National Energy Research
Scientific Computing Center (NERSC) is currently using distsync to replicate
file systems of over 100 million inodes and over four petabytes.
