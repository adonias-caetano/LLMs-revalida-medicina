#  Performance Comparison of Large Language Models on Brazil's Medical Revalidation Exam for Foreign-Trained Graduates

<p align="center">
This repository provides scripts and results from the study of Performance Comparison of Large Language Models on Brazil's Medical Revalidation Exam for Foreign-Trained Graduates.
</p>

<div align="justify">

 ## 📋 Requirements

* Google Colab
* Python Language
 * from google.colab import files
 * import numpy as np
 * import pandas as pd
 * import seaborn as sns
 * import matplotlib.pyplot as plt
 * import re
 * import random
 * import os
 * import asyncio
 * from unidecode import unidecode
 * from nltk.tokenize import word_tokenize, sent_tokenize
 * from nltk.corpus import stopwords
 * from wordcloud import WordCloud
 * from transformers import TrainingArguments, TextStreamer
 * from sklearn.model_selection import train_test_split
 * from imblearn.under_sampling import RandomUnderSampler
 * import faiss
 * import openai
 * from openai import AsyncOpenAI
 * from unsloth import FastLanguageModel
 * import torch
 * from trl import SFTTrainer
 * from unsloth import is_bfloat16_supported

* R Language
 * googledrive
 * readxl
 * dplyr

## 📖  Revalida

The **Revalida** (National Examination for the Revalidation of Medical Diplomas) is a Brazilian assessment designed to validate medical degrees obtained abroad. It is aimed at both foreign-trained doctors and Brazilian nationals who have studied medicine outside the country and wish to practise in Brazil. The exam ensures that candidates possess the necessary knowledge, skills, and competencies required for medical practice in Brazil.

The **Revalida** consists of two distinct phases:
1. **Written Examination** – This stage evaluates theoretical knowledge through multiple-choice and discursive questions.
2. **Clinical Skills Assessment** – Candidates must demonstrate practical medical competencies in simulated clinical scenarios.

To participate, applicants must meet specific requirements, including legal residency in Brazil and submission of authenticated academic documents. The exam is conducted twice a year and is now the **sole method** for revalidating foreign medical diplomas in Brazil.

Available exam repositories include assessments from **2017.01, 2017.02, 2020.01, 2020.02, 2021.01, 2022.01, 2022.02, 2023.01, 2023.02, and 2024.01**.

## 🛠 Fine-tuning BERT-based Models

We use two BERT-based models pre-trained in Brazilian Portuguese, namely, BERTimbau Base (BERT-Base) and BERTimbau Large (BERT-Large) from <a href="https://github.com/neuralmind-ai/portuguese-bert/"><strong>BERTimbau - Portuguese BERT</strong></a>.  The third model was the <a href="https://github.com/google-research/bert/blob/master/multilingual.md"><strong>BERT multilingual base</strong></a>. 

The AdamW optimizer was used to adjust parameters in the model, batch size of 16, configured with a learning rate equal to 2e-6 in seven training epochs. K-fold cross-validation was performed by dividing the pre-processed dataset into 80% for training and 20% for validation. 

## 🤖 Access our published paper

Published paper in the <a href="https://cadernos.ensp.fiocruz.br/ojs/index.php/csp"> <strong>Cadernos de Saúde Pública</strong></a>

### [Paper Link](https://www.scielo.br/j/csp/a/XrbVfvybPj9tvJ8qWv7j8VC/?lang=en) 

## 👏 Contributing
 
If there is a bug, or other improvement you would like to report or request, we encourage you to contribute.

Please, feel free to contact us for any questions: [![Gmail Badge](https://img.shields.io/badge/-ariel.teles@ifma.edu.br-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:ariel.teles@ifma.edu.br)](mailto:ariel.teles@ifma.edu.br )

## 📄 License

### <a href="https://doi.org/10.5281/zenodo.10070747"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.10070747.svg" alt="DOI"></a> 
### <a href="https://creativecommons.org/licenses/by/4.0/"><img src="https://licensebuttons.net/l/by/4.0//88x31.png" alt="DOI"></a> 

## 📚 References

* <a href="https://www.mdpi.com/2227-9032/10/4/698"><strong>Paper about Boamente System</strong></a>.
* <a href="https://www.sciencedirect.com/science/article/pii/S1877050922009668"><strong>Paper about XAI Boamente System</strong></a>.

