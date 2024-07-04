# Automatic Identification of Duplicate Questions in Indonesian Consumer Health Forums Using Learning-to-Rank

## Author

Febi Imanuela

## Abstract

The development of technology in the healthcare sector in Indonesia has introduced consultation services with doctors through consumer health forums. Over time, the issue of duplicate questions on these forums emerged. This problem needs to be addressed to accelerate the response process for similar questions and to keep the number of questions scalable with the capacity of the responding doctors. However, duplicate questions present their own challenge due to the complexity of natural language. This study utilizes Information Retrieval approach to identify pairs of duplicate questions in this domain as query and relevant document pairs. After initial ranking using BM25 as the baseline model, the ranking performance is improved through a re-ranking process using the feature-based LambdaMART model. This study leverages features that calculate the distance and similarity between vector representations of the query and document, obtained from word embedding and transformer models. Additionally, scoring features derived from the Cross Encoder model and the BM25 baseline model are proposed. The study also suggests features that consider the number of main idea keywords from the query that is also contained within the document. Experiment evaluation is conducted using cross validation and error analysis, with Mean Reciprocal Rank (MRR) as the primary metric. The highest performance achieved in the experiments is an MRR of 0.951 with a p-value of 0.016, which is significant to the baseline. Thus, this study provides empirical support for the effectiveness of the proposed re-ranking model for automatic identification of the query and relevant document, specifically duplicate question pairs in this context.

## Presentation Deck

https://bit.ly/PresentationMedicalL2R

## Repository Overview

- **[Febi]\_Index_and_Baseline.ipynb**  
  Experiment on data cleaning and indexing for BM25 baseline
- **[Febi]\_Precompute_Embedding.ipynb**  
  Precompute transformer-based embeddings (Sentence Transformer, T5 Encoder Model, and Pretrained IndoBERT)
- **[Febi]\_Rerank_and_Error_Analysis.ipynb**  
  Experiment on re-ranking using feature-based LambdaMART, followed by evaluation and error analysis framework
