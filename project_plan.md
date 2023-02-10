# Project Plan

## Morpheme Order Acquisition Analysis

### Summary

This project seeks to analyze morpheme acquisition order. Many 'natural order' studies proclaim that there is be a consistent order in which first and/or second language learners acquire proficiency in the use of grammatical morphemes. I would like to analyze large-scale, longitudinal learner corpora to determine this sequence and whether it actually aligns with previously proposed acquisition orders. Ideally, this project will compare and contrast a corpus of L1 or native-speaker production and a corpus of L2 or language learner production to see if and how the proposed 'natural morpheme acquisition order' manifests in L2 acquisition.

### Data

- [CHILDES](https://childes.talkbank.org/) offers a wide variety of spoken language from children that may be utilized for this project. This data has its own annotation and analysis format, the CHAT format, so significant time and wrangling will be dedicated to parsing these data files. 

- [WordBank](http://wordbank.stanford.edu/) is an open database of children's vocabulary development that could potentially supplement analysis of particular morphemes. 

- [PELIC](https://eli-data-mining-group.github.io/Pitt-ELI-Corpus/) is a large learner corpus of written and spoken texts. 


### Analysis

The end goal of this project is to analyze whether or not the data in the corpora are aligned with proposed morpheme acquisition orders, which could have implications for L2 learning and teaching. My hypothesis is that the acquisiton order may differ between L1 speakers and L2 learners due to the influence of factors such as language instruction and L1 transfer. My aim is to provide an in-depth exploration and statistical analysis regarding these potential differences. My plan for how the analysis will proceed is as follows:

1. Exploratory data analysis & summary statistics
2. Selection of particularly salient morphemes
3. Sampling and integration of data from corpora into new dataframe(s)
4. Further linguistic analysis

- Potentially helpful tools and things:
     - [MOR](https://talkbank.org/morgrams): part-of-speech tagging for CHAT (CHILDES format) data
    - [NLTK CHILDES documentation](https://www.nltk.org/howto/childes.html)
    - [PyLangAcq](https://pylangacq.org/): Python library for language acquisition research
    - [PELIC tutorials](https://github.com/ELI-Data-Mining-Group/PELIC-dataset/tree/master/tutorials)
