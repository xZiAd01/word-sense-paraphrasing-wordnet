# Word Sense & Paraphrasing with WordNet (NLTK)

This notebook performs automated text analysis and paraphrasing using **WordNet** (NLTK).
Given an input paragraph, it:
1. Repairs/aligns POS tags for WordNet usage
2. Maps content words to likely senses (synsets)
3. Finds shared high-level concepts across words
4. Generates paraphrases by swapping selected words with valid synonyms

## Key Components (as in the notebook)
- POS mapping and repair (Penn Treebank → WordNet POS)
- Sense mapping (`get_sense_map`)
- Shared concept discovery (hypernym-style general concepts)
- Controlled paraphrasing (`paraphrase_sentence`, pipeline runner)

## Tech Stack
- Python
- NLTK (WordNet, stopwords, tokenizers, POS tagger)

## Setup

### 1) Create environment (recommended)
```bash
python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows
# .venv\Scripts\activate
```
## 2) Install dependencies
```bash
pip install -r requirements.txt
```
## 3) Download required NLTK data (run once)
```bash
import nltk
nltk.download("punkt")
nltk.download("averaged_perceptron_tagger")
nltk.download("wordnet")
nltk.download("omw-1.4")
nltk.download("stopwords")
```
## Run
```
jupyter notebook
```

Open 3.2_final.ipynb and run cells in order.

## Notes / Configuration

- Paraphrases are heuristic and may produce awkward phrasing (expected for a rule-based baseline).

- Output quality depends heavily on WordNet coverage and POS tagging accuracy.
