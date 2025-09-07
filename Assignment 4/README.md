# NLP Assignment 4 -- N-Gram Language Models with Smoothing

## 📌 Overview

This assignment focuses on building and evaluating **n-gram language
models**.\
The following models were implemented: - **Unigram Model** - **Bigram
Model** - **Trigram Model** - **Quadrigram Model**

To handle data sparsity, three smoothing techniques were applied: 1.
**Add-One Smoothing** 2. **Add-K Smoothing** 3. **Add-Token-Type
Smoothing**

Finally, the models were tested on **1000 randomly chosen news
sentences** to compute sentence probabilities.

------------------------------------------------------------------------

## ⚙️ Requirements

-   Python 3.x
-   Jupyter Notebook
-   Libraries:
    -   `nltk`
    -   `numpy`
    -   `pandas`
    -   `matplotlib` (optional, for plots)
    -   `collections` (Python standard library)

Install dependencies (if needed):

``` bash
pip install nltk numpy pandas matplotlib
```

------------------------------------------------------------------------

## ▶️ How to Run

1.  Clone or download this repository.

2.  Open the Jupyter Notebook:

    ``` bash
    jupyter notebook NLP_Assignment_4.ipynb
    ```

3.  Run the cells in order:

    -   **Data Preprocessing** -- Tokenization and dataset preparation.
    -   **Model Building** -- Unigram, Bigram, Trigram, and Quadrigram
        models.
    -   **Smoothing** -- Add-One, Add-K, and Token-Type smoothing
        applied to n-grams.
    -   **Sentence Probability Evaluation** -- Compute probabilities for
        1000 sentences from news data.

------------------------------------------------------------------------

## 📂 Project Structure

    ├── NLP_Assignment_4.ipynb   # Main Jupyter Notebook with code & results
    ├── guj_Gujr.txt           # Language data used for model training (from Assignment 1)
    ├── Guj_sentences.txt       # 1000 randomly chosen sentences for evaluation
    ├── README.md                # Project documentation

------------------------------------------------------------------------

## 📝 What I Did

-   Implemented **n-gram language models** (1-gram to 4-gram).
-   Applied **three smoothing techniques** to address unseen
    words/sequences.
-   Evaluated the **probabilities of 1000 news sentences**.
-   Compared how different n-grams and smoothing methods affect results.

------------------------------------------------------------------------

## 📊 Results & Observations

-   **Higher-order n-grams** (Trigram, Quadrigram) give more
    context-aware probabilities but suffer more from sparsity.
-   **Add-One smoothing** overestimates unseen events.
-   **Add-K smoothing** allows better tuning by selecting `k`.
-   **Token-Type smoothing** provides an alternative, though not always
    a valid probability distribution.

------------------------------------------------------------------------

## Author

Assignment completed as part of **NLP Course -- Assignment 4**.\
Rollno.: *\[U23AI016\]*\
Institute: SVNIT


