# DGA Training Dataset

## Reason for releasing the dataset
Based on our experience, and that of others (see [Valuing Cybersecurity Research Datasets](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3469364)) cybersecurity research 
and the associated datasets are incredibly valuable and difficult to come by. Research in both academia and the 
private sector is critical to short and long term effectiveness of cybersecurity techniques and products. 
Publishing both research and the data used allows researchers from around the world to independently validate such 
research and determine the effectiveness of new techniques. We also feel strongly that sharing our research and data 
is both helpful to the community at large and encourages others to do the same. See our [blog](https://www.extrahop.com/company/blog/tech/) 
for additional information.

## Intended Use Of The Dataset

The dataset is intended to be used for research into the area DGA ([Domain Generation Algorithm](https://en.wikipedia.org/wiki/Domain_generation_algorithm)) 
detection, but has other applications as well. Being able to quickly and accurately identify a DGA is one of the keys to 
neutralizing the C&C (Command and Control) network of a Botnet. We use it for model design, training, validating our models.

## Dataset Description

  * The dataset contains 16,246,014 rows of data in a single file, it is compressed using gzip and its name is: dga-training-data-encoded-v3.json.gz
  * Each row of the dataset is JSON encoded and contains two pieces of information.
    - domain: is a string that represents a domain name, doesn't contain any TDL (Top Level Domain) or CC (Country Code) data.
    - threat: is either 'benign' or 'dga'
      - benign, means that it is not a dga
      - dga, means that it is a dga
  * All data in this dataset was passively harvested or synthesized from known dga algorithms.
  * The dataset is balanced roughly 50/50
  * Below is a sample of the data.
<pre>
      {"domain": "lespedi", "threat": "benign"}
      {"domain": "qgcyquqgygcsaausi", "threat": "dga"}
      {"domain": "segaluckykuji", "threat": "benign"}
      {"domain": "wqbnamentalistfanchonut", "threat": "dga"}
      {"domain": "jdqmyepcif", "threat": "dga"}
      {"domain": "qapqjdvaaxysbefd", "threat": "dga"}
      {"domain": "mattgolder", "threat": "benign"}
      {"domain": "skigimasaaccsgsuimuwmissuqa", "threat": "dga"}
      {"domain": "thegrimaldisaredead", "threat": "benign"}
      {"domain": "oxfordlanguagedictionaries", "threat": "benign"}
</pre>
