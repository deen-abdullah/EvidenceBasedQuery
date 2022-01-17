# EvidenceBasedQuery
## Our approach
In this project, we experimented on evidence based query for the query focused summarization (QFS) task.
Here, we showed that evidence (common words between document and summary) can be used as query for QFS task.

A. For the evidence keywords, we first extracted evidence from news articles and their corresponding highlights of CNN/DM data set.

B. Then we fine tuned T5 model with news articles and evidences of CNN/DM data set. This trained Evidence Model can predict evidence for a given document.

C. Using this Evidence Model, we generated evidences for the Debatepedia data set.

D. Finally, we fine tuned several models (Pegasus, BART, ... ) for QFS task. We used rank based method where we ranked the sentences of the documents according to the query. For the comparison, we used two types of queries for QFS tasks: 
1. query came with debatepedia data set, and 
2. our generated evidence as query.
## About files
1. EvidenceExtraction.ipynb: To perform task A.
2. EvidenceModel.ipynb: To perform task B.
3. EvidenceGeneration.ipynb: To perform task C. Using this script, we generated and incorporated evidences on the debatepedia data set (debatepediaEvidence_train.json, debatepediaEvidence_valid.json and debatepediaEvidence_test.json).
4. Fine_Tune_Pegasus.ipynb: To perform task D. 
