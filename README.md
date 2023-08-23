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
- [Part 1: Downloading + Unzipping Data](Part_1_download_+_unzip.ipynb)

## Part 2: Preprocessing using AraBERTv2
In this Colab notebook, the preprocessing function from AraBERTv2 is applied to the corpora. This function cleans the data by removing HTML markup, URLs, and emails, among other things, making it ready for further analysis.
- [Part 2: Preprocessing using AraBERT](Part_2_Preprocessing_using_AraBERTv2.ipynb)

## Part 3: Target Words and Occurrences
This Colab notebook focuses on extracting target words from the corpora based on their frequency distribution. It also identifies the occurrences of these target words in both time periods, providing essential context for the analysis.
- [Part3: Target Words and Occurrences](Part_3_Target_Words_+_Occurrences.ipynb)
  
## Part 4: Project Pipeline
This Colab notebook serves as an illustrative pipeline using a simplified dataset of two sentences (C1 and C2). It walks through the entire methodology, offering a clear understanding of how the code works in practice. This pipeline can be executed as a standalone notebook. 
- [Part 4: Project Example Pipeline](Part_4_Project_Pipeline.ipynb)

## SCWS Dataset Evaluation Task
This Colab notebook employs the SCWS evaluation dataset to validate the methodology demonstrated in the pipeline. It achieves a robust Spearman correlation result between the method's outcomes and benchmark gold labels. This evalaution task can be executed as a standalone notebook. It requires the SCWS dataset included in the **Data Files and Results** section. 
- [Evaluation Task](SCWS_dataset_evaluation_task.ipynb)

## Part 5: AraBERTv2 Base Model
Using C1 and C2 data along with target words from Part 3, this Colab notebook applies the code to the AraBERTv2 base model. It calculates cosine similarity scores between embeddings extracted from the two time periods.
- [Part 5: AraBERTv2 Base Model](Part_5_Arabertv2_Base.ipynb)

## Part 6: CAMeLBERT MSA Model
Similarly, this Colab notebook applies the code to the CAMeLBERT MSA model. It computes cosine similarity scores between embeddings of C1 and C2, using target words as the focus.
- [Part 6: CAMeLBERT MSA Model](Part_6_CAMeLBERT_MSA.ipynb)

## Part 7: CAMeLBERT CA Model
Similarly, this Colab notebook applies the code to the CAMeLBERT CA model. It computes cosine similarity scores between embeddings of C1 and C2, using target words as the focus.
- [Part 7: CAMeLBERT CA Model](Part_7_CAMeLBERT_CA.ipynb)

## Part 8: Results
Using the cosine similarity scores from Parts 5, 6, and 7, this Colab notebook conducts in-depth analysis and visualizations. The results provide valuable insights into the semantic change patterns over time.
- [Part 8: Results](Part_8_Results.ipynb)

## Data Files and Results
This section explains the purpose and format of the provided data files and results. These files provide easy access to each part of the repository. It offers the data needed to directly access any notebook without running the preceding ones. You'll find the output files from each notebook, allowing you to jump between notebooks without the necessity to execute the entire sequence. 
- [Part 3 Output: Target Words](target_words.pkl)
- [Part 3 Output: Occurrences] : Files are too large to upload here. Google Drive link to corpus text files: https://drive.google.com/drive/folders/1uHJHDLbZr0_UhFIqiSAJ1xXlyGqqbUtH?usp=sharing

The part 3 output files (target words and occurrences) can be used in the subsequent notebooks (Part 5 onwards). 

- [Part 5 Output: AraBERT cosine](cosine_Arabertb.csv)
- [Part 6 Output: CAMeLBERT MSA cosine](cosine_MSA.csv)
- [Part 7 Output: CAMeLBERT CA cosine](cosine_CA.csv)
- [All Results Combined (Parts 5,6 and 7)](Results.pkl)

The outputs from all models (i.e. parts 5,6 and 7) can be used in the results notebook. 

-[SCWS Dataset for Evaluation](ratings.txt)

This is the SCWS ratings dataset used for the evaluation task. 

## Acknowledgments
1. AraBERT Model
@inproceedings{antoun2020arabert,
  title={AraBERT: Transformer-based Model for Arabic Language Understanding},
  author={Antoun, Wissam and Baly, Fady and Hajj, Hazem},
  booktitle={LREC 2020 Workshop Language Resources and Evaluation Conference 11--16 May 2020},
  pages={9}
}
2. CAMeLBERT Models
@inproceedings{inoue-etal-2021-interplay,
    title = "The Interplay of Variant, Size, and Task Type in {A}rabic Pre-trained Language Models",
    author = "Inoue, Go  and
      Alhafni, Bashar  and
      Baimukan, Nurpeiis  and
      Bouamor, Houda  and
      Habash, Nizar",
    booktitle = "Proceedings of the Sixth Arabic Natural Language Processing Workshop",
    month = apr,
    year = "2021",
    address = "Kyiv, Ukraine (Online)",
    publisher = "Association for Computational Linguistics"
}
3. OpenITI Corpus
Nigst, Lorenz, Romanov, Maxim, Savant, Sarah Bowen, Seydi, Masoumeh, & Verkinderen, Peter. (2023). OpenITI: a Machine-Readable Corpus of Islamicate Texts (2022.2.7) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.7687795
