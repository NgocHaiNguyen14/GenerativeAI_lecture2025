# 🤖 Large Language Models (LLMs)

This folder focuses on **Large Language Models** (LLMs), including theoretical foundations and practical implementations using models such as **BERT** and **GPT-2**.

---

## 📁 Contents

| File / Subfolder             | Description                                           |
|-----------------------------|-------------------------------------------------------|
| `LLM_theory.ipynb`            | Core concepts and architecture of Transformer & LLMs |
| `BERT/vertopal_BERT.ipynb`    | Fine-tuning BERT on the CoLA dataset                 |
| `GPT-2/vertopal.com_GPT_2.ipynb` | Training and evaluating GPT-2 on dialogue summarization |

---

## 📘 Overview

LLMs are AI systems based on **Transformer architecture** and trained on large-scale text corpora. They are capable of:

- Text generation (e.g., GPT)
- Sentence classification (e.g., BERT)
- Translation, summarization (e.g., BART, T5)
- Chat and reasoning (e.g., ChatGPT, LLaMA)

---

## 📌 Topics Covered

### 🔹 `LLM_theory.ipynb`

- Transformer architecture:
  - Token embeddings, positional encodings
  - Self-attention and multi-head attention
  - Encoder/Decoder blocks
- Core LLMs comparison:
  | Model | Architecture       | Directionality | Pretraining Task              | Use Cases                        |
  |-------|--------------------|----------------|-------------------------------|----------------------------------|
  | GPT   | Decoder-only       | Left-to-right  | Causal LM                     | Chatbots, text generation        |
  | BERT  | Encoder-only       | Bidirectional  | MLM + NSP                     | Classification, QA, NER          |
  | BART  | Encoder + Decoder  | Bi + Autoregressive | Denoising autoencoder    | Summarization, translation       |

---

### 🔹 `BERT/vertopal_BERT.ipynb``

- Dataset: **Corpus of Linguistic Acceptability (CoLA)**
- Fine-tuning BERT on:
  - `in_domain_train.tsv` for training
  - `out_of_domain_dev.tsv` for cross-domain evaluation
- Shows training pipeline using Hugging Face Transformers
- Great for tasks like:
  - Domain adaptation
  - Sentence-level classification
  - Robustness testing

---

### 🔹 `GPT-2/vertopal.com_GPT_2.ipynb``

- Dataset: **dialogsum-test** (from Hugging Face)
- Task: Dialogue summarization using GPT-2
- Key steps:
  - Install with `bitsandbytes`, `peft`, `trl`, etc.
  - Load GPT-2 with 4-bit quantization for efficient GPU use
  - Generate summaries with zero-shot inference
- Includes:
  - GPU memory monitoring
  - Prompt formatting
  - Evaluation vs human baseline

---

## 🛠️ Requirements

```bash
pip install transformers datasets torch bitsandbytes peft accelerate trl
```
## ✍️ Author
Prepared by Hai Nguyen Ngoc
2025 – Part of Generative AI Lecture Series
