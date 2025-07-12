# 🧬 Generative AI Notes

This folder contains notebooks and lecture notes focused on the **theory and practice of Generative AI** models. The main file is:

- 📄 `generativeAI.ipynb`

---

## 📘 Overview

Generative AI refers to a class of models capable of **creating new content**, such as:

- Images (e.g., faces, artwork)
- Text (e.g., articles, stories)
- Audio (e.g., music, speech)
- Code
- Video

These models **learn patterns from data** and generate outputs that resemble the training distribution.

---

## 📌 Topics Covered

### 🔹 Theory

| Model Type          | Generates               | Core Idea                              |
|---------------------|--------------------------|-----------------------------------------|
| VAE (Variational AE) | Images, audio           | Latent space sampling                   |
| GAN (Generative Adversarial Network) | Images, videos | Generator vs Discriminator             |
| Diffusion Models    | Ultra-realistic images   | Denoising from noise                    |
| Autoregressive Models | Text, music, code      | Predict next token step-by-step        |
| Transformers (LLMs) | Text, reasoning          | Attention-based sequence modeling       |
| Flow Models         | Invertible data          | Exact likelihood and sampling           |

Includes architecture comparisons of VAE vs GAN vs Diffusion.

---

### 🔹 Practice & Code

#### ✅ VAE on MNIST (Digit: 5)

- Load and filter MNIST data for digit 5
- Define a simple VAE architecture
- Train for 10 epochs
- Visualize:
  - Original vs reconstructed digits
  - Generated samples from latent space

#### ✅ GAN on MNIST (Digit: 4)

- Train a GAN to generate digit 4 images
- Define Generator and Discriminator in PyTorch
- Binary cross-entropy loss
- Trained for 20 epochs
- Outputs show increasing fidelity of generated digits

---

## 🔍 Key Learning Points

- Understand how different generative models work
- Train and evaluate VAE and GAN on real image datasets
- Learn how latent spaces are sampled
- Compare output quality, training stability, and use cases

---

## 📦 Requirements

```bash
pip install torch torchvision matplotlib
```
## ✍️ Author
Prepared by Hai Nguyen Ngoc
2025 – Part of Generative AI Lecture Series
