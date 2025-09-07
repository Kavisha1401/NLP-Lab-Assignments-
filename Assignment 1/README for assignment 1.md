# NLP Assignment 1 -- Text Preprocessing

## 📌 Overview

This repository contains my submission for **Assignment 1** of the
**Natural Language Processing (AI357)** course.\
The focus of this assignment is **text preprocessing** using
tokenization and corpus statistics.

The tasks completed in this notebook include:\
1. **Dataset Download**\
- Downloaded monolingual text data from:\
- [IndicCorpV2](https://huggingface.co/datasets/ai4bharat/IndicCorpV2)\
- [OSCAR-2301](https://huggingface.co/datasets/oscar-corpus/OSCAR-2301)

2.  **Sentence & Word Tokenization**
    -   Implemented a custom tokenizer to handle:
        -   Punctuation\
        -   URLs\
        -   Numbers & decimals\
        -   Email IDs\
        -   Dates
3.  **Saving Tokenized Data**
    -   Stored tokenized sentences into text files (each line = one
        tokenized sentence).\
    -   Learned to use **Parquet format** for large data storage with
        compression.
4.  **Corpus Statistics Computation**
    -   Total number of characters → **118**\
    -   Average word length → **3.52**\
    -   Type-Token Ratio (TTR) → **0.926**

------------------------------------------------------------------------

## ⚙️ Requirements

Make sure you have the following installed:

``` bash
pip install pandas numpy nltk datasets pyarrow
```

------------------------------------------------------------------------

## ▶️ How to Run the Notebook

1.  **Clone the repository (or open in Colab):**

    ``` bash
    git clone <your_repo_link>
    cd NLP/Assignment_1
    ```

2.  **Open the Jupyter Notebook:**

    -   Run locally:

        ``` bash
        jupyter notebook assignment1.ipynb
        ```

    -   Or upload `assignment1.ipynb` to [Google
        Colab](https://colab.research.google.com/).

3.  **Run all cells in order.**

    -   The dataset will be downloaded from Hugging Face.\
    -   Tokenization will be performed.\
    -   Tokenized outputs will be saved in files.\
    -   Corpus statistics will be displayed.

------------------------------------------------------------------------

## 📝 Notes

-   Large datasets may take time to process. Use smaller samples for
    testing.\
-   Use Parquet format (`.parquet`) to efficiently store and compress
    large tokenized corpora.
