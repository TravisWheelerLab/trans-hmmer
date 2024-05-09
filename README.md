## PILOT IMPLEMENTATION of Translated (protein-to-DNA) search in a HMMER fork

**IF YOU ARE LOOKING FOR OUR TRANSLATED SEARCH SOFTWARE, PLEASE VISIT THE BATH REPOSITORY: [https://github.com/TravisWheelerLab/BATH](https://github.com/TravisWheelerLab/BATH)**

---------

__DEPRECATED DESCRIPTION BELOW__

**WARNING:  This is a fork of the [HMMER repository](https://github.com/EddyRivasLab/hmmer), and should not be treated as the original.**

[HMMER](http://hmmer.org) searches biological sequence databases for
homologous sequences, using either single sequences or multiple
sequence alignments as queries. HMMER implements a technology called
"profile hidden Markov models" (profile HMMs). 

This fork includes a new tool, hmmsearcht, for performing so-called
"translated search", directly comparing a file of protein profile HMMs 
to a target set of one or more nucleotide sequences. Other standard
HMMER tools are not compiled, to avoid clashing with a standard 
hHMMER installation. 


The approach is functionally equivalent to identifying all open reading frames
(ORFs) in the target sequence, then searching them with hmmsearch.
These two new tools contribution (hmmsearcht) provides a few benefits; most importantly:
- it simplifies the process of parsing results to recover hit positions
- it presents alignments showing both amino acid and encoding codons


### to clone a copy of this fork of HMMER3 source from github:

```bash
   % git clone https://github.com/TravisWheelerLab/trans-hmmer 
   % cd hmmer
   % git submodule init
   % git submodule update --remote
   % autoconf
   % ./configure
   % make
```

You will find the executables `hmmsearcht` and `hmmscant` in the 
`src/` directory, along with a copy of `hmmbuild`.


### to report a problem:

Visit the main HMMER repo
[issues tracking page at github](https://github.com/TravisWheelerLab/hmmer/issues).

