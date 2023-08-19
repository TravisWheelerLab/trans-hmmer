## Translated (protein-to-DNA) search with hmmsearcht a HMMER fork 

*** Warning:  This is not the primary repository of HMMER. Please find the official repo at: https://github.com/EddyRivasLab/hmmer ***

[![](https://travis-ci.org/EddyRivasLab/hmmer.svg?branch=develop)](https://travis-ci.org/EddyRivasLab/hmmer)
![](http://img.shields.io/badge/license-BSD-brightgreen.svg)

[HMMER](http://hmmer.org) searches biological sequence databases for
homologous sequences, using either single sequences or multiple
sequence alignments as queries. HMMER implements a technology called
"profile hidden Markov models" (profile HMMs). 

This fork includes an additional tool, hmmsearcht, that directly 
compares a file of protein profile HMMs to a target set of one or more
nucleotide sequences. This is called translated search. The approach 
here is functionally equivalent to identifying all open reading frames
(ORFs) in the target sequence, then searching them with hmmsearch.
Our contribution (hmmsearcht) provides a few benefits; most importantly:
- it simplifies the process of parsing results to recover hit positions
- it presents alignments showing both amino acid and encoding codons


### to clone a copy of this fork of HMMER3 source from github:

The tarball way, above, is a better way to install HMMER (it includes
a precompiled Userguide.pdf, for example), but you can also clone our
github repo. You need to clone both the HMMER and Easel repositories,
as follows:


```bash
   % git clone https://github.com/TravisWheelerLab/hmmer 
   % cd hmmer
   % git checkout develop
   % git clone https://github.com/TravisWheelerLab/easel
   % (cd easel; git checkout develop)
   % autoconf
```

and to build:

```bash
   % ./configure
   % make
```


### to report a problem:

Visit the main HMMER repo
[issues tracking page at github](https://github.com/TravisWheelerLab/hmmer/issues).

