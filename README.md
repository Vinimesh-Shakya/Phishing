# Comparative Analysis of Textual and High-Dimensional Numerical Features for Email Phishing

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/Framework-PyTorch%20%2F%20TensorFlow-orange.svg)](https://github.com/Vinimesh-Shakya/Phishing)

Official repository for the research paper: **"Comparative Analysis of Textual and High-Dimensional Numerical Features for Email Phishing"** by Vinimesh Shakya and Shubha Mishra.

This project evaluates and compares the performance of machine learning and deep learning models on two distinct data modalities for phishing detection: high-dimensional numerical features (URL-based metadata) and textual features (raw email bodies).

---

## 🚀 Key Highlights

* **Modality Comparison:** Direct performance and computational trade-off analysis between textual semantics (NLP) and structured numerical features.
* **Deep Learning Architectures:** Implementation of **BERT** and **LSTM** for text data, alongside **TabNet** and **MLP** for tabular numerical data.
* **Classical ML Baselines:** Comprehensive testing using Logistic Regression, Random Forest, Gradient Boosting, AdaBoost, XGBoost, and CatBoost.
* **Computational Efficiency:** Demonstrates that TabNet on numerical features achieves an F1-score of **99.70%** in just 44 seconds (CPU), while BERT achieves **98.26%** requiring 1.5+ hours (GPU).

---

## 📂 Datasets

1. **Dataset I (Numerical Feature Dataset):**
   * 10,000 instances (5,000 phishing, 5,000 legitimate).
   * 48 URL-based attributes reduced to the top 30 using mutual information scores.
2. **Dataset II (Text Dataset):**
   * 20,698 emails (imbalanced: 39.2% phishing vs 60.8% safe).
   * Preprocessed using WordNet lemmatization, stop-word removal, TF-IDF vectorization, and n-gram characteristics.

---

## 📊 Key Results

### Text Data (Dataset II) Performance
| Model | Accuracy | Precision | Recall | F1 Score |
| :--- | :---: | :---: | :---: | :---: |
| **BERT** | **98.26%** | **98.28%** | **98.26%** | **98.26%** |
| Logistic Regression | 97.00% | 94.05% | 98.61% | 96.27% |
| XGBoost | 96.42% | 93.13% | 98.12% | 95.56% |

### Feature Data (Dataset I) Performance
| Model | Accuracy | Precision | Recall | F1 Score |
| :--- | :---: | :---: | :---: | :---: |
| **TabNet** | **99.70%** | **99.90%** | **99.50%** | **99.70%** |
| MLP | 99.55% | 99.60% | 99.50% | 99.55% |
| XGBoost | 99.20% | 99.40% | 99.31% | 99.21% |

### Computational Trade-off
| Model | Hardware | F1-Score | Train Duration | Epochs |
| :--- | :--- | :---: | :--- | :---: |
| **BERT** | T4 GPU (Colab) | 98.26% | 1 hr 34 min 38 s | 4 |
| **TabNet** | CPU (32GB RAM) | 99.70% | 44 s | 30 |

---

## 🛠️ Usage

```bash
# Clone the repository
git clone https://github.com/Vinimesh-Shakya/Phishing.git
cd Phishing

# Install dependencies
pip install -r requirements.txt
```

---

## 📑 Citation

Our research paper, *"Comparative Analysis of Textual and High-Dimensional Numerical Features for Email Phishing,"* is currently **under review for publication**. 

The official BibTeX citation and DOI link will be updated here once the paper is published. If you find this repository or methodology useful for your own work in the meantime, please consider starring this repository and linking back to this GitHub page!


<!--
## 📑 Citation

If you find this repository useful, please cite our paper:

```bibtex
@article{shakya2026comparative,
  title={Comparative Analysis of Textual and High-Dimensional Numerical Features for Email Phishing},
  author={Shakya, Vinimesh and Mishra, Shubha},
  year={2026}
}
```
-->

