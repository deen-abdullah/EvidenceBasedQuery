# Project
## Our approach
In this experiment, we developed an evidence-based model to generate evidence-based queries for the query-focused summarization (QFS) task. Here, we showed that evidence (common words between document and summary) could be used as a query for the QFS task. We used a transfer learning approach to avoid target leakage. First, we fine-tuned the T5 model with CNN/DM data set for the evidence generation task. Then, using this evidence-based model, we generated evidence-based queries and performed the QFS task on the Debatepedia and TD-QFS data sets.

A. For the evidence keywords, we first extracted evidence keywords from news articles and their corresponding highlights of the CNN/DM data set.

B. Then, we fine-tuned the T5 model with news articles and evidence keywords of the CNN/DM data set. This trained Evidence-based model can predict evidence keywords for a given document.

C. Using this Evidence-based model, we generated evidence-based queries for the Debatepedia and TD-QFS data sets.

D. Finally, we fine-tuned several models (Pegasus, BART, RoBERTa and LED) for the QFS task on the Debatepedia data set. We used the rank-based method, where we ranked the sentences of the documents according to the evidence-based queries.

E. Additionally, we perform another experiment using QuerySum (Xu and Lapata, 2020), a state-of-the-art QFS model to compare the results of the original queries and the evidence-based queries of the TD-QFS data set.

 For the comparison, we used two types of queries for the QFS tasks:
1. queries came with data sets (original), and
2. our generated evidences as evidence-based queries.
## About files
1. EvidenceExtraction.ipynb: To perform task A.
2. EvidenceModel.ipynb: To perform task B.
3. EvidenceGeneration.ipynb: To perform task C. Using this script, we generated and incorporated evidence-based queries in the debatepedia data set (debatepediaEvidence_train.json, debatepediaEvidence_valid.json and debatepediaEvidence_test.json).
4. Fine_Tune_Pegasus.ipynb: To perform task D.
5. Fine_Tune_BART.ipynb: To perform task D.
6. Fine_Tune_RoBERTa.ipynb: To perform task D.
7. Fine_Tune_LED.ipynb: To perform task D.
8. querysum\EvidenceGenerationFor_tdqfs.ipynb: To perform task E.
