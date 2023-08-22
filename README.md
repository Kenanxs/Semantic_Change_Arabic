# Arabic Semantic Change Analysis using Unsupervised Techniques

This project explores semantic change in the Arabic language through a computational approach, filling a gap in linguistic research. Semantic change, the phenomenon of words changing meanings over time, is a critical aspect of language evolution. While extensively studied in various languages, Arabic has remained unexplored in this context.

**Motivation:** Despite Arabic's historical significance and wide usage, little attention has been given to its semantic evolution. This project aims to shed light on this aspect, providing insights into the cultural and historical evolution of the Arab world. Furthermore, understanding semantic change in Arabic can enhance NLP models and sentiment analysis tools.

**Approach:** Leveraging pretrained BERT models tailored for Arabic, we employ an unsupervised technique to analyze semantic change. By comparing word embeddings across different time spans, we identify words that have remained stable or undergone changes in meaning.

**Contributions:** This study introduces a unique approach to studying Arabic semantic change and offers a candidate word set for evaluating models in this field. While not a complete evaluation set, this seed dataset can guide future efforts in semantic change research.

## Table of Contents
- [Part 1: Downloading and Unzipping](#part-1-downloading-and-unzipping)
- [Part 2: Preprocessing using AraBERTv2](#part-2-preprocessing-using-arabertv2)
- [Part 3: Target Words and Occurrences](#part-3-target-words-and-occurrences)
- [Part 4: Project Pipeline](#part-4-project-pipeline)
- [SCWS Dataset Evaluation Task](#scws-dataset-evaluation-task)
- [Part 5: Arabertv2 Base Model](#part-5-arabertv2-base-model)
- [Part 6: CamelBERT MSA Model](#part-6-camelbert-msa-model)
- [Part 7: CamelBERT CA Model](#part-7-camelbert-ca-model)
- [Part 8: Results](#part-8-results)
- [Data Files and Results](#data-files-and-results)

## Part 1: Downloading and Unzipping
This Colab notebook guides you through the process of downloading and unzipping the OpenITI corpus. It also splits the data into two time periods, crucial for the semantic change study. The notebook includes links to the reliable Zenodo 2023 version of the data, ensuring code reproducibility.

## Part 2: Preprocessing using AraBERTv2
In this Colab notebook, the preprocessing function from AraBERTv2 is applied to the corpora. This function cleans the data by removing HTML markup, URLs, and emails, among other things, making it ready for further analysis.

## Part 3: Target Words and Occurrences
This Colab notebook focuses on extracting target words from the corpora based on their frequency distribution. It also identifies the occurrences of these target words in both time periods, providing essential context for the analysis.

## Part 4: Project Pipeline
This Colab notebook serves as an illustrative pipeline using a simplified dataset of two sentences (C1 and C2). It walks through the entire methodology, offering a clear understanding of how the code works in practice.

## SCWS Dataset Evaluation Task
This Colab notebook employs the SCWS evaluation dataset to validate the methodology demonstrated in the pipeline. It achieves a robust Spearman correlation result between the method's outcomes and benchmark gold labels.

## Part 5: AraBERTv2 Base Model
Using C1 and C2 data along with target words from Part 3, this Colab notebook applies the code to the AraBERTv2 base model. It calculates cosine similarity scores between embeddings extracted from the two time periods.

## Part 6: CAMeLBERT MSA Model
Similarly, this Colab notebook applies the code to the CAMeLBERT MSA model. It computes cosine similarity scores between embeddings of C1 and C2, using target words as the focus.

## Part 7: CAMeLBERT CA Model
Similarly, this Colab notebook applies the code to the CAMeLBERT CA model. It computes cosine similarity scores between embeddings of C1 and C2, using target words as the focus.

## Part 8: Results
Using the cosine similarity scores from Parts 5, 6, and 7, this Colab notebook conducts in-depth analysis and visualizations. The results provide valuable insights into the semantic change patterns over time.

## Data Files and Results
This section explains the purpose and format of the provided data files and results. These files provide easy access to each part of the repository. It offers the data needed to directly access any notebook without running the preceding ones. You'll find the output files from each notebook, allowing you to jump between notebooks without the necessity to execute the entire sequence. 




