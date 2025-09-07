# NLP Assignment 2: DFA and FST

This directory contains solutions for **NLP Assignment 2**, which involves constructing a **Deterministic Finite Automaton (DFA)** for simplified English words and a **Finite State Transducer (FST)** for generating morphological features from nouns.

---

## Tasks

### 1. Deterministic Finite Automaton (DFA)
A DFA that accepts valid simplified English words. A valid word must:
- Start with a lowercase letter.
- Be followed by zero or more lowercase letters.
- Not contain digits, uppercase letters, spaces, or special characters.

**Examples:**
- ✅ Accepted: `cat`, `dog`, `a`, `zebra`
- ❌ Not Accepted: `dog1`, `1dog`, `DogHouse`, `Dog_house`, ` cats`

The DFA can be visualized using:
- [visual-automata](https://pypi.org/project/visual-automata/)
- [automathon](https://github.com/rohaquinlop/automathon)

### 2. Finite State Transducer (FST)
An FST that generates morphological features for nouns from the **Brown Corpus** (provided in `brown_nouns.txt`).

**Examples:**
```
fox     → fox+N+SG
foxes   → fox+N+PL
watches → watch+N+PL
tries   → try+N+PL
```

Rules implemented:
- **E insertion**: add `e` before `s` when the root ends with `-s`, `-z`, `-x`, `-ch`, `-sh`.
- **Y replacement**: change `-y` to `-ie` before adding `s`.
- **S addition**: simply add `s` at the end.

If an invalid form is encountered, output **`Invalid Word`**. Example:
```
foxs → Invalid Word
```

---

## Files
```
├── NLP-Assignment-2.pdf          # Assignment description
├── brown_nouns.txt               # Input noun corpus
├── dfa_solution.ipynb            # Notebook/implementation of DFA and FST
├── README.md                     # Project documentation
```

---

## Installation
Make sure you have Python 3.8+ installed. Then install dependencies:

```bash
pip install visual-automata automathon
```

---

## Usage
### Run DFA
Open the DFA notebook and run cells to:
- Build the automaton.
- Test input strings for acceptance.
- Visualize the DFA.

### Run FST
Open the FST notebook and run cells to:
- Load nouns from `brown_nouns.txt`.
- Apply morphological rules.
- Output valid forms with tags (SG/PL).

---

## Example Output
**DFA test:**
```
Input: cat → Accepted
Input: Dog1 → Not Accepted
```

**FST test:**
```
Input: fox     → fox+N+SG
Input: foxes   → fox+N+PL
Input: foxs    → Invalid Word
```

---




