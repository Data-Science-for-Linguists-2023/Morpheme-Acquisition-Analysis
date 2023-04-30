Final report
================
by Sen Sub Laban

## Contents
> <a href="#introduction" id="toc-introduction">Introduction</a>
> 
> <a href="#data-language-of-conspiracy-loco-corpus"
>    id="toc-data-language-of-conspiracy-loco-corpus">Data</a>
>
> <a href="#analysis" id="toc-analysis">Analysis</a>
>
> <a href="#process-reflection" id="toc-process-reflection">Process
>   reflection</a>
>
> <a href="#references-and-further-reading"
    id="toc-references-and-further-reading">References and further
    reading</a>

## Introduction

 This project was conducted as an analysis of morpheme acquisition order. Many 'natural order' studies proclaim that there is a consistent order in which language learners acquire proficiency in the use of grammatical morphemes. To understand this, it is important to make the distinction between lexical and grammatical morphemes. In the word *played*, there is a lexical morepheme (*play*) and a grammatical morpheme (*-ed*). The field of natural order studies, and this project, is primarily concerned with the latter type, which are also known as functors. The terms functor and morpheme are used interchangeably in this project. 
 
 Natural order studies originated in the 1970's when researchers were looking into the "independent grammars assumption," that is, the perspective that when children acquire their first language, they begin as speakers of their own personal languages rather than as defective speakers of the adult version of the language. The first of many studies of this kind was Brown's (1973) longitudinal study of three native American-English speaking children. Brown observed that children learn English morphemes in the same order, though not at the same age. The work of Brown (1973) and other first language researchers was extended to second language acquisition to demonstrate that SLA is not just a matter of learned responses but that competence is actually developed according to a predictable series of benchmarks. Various studies in SLA supported researchers' expectations that the order of morpheme acquisition is largely consistent across language learners, and also revealed that children and adult learners acquire morphemes in the same general order. Such studies have been largely influential in the field until the present day.

 Curious to see if proposed 'natural orders' of morpheme acquisition could be analyzed through corpora, I formulated this project. My questions are as follows: (1) Does the sequence of morpheme acquisition in the data align with previously proposed acquisition orders? and (2) How does acquisition potentially differ between first langauge (L1) and second langauge (L2) corpora? 

## Data
The data utilized in this project was mostly sourced from [TalkBank](https://talkbank.org/). TalkBank is a multilingual database focused on research in the study of human communication. It provides repositories in 14 research areas, including child langauge acquisition ([CHILDES](https://childes.talkbank.org/)) and second language acquisition ([SLABank](https://slabank.talkbank.org/)). I used corpora from these two collections in order to conduct my analysis. The L1 data I selected was Berman & Slobin's (1994) [Frog Story corpus](https://childes.talkbank.org/access/Frogs/English-Slobin.html), which consists of recorded narratives of 12 different native English speakers telling a wordless "frog story" from a picture book. Each speaker was recorded at several different age levels (3, 4, 5, 9, and 20), making it suitable for looking into morpheme usage over time. The L2 corpus is the Vercelloti corpus from SLABank, which consists of reocrdings from learners witha variety of L1's and varying levels of English proficiency. 

The transcripts in TalkBank databases are stored in a dedicated format known as CHAT. A Python library, [PyLangAcq](https://pylangacq.org/), was used to import and parse the CHAT data files. The structure of the CHAT data and process of importing said data can be seen [here](https://nbviewer.org/github/Data-Science-for-Linguists-2023/Morpheme-Acquisition-Analysis/blob/main/notebooks/data_curation.ipynb#importing-native-corpus). Utilizing PyLangAcq to extract the data that I needed from the CHAT files, I created two separate dataframes, one for native English speakers and another for English langauge learners, which are stored in [this folder](../data_samples). The CHAT files provided tokens as well as annotations for morphemes and part-of-speech (POS), which I extracted and added to respective columns. 

A major roadblock in the process of acquiring my data was that the Vercelloti corpus CHAT files did not contain crucial learner metadata, such as the years spent learning English, that was necessary for my analysis. I was able to resolve this because Vercelloti's corpus is actually sourced from [PELIC](https://eli-data-mining-group.github.io/Pitt-ELI-Corpus/). I was able to successfully [create a csv file](https://nbviewer.org/github/Data-Science-for-Linguists-2023/Morpheme-Acquisition-Analysis/blob/main/notebooks/data_curation_cont.ipynb#augmenting-the-l2-metadata) that maps the Vercelloti corpus participant ids to the PELIC anonymized ids and used it to import the necessary information about the subjects into my larger dataframe. 

## Analysis
Once all the data was in order, I began my analysis. Researchers typically measure morpheme acquisition order by suppliance in obligatory context (SOC). To quote Brown (1973): 
>*Grammatical morphemes are obligatory in certain contexts, and so one can set an acquisition criterion not simply in terms of output, but in terms of output-where-required. Each obligatory context can be regarded as a kind of test item which the child passes by supplying the required morpheme or fails by supplying none or one that is not correct. This performance measure, the percentage of morphemes supplied in obligatory contexts, should not be dependent on the topic of conversation or the character of the interaction.*

The complexity of creating a model to actually measure SOC using Python would be beyond the scope of this project (at least with my current coding abilities), so I went about analysis in another way: by comparing the normalized frequencies of selected morphemes at each age or stage of acquisiton across the corpora. Functions to compile and count the occurence of 11 functors, selected from those investigated by Brown (1973) were run across both dataframes. The morpheme counts were normalized by dividing the counts by text length. Then, I calculated the means of the counts for each morpheme and level and stored that data in two new dataframes, which can be found in [data_samples](../data_samples). At first glance, it was challenging to parse the dataframes and extract meaningful patterns, so I generated the visualizations below. 

![Learner corpus](../data_samples/visuals/Lcorp_linegraph.png)

![Native corpus](../data_samples/visuals/Ncorp_linegraph.png)




## Conclusion

Potential avenues for further analysis include COCA, which I didn't get around to. 

## Process reflection

## References and further reading

Brown, R. (1973). A first language. Cambridge, MA: Harvard University Press.

Jeong, D. B. (2002). Second language acquisition in childhood. Seoul, Korea: Kyungjin Publishing Co. 

Juffs, A., Han, N-R., & Naismith, B. (2020). The University of Pittsburgh English Language Corpus (PELIC) [Data set]. http://doi.org/10.5281/zenodo.3991977

Krashen, S. D. (1985). The Input Hypothesis: Issues and implications. New York: Longman.

Lee, Jackson L., Ross Burkholder, Gallagher B. Flinn, and Emily R. Coppess. 2016. Working with CHAT transcripts in Python. Technical report TR-2016-02, Department of Computer Science, University of Chicago.

MacWhinney, B. (2000). The CHILDES Project: Tools for Analyzing Talk. 3rd Edition.  Mahwah, NJ: Lawrence Erlbaum Associates.

R. A. Berman & D. I. Slobin (1994). Relating events in narrative: A crosslinguistic developmental study. Hillsdale, NJ: Lawrence Erlbaum Associates.

Vercellotti, M. L. (2017). The development of complexity, accuracy, and fluency in second language performance: A longitudinal study. Applied Linguistics, 38(1), 90-111.
