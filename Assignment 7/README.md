#  NLP Assignment 10 – POS Tagging using HMM  
### Submitted by: **U23AI016**

##  Overview
This project implements a Hidden Markov Model (HMM) based POS tagger using:

- K-Fold Cross-Validation  
- Emission & Transition Probability Estimation  
- Viterbi Decoding  
- Evaluation using Precision, Recall, and F1-Score  

The model uses the provided **WSJ POS-tagged corpus** (`wsj_pos_tagged_en.txt`), which contains 3914 tagged sentences.

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `main.py` | Contains HMM training, Viterbi decoding, K-fold cross-validation, and evaluation code |
| `wsj_pos_tagged_en.txt` | POS-tagged dataset |
| `output.png` | Screenshot of evaluation results |
| `NLP-Assignment-10.pdf` | Assignment description |

---

##  Program Workflow

###  1. Read Tagged Corpus  
The dataset is parsed into `(words, tags)` sequences.

###  2. K-Fold Data Splitting  
The sentences are split into 5 folds for cross-validation.

###  3. HMM Training  
From the training split, the program calculates:

- Transition probabilities  
- Emission probabilities  
- Laplace smoothing for unknown words  

###  4. Viterbi Decoding  
Predicts the most likely tag sequence for each test sentence using dynamic programming.

###  5. Evaluation  
Computes overall *Precision, Recall, and F1-score* for each fold and their averages.

---

##  How to Run

Make sure the dataset and `main.py` are in the same directory.  
Then run:

```bash
python main.py
