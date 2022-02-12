# EvidenceBasedQuery
## Our approach
We generated an evidence-based query for the query-focused summarization (QFS) task in this experiment. Here, we showed that evidence (common words between document and summary) could be used as a query for the QFS task. First, we fine-tuned the T5 model with CNN/DM data set for the evidence generation task to avoid target leakage. Then, using this evidence model, we generated evidence-based queries and performed the QFS task on the Debatepedia data set.

A. For the evidence keywords, we first extracted evidence keywords from news articles and their corresponding highlights of the CNN/DM data set.

B. Then, we fine-tuned the T5 model with news articles and evidence keywords of the CNN/DM data set. This trained Evidence Model can predict evidence keywords for a given document.

C. Using this Evidence Model, we generated evidence-based queries for the Debatepedia data set.

D. Finally, we fine-tuned several models (Pegasus, BART, RoBERTa and LED) for the QFS task on the Debatepedia data set. We used the rank-based method, where we ranked the sentences of the documents according to the evidence-based queries. For the comparison, we used two types of queries for QFS tasks: 
1. queries came with Debatepedia data set, and 
2. our generated evidence as queries.
## About files
1. EvidenceExtraction.ipynb: To perform task A.
2. EvidenceModel.ipynb: To perform task B.
3. EvidenceGeneration.ipynb: To perform task C. Using this script, we generated and incorporated evidence-based queries in the debatepedia data set (debatepediaEvidence_train.json, debatepediaEvidence_valid.json and debatepediaEvidence_test.json).
4. Fine_Tune_Pegasus.ipynb: To perform task D. 
5. Fine_Tune_BART.ipynb: To perform task D.
6. Fine_Tune_RoBERTa.ipynb: To perform task D.
7. Fine_Tune_LED.ipynb: To perform task D.
