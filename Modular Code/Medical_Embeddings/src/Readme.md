## NLP Project: Word Embeddings with Word2Vec & FastText

Natural Language Processing (NLP) has progressed significantly with the introduction of word embeddings, which convert text into meaningful numeric vector representations. Traditional methods like One-Hot Encoding or TF-IDF often fail to capture semantic meaning, but modern embeddings learn contextual relationships directly from large text corpora.

In this project, you will learn to build domain-specific medical word embeddings using Gensim’s Word2Vec and FastText models, and use them to create a search engine with a Streamlit UI.

### Word Embeddings Overview

Word embeddings are dense vector representations that capture the contextual meaning of words. They improve NLP model generalization, handle vocabulary variations, and perform extremely well even on smaller datasets.

Two popular embedding techniques covered in this project are:

-Word2Vec
-Word2Vec consists of two architectures:
-CBOW (Continuous Bag of Words)
-Skip-Gram

The Skip-Gram model predicts the context of a given word and is especially effective for rare-word representations.

#### FastText

Developed by Facebook AI, FastText improves word embeddings by treating each word as a collection of character n-grams.
This helps:

- Capture subword information
- Handle misspellings
- Improve accuracy on domain-specific vocabularies

### Business Objective

In medical and clinical research, vocabulary evolves fast, and general-purpose embeddings may not capture domain-specific terminology.
This project aims to build medical word embeddings using Word2Vec and FastText trained on clinical trial text data, enabling more accurate semantic search and retrieval.

The final output is a search engine that:

- Takes a user query
- Performs preprocessing
- Converts it into vectors
- Computes cosine similarity
- Returns top ‘n’ most relevant clinical abstracts
- Displays everything using a Streamlit UI

### Dataset Description

We use a clinical trials dataset related to COVID-19:

Dataset Link:
https://dimensions.figshare.com/articles/dataset/Dimensions_COVID-19_publications_datasets_and_clinical_trials/11961063


## Steps to Run

There are two ways to execute the end to end flow.

- Modular Code (Medical.py)
- IPython

### Modular code

- Create virtualenv

### Code Implementation

The Python 3.9 version is supported for the execution of this project.
1. Running the codes locally: Python 3.9
    - Create a virtual environment: In the terminal or command prompt, use the following command to create a new virtual environment:

        - For Windows:
            `py -3.9 -m venv env`

        - For macOS and Linux:
            `python3 -m venv venv`
        This command creates a new virtual environment named "venv" in the current directory.

    - Activate the virtual environment:

        - For Windows (Command Prompt):
            `venv\Scripts\activate`


        - For macOS and Linux (Terminal) :
            `source venv/bin/activate`
    
    Once the virtual environment is activated, you should see the environment name (e.g., (venv)) in the terminal or command prompt.

    - Install project requirements: With the virtual environment active, you can now install the required packages for your project. Typically, the required packages are listed in a requirements.txt file. Make sure you have the requirements.txt file for your project.

2. Setup the pip and installing dependencies in Virtual environment

    - Upgrade pip
        `python -m pip install --upgrade pip`

    - To install the requirements, use the following command:
        `pip install -r requirements.txt`

- Run Streamlit Application `streamlit run Medical.py`

### IPython Notebook

Follow the instructions in the notebook `Medical Embeddings_Final.ipynb`

- Install requirements `pip install -r requirements.txt`
- Run Streamlit Application `streamlit run Medical.py`

    - Note: When you execute the code from the Jupyter Notebook, make sure to copy all these files into the modular_code folder (or into the same directory from where you will run the Streamlit application). This ensures that when you run the command streamlit run medical.py, all modules are correctly imported and the app works without errors.

      - Dimension-covid.csv
      - skipgramx11.bin
      - FastText.bin
      - skipgram-vec.csv
      - FastText-vec.csv

- Check result evaluation for all inputs in the streamlit application

### IPython Notebook

Follow the instructions in the notebook `Medical Embeddings_Final.ipynb`

