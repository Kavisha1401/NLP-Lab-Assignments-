# NLP Assignment 7

**Student:** U23AI016

## Overview

This assignment implements various NLP techniques including PMI (Pointwise Mutual Information) calculation, TF-IDF vectorization, and nearest neighbor search on tokenized text data.

## Assignment Tasks

### Question 1: PMI Score Computation
Computes PMI scores for all bigrams in validation and testing sets using bigram and unigram language models trained on training data.

**Implementation:** `q1.ipynb`

**Key Features:**
- Loads pre-trained unigram and bigram models from pickle files
- Calculates PMI scores using the formula: `PMI(w1, w2) = log(P(w1,w2) / (P(w1) * P(w2)))`
- Generates PMI tables for validation and test sets
- Outputs top 10 PMI scores for each dataset
- Saves results to parquet files

**Output Files:**
- `validation_pmi.parquet`
- `test_pmi.parquet`

### Question 2: TF-IDF Vectorization
Vectorizes all sentences in training, validation, and testing data using TF-IDF. Uses IDF scores learned from training data for validation and test sets.

**Implementation:** `q2.ipynb`

**Key Features:**
- Custom implementation of TF-IDF without external libraries
- Tokenization with lowercase conversion and punctuation removal
- IDF computation from training corpus (5,477 unique words)
- Memory-efficient sparse vector representation
- Separate vectorization for train (1,238), validation (154), and test (156) sentences

**Key Functions:**
- `tokenize()`: Preprocesses and splits sentences into tokens
- `compute_idf()`: Calculates inverse document frequency from training data
- `compute_tf()`: Calculates term frequency for individual sentences
- `create_tfidf_vectors()`: Generates sparse TF-IDF vectors

### Question 3: Nearest Neighbor Search
Finds nearest neighbors for each sentence in validation and testing sets using TF-IDF vectors and cosine similarity.

**Implementation:** `q3.ipynb`

**Key Features:**
- Uses scikit-learn's `TfidfVectorizer` for vectorization
- Computes cosine similarity matrices for validation and test sets
- Finds nearest neighbor by excluding self-similarity (diagonal set to -1)
- Appends nearest neighbor information to original dataframes

**Output Files:**
- `validation_with_neighbors.parquet`
- `test_with_neighbors.parquet`

### Question 4: Bonus Question
Extends nearest neighbor search to find neighbors in the training set for validation and test sentences. Addresses computational efficiency for large training datasets.

**Status:** To be implemented

**Suggested Approach:**
- Use approximate nearest neighbor algorithms (e.g., FAISS, Annoy)
- Implement batch processing for memory efficiency
- Consider dimensionality reduction techniques
- Use sparse matrix operations for faster computation

## Usage

Run each notebook in sequence:

```bash
jupyter notebook q1.ipynb  # Compute PMI scores
jupyter notebook q2.ipynb  # Generate TF-IDF vectors
jupyter notebook q3.ipynb  # Find nearest neighbors
```

## Results Summary

- **Vocabulary Size:** 5,477 unique words (from training data)
- **Training Sentences:** 1,238
- **Validation Sentences:** 154
- **Test Sentences:** 156
- **Bigram Model Size:** 8,264 bigrams

## Notes

- The dataset appears to be in Gujarati language (Devanagari script)
- PMI scores show many `-inf` values due to zero bigram counts in validation/test sets
- Sparse vector representation used in Q2 for memory efficiency
- Q3 uses sklearn's TfidfVectorizer for consistency and performance

## Future Improvements

1. Handle out-of-vocabulary words more gracefully
2. Implement smoothing techniques for PMI calculation
3. Optimize nearest neighbor search for large datasets (Question 4)
4. Add evaluation metrics for nearest neighbor quality
5. Implement cross-validation for model validation

## References

- Assignment requirements from `NLP-Assignment-7.pdf`
- Pre-trained models from Assignment 4
- Datasets from Assignment 5
