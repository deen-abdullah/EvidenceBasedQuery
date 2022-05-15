In this experiment we used [QuerySum](https://github.com/yumoxu/querysum) model (Xu and Lapata, 2020), and [TD-QFS](https://drive.google.com/file/d/1X1rKKP5SrUoU9-ki0urrlhO_L35Vl2oO/view?usp=sharing) data set. Instead of using the query from the data set, we used our generated query and performed the QFS using QuerySum model. We wanted to investigate the performance of the existing SOTA QFS model with our evidence-based queries.

QuerySum model is available [here](https://github.com/yumoxu/querysum).

Use 'EvidenceGenerationFor_tdqfs.ipynb' file to generate the query for TD-QFS data set. We used the same documents as the author used for generating their queries. Then replace them on 'data/tdqfs/query_info.txt'. Finally, follow the steps on QuerySum model to get the results.
