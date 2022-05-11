In this experiment we used [querysum](https://github.com/yumoxu/querysum) model, and [DUC 2006 and 2007](https://www-nlpir.nist.gov/projects/duc/data.html) data sets. Instead of using the query from the data sets, we used our generated query and performed the QFS using querysum model.

querysum model is available [here](https://github.com/yumoxu/querysum). Since we are not allowed to distribute DUC data, you can request DUC 2006-2007 from [NIST](https://www-nlpir.nist.gov/projects/duc/data.html).

Use our 'EvidenceGeneration.ipynb' file to generate the query for DUC data sets. Then replace them on 'data/topics'. Finally, follow the steps on querysum model to get the results.
