# Byte Pair Encoding (BPE) and WordPiece Tokenization  
### Assignment – NLP  
### Roll No: **U23AI016**  
### Author: **Kavisha Vaja**

---

##  Overview  
This project implements **Byte Pair Encoding (BPE)** and **WordPiece Tokenization** **from scratch**, using the Gujarati corpus provided in Assignment-1.  
Both models generate a vocabulary size of **32,000 tokens**, without relying on external tokenization libraries.

---

## 📁 Files Included  
| File Name | Description |
|----------|-------------|
| `tokenized.json` | Preprocessed corpus data |
| `bpe_vocab.txt` | Generated BPE vocabulary |
| `wp_vocab.txt` | Generated WordPiece vocabulary |
| `bpe_train.py` | BPE training script |
| `wordpiece_train.py` | WordPiece training script |
| `README.md` | Documentation |

---


## 🚀 Features  
- Pure Python implementation (no external NLP/tokenizer libraries).  
- Supports Gujarati Unicode text.  
- Efficient merge operations using frequency-based BPE and likelihood-based WordPiece.  
- Outputs clean vocabulary files containing 32k subword tokens.  

---

## ▶️ How to Run the Code  

### **1. Train BPE**
```bash
python bpe_train.py
