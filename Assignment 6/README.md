# NLP Assignment 6 – Quadrigram Language Models  

##  Overview  
This assignment implements **Quadrigram (4-gram) Language Models** with two smoothing techniques:  
1. **Katz Backoff**  
2. **Kneser–Ney Smoothing**  

For each model, we generate sentences using:  
- **Greedy decoding** (maximum likelihood)  
- **Beam Search** (beam size = 20)  

The dataset used is `Guj_3000.txt`, which contains Gujarati sentences.  

---

## ⚙️ How to Run  

### 1. Open in Google Colab  
- Upload the notebook (`Assignment6.ipynb`) to **Google Colab**.  
- Upload the dataset file `Guj_3000.txt` in the same Colab session.  

### 2. Install Dependencies  
The only external library required is **NLTK**:  
```bash
!pip install nltk
```

### 3. Run the Notebook Step by Step  
The notebook is divided into sections:  
1. **Setup & Imports** – installs dependencies and loads libraries.  
2. **Load and Preprocess Dataset** – reads `Guj_3000.txt`, tokenizes sentences, and adds start/end tokens.  
3. **Build N-gram Counts** – extracts unigram, bigram, trigram, and quadrigram frequencies.  
4. **Katz Backoff Implementation** – computes backoff probabilities.  
5. **Kneser–Ney Smoothing Implementation** – computes smoothed probabilities.  
6. **Sentence Generation Functions** – implements greedy and beam search decoding.  
7. **Sentence Generation** – generates sample sentences for all models and methods.  

### 4. Outputs  
- The notebook prints generated Gujarati sentences.  
- Example outputs:  
  ```
  🔹 Katz Backoff - Greedy
  ગાંધીનગરમાં હાલમાં રાજકારણ ક્ષેત્રે શાળા વિકાસ સમિતિએ સ્થગિત થયું
  જામનગરમાં હાલમાં વિજ્ઞાન ક્ષેત્રે રાજ્ય સરકારએ શરુ કર્યું
  
  🔹 Kneser–Ney - Beam Search
  સુરતમાં આજે શિક્ષણ ક્ષેત્રે ઔદ્યોગિક વિકાસ નિગમએ ખુલાસો કર્યો
  જૂનાગઢમાં આ મહિને ક્રીડા ક્ષેત્રે શાળા વિકાસ સમિતિએ શરુ કર્યું
  ```
- You can adjust the loop to generate **100 sentences per model**.  

---

## 📂 Files in this Repository  
- `Assignment6.ipynb` → Colab notebook with full implementation.  
- `Guj_3000.txt` → Gujarati dataset (input text).  
- `README.md` → Instructions and documentation.  

---

## ✅ What I Did in This Assignment  
- Preprocessed Gujarati dataset for n-gram modeling.  
- Implemented **Katz Backoff** for quadrigrams.  
- Implemented **Kneser–Ney Smoothing** for quadrigrams.  
- Implemented **Greedy decoding** and **Beam Search (beam size=20)**.  
- Generated sample Gujarati sentences using both models and decoding methods.  


## Author

Assignment completed as part of **NLP Course - Assignment 6**.\
Rollno.: *U23AI016*\
Institute: SVNIT
