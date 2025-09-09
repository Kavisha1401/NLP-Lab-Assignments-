#  NLP Assignment 5 -- N-gram Language Models with Smoothing

## 📂 Project Overview

This project implements **statistical language models** (Unigram,
Bigram, Trigram, and Quadrigram) for a Gujarati dataset. It applies two
smoothing techniques to handle unseen words and n-grams:

-   **Good-Turing Smoothing** (all models)
-   **Deleted Interpolation** (Quadrigram model)


------------------------------------------------------------------------

## 🗂 Dataset

-   Input: `Guj_3000.txt` (Gujarati sentences, one per line)
-   Preprocessing: Tokenization, padding with `<s>` and `</s>` for
    n-grams
-   Splits:
    -   **Training set** -- Remaining sentences
    -   **Validation set** -- 1000 sentences (or proportionally fewer if
        dataset \< 3000)
    -   **Test set** -- 1000 sentences (or proportionally fewer if
        dataset \< 3000)

------------------------------------------------------------------------

## 🛠 Features Implemented

### 1. **Data Preparation**

-   Reads raw text file
-   Tokenizes sentences into words
-   Splits into Train/Val/Test

### 2. **N-gram Models**

-   Built **Unigram, Bigram, Trigram, Quadrigram** frequency counts
-   Vocabulary extracted from training data

### 3. **Good-Turing Smoothing**

-   Handles unseen n-grams
-   Computes adjusted counts and probabilities
-   Generates **Nc table** (`count → frequency of that count`)
-   Produces **C**\* values for top 100 frequencies

### 4. **Sentence Probability Computation**

-   Calculates **log probability** of each sentence in validation and
    test sets

### 5. **Deleted Interpolation (Quadrigram)**

-   Combines Unigram + Bigram + Trigram + Quadrigram
-   Optimizes λ (weights) using held-out data



## 🚀 How to Run

### 1. Open Google Colab

Go to [Google Colab](https://colab.research.google.com/)

### 2. Upload Files

-   Upload `Guj_3000.txt` into `/content/`
-   Upload `NLP-Assignment-5.pdf` (optional for reference)

### 3. Run the Notebook

Copy-paste `Assignment5_NLP.ipynb` code (provided in this repo) into
Colab and execute cells in order.

### 4. Outputs

-   Logs will show vocabulary, probabilities, and example sentence
    scores\
-   A table of top 100 Good-Turing counts will be printed\
-   Final λ values from Deleted Interpolation will be displayed

------------------------------------------------------------------------

## 📑 File Structure

    .
    ├── Guj_3000.txt              # Dataset (Gujarati sentences)
    ├── Assignment5_NLP.ipynb     # Main Colab notebook
    ├── NLP-Assignment-5.pdf      # Assignment brief
    └── README.md                 # Project documentation

------------------------------------------------------------------------

## 📌 Notes

-   If your dataset has \< 3000 sentences, the script automatically
    adjusts splits proportionally.
-   All outputs are printed in Colab; you can also save them into `.csv`
    if required.

------------------------------------------------------------------------
## Author

Assignment completed as part of **NLP Course - Assignment 5**.\
Rollno.: *\[U23AI016\]*\
Institute: SVNIT


