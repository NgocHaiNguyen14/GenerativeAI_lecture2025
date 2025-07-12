# 🧠 BERT Fine-Tuning: CoLA Dataset

This folder contains the notebook and notes related to **fine-tuning BERT** (Bidirectional Encoder Representations from Transformers) on the **Corpus of Linguistic Acceptability (CoLA)**.

- 📄 `BERT.ipynb`

---

## 📘 Overview

BERT is a **transformer-based** encoder-only model designed to learn deep bidirectional representations from unlabeled text.

This notebook explores:

- Fine-tuning BERT for **sentence-level classification**
- Evaluating BERT's **generalization ability** across domains

---

## 🧾 Dataset: CoLA

- **Name:** Corpus of Linguistic Acceptability
- **Size:** 10k+ sentences (train/dev)
- **Task:** Binary classification — Acceptable (1) vs. Unacceptable (0)
- **Domain Split:**
  - `in_domain_train.tsv` → Used for training
  - `out_of_domain_dev.tsv` → Used for validation/generalization

📎 [Dataset source](https://nyu-mll.github.io/CoLA/)

---

## 📌 Key Steps

1. **Data Preprocessing**
   - Load `.tsv` files into Pandas
   - Tokenize sentences with BERT's WordPiece tokenizer
   - Convert to tensors

2. **Model Setup**
   - Use `BertForSequenceClassification` from Hugging Face Transformers
   - Add classification head

3. **Training**
   - Use `AdamW` optimizer and learning rate scheduler
   - Track loss and evaluation metrics

4. **Evaluation**
   - Accuracy on out-of-domain samples
   - Visualize performance

---

## 💡 Why CoLA?

- Tests **linguistic generalization**
- Measures **domain transfer robustness**
- Good benchmark for BERT's **attention to syntax and grammar**

---

## 🛠️ Requirements

```bash
pip install torch scikit-learn transformers pandas numpy matplotlib
```
## ✍️ Author
Prepared by Hai Nguyen Ngoc
2025 – For the Generative AI Lecture Series
