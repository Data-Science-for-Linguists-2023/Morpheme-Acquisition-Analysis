# Progress report

## 1st Progress Report

### Accomplishments

The data import process so far is detailed in [this notebook](/notebooks/data_curation.ipynb).

 - **L2 Data**: I decided to utilize the [COREFL Corpus](http://corefl.learnercorpora.com/) rather than the PELIC, since it has spoken data transcripts available and I am more interested in analyzing speech for this project. The data was imported successfully and tidied into a dataframe with all the relevant information. However, the mean years of studying English is 12.75, which might be quite high for an analysis of early morpheme acquisition that is comparable to a child learning their L1. I may narrow the scope to participants who have been learning English for a smaller amount of time, or supplement with some additional learner data from another spoken and transcribed corpus that has a wider range of proficiency and L1s, though this has been challenging to find thus far. 

- **L1 Data**: I chose to work with the "[Frog Story](https://childes.talkbank.org/access/Frogs/English-Slobin.html)" data from the CHILDES corpus, which consists of recorded narratives of 12 different English speakers across different age levels. I installed the `PyLangAcq` library and was able to use it to succesfully parse through CHILDES `CHAT` format and create a dataframe with the information necessary for my analysis. The transcripts are already tokenized and marked for part-of-speech and specific morphemes, which is incredibly helpful. 

### Next Steps

- I would like to supplement the L2 Data with additional data from other corpora, since it is limited to two L1s (Spanish and German) which are quite similar to English, and the learners have been learning English for quite a long period of time. 

- The texts in the L2 data must be tokenized and tagged for part-of-speech and morphemes, so to parallel the `CHAT` style L1 data derived from the CHILDES corpus. This may prove challenging.

- Alternatively, rather than using adult language learner corpora for the L2 analysis, I could instead utilize data from the Bilingual speaker portion of CHILDES, focusing on children speaking in their L2 instead. This has the benefit of the data already being in `CHAT` format, tokenized and tagged. I am looking into both options at this time to figure out which would be more suitable and efficient. 

### Sharing Plan

At this point in time, I plan to share this project's code, data, and analysis in its entirety. The corpora I am utilizing are made freely available by their authors. They do not contain any type of sensitive or identifying information regarding its participants, and neither will the output of my work and analysis.

## Feb. 10, 2023

- Created project repository on GitHub

- [Project plan](/project_plan.md) written

- Datasets (tentatively) chosen

- Next steps: delve deeper into the data to understand what needs to be processed, how to reconcile and subset datasets, and what is and may not be possible in terms of the scope of my analysis.