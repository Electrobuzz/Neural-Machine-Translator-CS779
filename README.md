# 🌐 Neural Machine Translation for Indian Languages (EN→HI, EN→BN)

## 📌 Overview
This project implements a **from-scratch Neural Machine Translation (NMT) system** for translating English into **Hindi** and **Bengali**.

Built under strict constraints (no pretrained models or external architectures), the system uses a **Transformer-based Seq2Seq model** along with a **custom Byte Pair Encoding (BPE) tokenizer**.

---

## 🚀 Features
- Fully from-scratch implementation (no BERT/GPT, no HuggingFace)
- Custom Transformer architecture
- Optimized Fast BPE Tokenizer
- Supports:
  - English → Hindi
  - English → Bengali
- Advanced training techniques:
  - Noam Learning Rate Scheduler
  - Label Smoothing
  - Gradient Clipping

---

## 🏆 Results

| Metric  | Score |
|--------|------|
| BLEU   | 0.175 |
| ROUGE  | 0.446 |
| chrF++ | 0.445 |
| Rank   | 16 |

---

## 📂 Dataset
- English–Hindi: 80,797 sentence pairs  
- English–Bengali: 68,849 sentence pairs  

---

## 🧠 Model Architecture

### Tokenizer
Custom **OptimizedFastBPETokenizer**
- Built from scratch
- Efficient merge operations using word-frequency dictionary

### Transformer
- Embedding size: 256  
- Encoder layers: 3  
- Decoder layers: 3  
- Attention heads: 4  
- Feedforward dimension: 1024  

---

## 🔄 Training Details

### Optimizer
- Adam (β₁=0.9, β₂=0.98, ε=1e-9)

### Techniques
- Noam Learning Rate Scheduler  
- Label Smoothing (0.1)  
- Gradient Clipping (1.0)  
- Padding & sequence truncation  

---

## 📉 Model Evolution

| Phase | Model | Outcome |
|------|------|--------|
| Week 1–2 | GRU | Failed (collapse) |
| Week 3 | LSTM | Failed |
| Week 4 | GRU + Attention | Low performance |
| Week 5 | Transformer | Successful |

---

## 🔍 Inference
- Greedy decoding
- Stops at `<eos>` or max length

---

## 🛠️ Tech Stack
- Python
- PyTorch
- NumPy

---
