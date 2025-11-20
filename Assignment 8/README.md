# NLP Assignment  
**Name:** Kavisha Vaja  
**Roll No:** U23AI016  
**Course:** Natural Language Processing  

---

## Contents
This directory contains solutions for two NLP tasks:

- **Q2 – WordPiece Tokenization**
- **Q3 – Sentence Classification using Naïve Bayes**

---

## Q2 – WordPiece Tokenization
- All sentences from the dataset were first **lowercased** and **tokenized** using whitespace and punctuation.
- Implemented the **WordPiece algorithm**:
  - Created an initial character-level vocabulary.
  - Calculated bigram pair frequencies.
  - Applied **20 merge operations** to create subword units.
- The final vocabulary obtained after 20 merges was used to tokenize the target sentence:

**Sentence to tokenize:**  
`The cat is chasing the dog quietly.`

All steps, tables, and final tokenization results are provided in **q2.ipynb**.

---

## Q3 – Sentence Classification (Inform / Promo / Reminder)

### Training Data
A dataset of 9 sentences labelled as:
- **Inform**
- **Promo**
- **Reminder**

### Feature Engineering
Designed meaningful features for classification:
- **Binary features**:
  - Presence of **URL**
  - Presence of **numbers**
  - Presence of **punctuation** such as exclamation marks
- **Bag-of-words features**
- **Bigram probabilities** computed with **add-K smoothing (K = 0.3)**

### Preprocessing
- Lowercasing
- Removing unnecessary punctuation
- Extracting unigram and bigram features
- Vocabulary building for the Naïve Bayes classifier

### Classification
A **Naïve Bayes classifier** was trained using:
- Class prior probabilities  
- Feature likelihoods  
- Bigram likelihoods with smoothing  

The model predicts the label for the test sentence:

`You will get an exclusive offer in the meeting!`

All preprocessing steps, feature extraction, probability tables, and final classification output are included in **q3.ipynb**.

---

