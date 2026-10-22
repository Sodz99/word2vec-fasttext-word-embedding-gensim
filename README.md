# Word2Vec and FastText Word Embedding with Gensim in Python

The project aims to train the Skip-gram and FastText models for performing word embeddings and then building a search engine along with a Streamlit UI.

## Overview
The biggest challenge in the NLP (Natural Language Processing) domain is to extract the context from text data, and word embeddings are the solution that represents words as semantically meaningful dense vectors. They overcome many of the problems that other techniques like one-hot encodings and TFIDF have.

Embeddings boost generalization and performance for downstream NLP applications even with fewer data. So, word embedding is the feature learning technique where words or phrases from the vocabulary are mapped to vectors of real numbers capturing the contextual hierarchy.

General word embeddings might not perform well enough on all the domains. Hence, we need to build domain-specific embeddings to get better outcomes. In this project, we will create medical word embeddings using Word2vec and FastText in python.

## Data
We are considering a clinical trials dataset for our project based on Covid-19. The link for this dataset is as follows: Link:https://dimensions.figshare.com/articles/dataset/Dimensions_COVID- 19_publications_datasets_and_clinical_trials/11961063

There are 10666 rows and 21 columns present in the dataset. The following two columns are essential for us,  Title  Abstract

_Data is not included in this repository._

## Approach
1. Importing the required libraries
2. Reading the dataset
3. Pre-processing  Remove URLs  Convert text to lower case  Remove numerical values  Remove punctuation.  Perform tokenization  Remove stop words  Perform lemmatization  Remove ‘\n’ character from the columns
4. Exploratory Data Analysis (EDA)  Data Visualization using word cloud
5. Training the ‘Skip-gram’ model
6. Training the ‘FastText’ model
7. Model embeddings – Similarity
8. PCA plots for Skip-gram and FastText models
9. Convert abstract and title to vectors using the Skip-gram and FastText model
10. Use the Cosine similarity function
11. Perform input query pre-processing
12. Define a function to return top ‘n’ similar results
13. Result evaluation
14. Run the Streamlit Application

Modular code overview

Once you unzip the modular_code.zip file you can find the following folders within it.
1. input
2. src
3. output
4. lib
1. Input folder - It contains the data that we use for our analysis. A clinical trials dataset is considered for our project, which is based on Covid-19.  Dimension-covid.csv. There are 10666 rows and 21 columns present in the dataset.
2. Src folder - This is the most important folder of the project. This folder contains all the modularized code for all the above steps in a modularized manner. This folder consists of:  engine.py

   ML_pipeline The ML_pipeline is a folder that contains all the functions put into different python files, which are appropriately named. These python functions are then called inside the engine.py file.

3. Output folder – The output folder contains the best fitted model that we trained for this data. This model can be easily loaded and used for future use and the user need not have to train all the models from the beginning.

Note: This model is built over a chunk of data. One can obtain the model for the entire data by running engine.py by taking the quality data to train the models.

4. Lib folder - This is a reference folder. It contains,  The original ipython notebook that we saw in the videos.  The Medical.py notebook which will be used for running our Streamlit UI  The ppt used in the videos is also present in this folder.

## Tech stack
 Language - Python  Libraries and Packages - pandas, numpy, matplotlib, plotly, gensim, streamlit, nltk.

Environment – Jupyter Notebook

## How to run
```bash
pip install -r Ipython Notebook/requirements.txt
python Modular Code/Medical_Embeddings/src/engine.py
```
Notebooks: [`Medical Embeddings_Final.ipynb`](Ipython%20Notebook/Medical%20Embeddings_Final.ipynb), [`Medical Embeddings_Final.ipynb`](Modular%20Code/Medical_Embeddings/lib/Medical%20Embeddings_Final.ipynb)

## Project structure
```
.gitignore
Ipython Notebook/
  Medical Embeddings_Final.ipynb
  requirements.txt
Modular Code/
  Medical_Embeddings/
    lib/
    requirements.txt
    src/
README.md
```

## Credits
Based on a ProjectPro guided project.
