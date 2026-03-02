# Optimizers_and_Tranformer

# Optimizer Comparison on Transformer (Adam, AdamW, SGD)

This repository contains experiments comparing the performance of three optimizers — **SGD**, **Adam**, and **AdamW** — on a transformer-based sentiment classification task (IMDB dataset).

## 🔍 Overview
- **Model:** Transformer
- **Dataset:** IMDB Sentiment Analysis
- **Epochs:** 20
- **Batch size:** 128
- **Framework:** TensorFlow / PyTorch

## 📈 Results Summary
![Optimizer Comparison](plots/optimizer_comparison_report.png)

| Optimizer | Val Accuracy | Val Loss | Observation |
|------------|---------------|-----------|-------------|
| SGD | 53.3% | 0.80 | Slow convergence, stable generalization |
| Adam | 78.6% | 0.47 | Fast learning, slight overfitting |
| AdamW | **81.1%** | **0.42** | Best generalization, stable training |

## 🧠 Key Insight
AdamW achieves smoother convergence by decoupling weight decay from gradient updates, improving regularization over Adam.

---

## ⚙️ Reproduce
```bash
pip install -r requirements.txt
python notebooks/optimizer_comparison.ipynb
