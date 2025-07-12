# 🧠 GPT-2: Dialogue Summarization with Quantization

This folder contains the notebook and notes for **fine-tuning and evaluating GPT-2** on a dialogue summarization task using **efficient 4-bit quantization**.

- 📄 `GPT_2.ipynb`)

---

## 📘 Overview

This notebook demonstrates how to:

- Load and run GPT-2 with **low-bit quantization** using `bitsandbytes`
- Use the **dialogsum-test** dataset from Hugging Face
- Generate summaries from conversational input in **zero-shot** mode
- Evaluate model output vs. human-written summaries

---

## 📎 Dataset: `dialogsum-test`

- **Source:** Hugging Face (`neil-code/dialogsum-test`)
- **Task:** Summarize multi-turn dialogue into concise sentences
- **Features:**
  - `dialogue`: the raw conversation
  - `summary`: the ground truth summary
  - `topic`: the general subject of the conversation

---

## 🧪 Key Components

### 🔹 Setup

- Installs tools: `bitsandbytes`, `transformers`, `trl`, `peft`, `datasets`, etc.
- Disables Weights & Biases tracking (`WANDB_DISABLED=true`)
- Loads the GPT-2 model with:
  - `load_in_4bit=True`
  - `bnb_4bit_quant_type='nf4'`
  - `bnb_4bit_compute_dtype=torch.float16`

### 🔹 Prompting & Inference

- Formats input as:
  ```
  Instruct: Summarize the following conversation.
  [dialogue]
  Output:
  ```
- Uses `generate()` with:
  - `temperature=0.1`
  - `top_p=0.95`
  - `num_beams=1`

### 🔹 Evaluation

- Compares model-generated output with human reference summaries
- Logs GPU memory usage using NVML (NVIDIA Management Library)
- Shows timing and inference performance

---

## 📦 Requirements

```bash
pip install bitsandbytes transformers peft accelerate datasets scipy einops evaluate trl
```

Make sure you have a CUDA-compatible GPU to benefit from quantization.

---

## 📁 File

| File Name                | Description                          |
|--------------------------|--------------------------------------|
| `vertopal.com_GPT_2.ipynb` | Fine-tuning GPT-2 for summarization  |

---

## ✍️ Author

Prepared by Hai Nguyen Ngoc
2025 – Part of _Generative AI Lecture Series_

