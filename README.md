# EvidenceBasedQuery
## Our approach
In this experiment, we generated evidence-based query for the query focused summarization (QFS) task.
Here, we showed that evidence (common words between document and summary) can be used as query for QFS task. 
To avoid target leakage, we fine tuned T5 model with CNN/DM data set for evidence generation task. Then, using this evidence model, we generated evedence-based queries and performed QFS task on Debatepedia data set.

A. For the evidence keywords, we first extracted evidence keywords from news articles and their corresponding highlights of CNN/DM data set.

B. Then we fine tuned T5 model with news articles and evidences of CNN/DM data set. This trained Evidence Model can predict evidence for a given document.

C. Using this Evidence Model, we generated evidence-based queries for the Debatepedia data set.

D. Finally, we fine tuned several models (Pegasus, BART, RoBERTa and LED) for QFS task on Debatepedia data set. We used rank-based method where we ranked the sentences of the documents according to the evidence-based queries. For the comparison, we used two types of queries for QFS tasks: 
1. queries came with debatepedia data set, and 
2. our generated evidence as queries.
## About files
1. EvidenceExtraction.ipynb: To perform task A.
2. EvidenceModel.ipynb: To perform task B.
3. EvidenceGeneration.ipynb: To perform task C. Using this script, we generated and incorporated evidence-based queries in the debatepedia data set (debatepediaEvidence_train.json, debatepediaEvidence_valid.json and debatepediaEvidence_test.json).
4. Fine_Tune_Pegasus.ipynb: To perform task D. 
5. Fine_Tune_BART.ipynb: To perform task D.
6. Fine_Tune_RoBERTa.ipynb: To perform task D.
7. Fine_Tune_LED.ipynb: To perform task D.
