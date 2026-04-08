# 📘 Interpretable Multi-Class Text Classification: DistilBERT vs. SVM

This repository contains a comparative study of modern Transformer-based architectures and traditional Machine Learning baselines for text classification.

Using the DBpedia 14-class ontology dataset, we evaluate performance and interpret model decision-making using LIME (Local Interpretable Model-agnostic Explanations).

---

## 📌 Project Overview

The goal of this project is to classify Wikipedia abstracts into **14 mutually exclusive categories** (e.g., Company, Artist, Plant, Animal).

We compare:
- A high-performance **DistilBERT model**
- A traditional **TF-IDF + Linear SVM baseline**

---

## 🚀 Key Features

- **Dataset**: 560,000 training samples across 14 classes  
- **Models**:
  - **DistilBERT**: A distilled version of BERT optimized for sequence classification  
  - **SVM Baseline**: TF-IDF vectorization with Linear Support Vector Machine  
- **Interpretability**:
  - Token-level explanations using **LIME**

---

## 📊 Results & Performance

The DistilBERT model consistently outperformed the traditional baseline, especially in capturing semantic nuances in complex categories like *WrittenWork* and *Company*.

| Model           | Accuracy | Weighted F1-Score |
|----------------|----------|-------------------|
| DistilBERT     | 99.27%   | 0.9927            |
| TF-IDF + SVM   | 98.68%   | 0.9868            |

---

## 📂 Repository Contents

- `notebook/MAIN.ipynb`  
  → End-to-end pipeline for preprocessing, TF-IDF training, and DistilBERT fine-tuning  

- `notebook/TEST.ipynb`  
  → Evaluation pipeline with:
  - Confusion matrix  
  - Classification report  
  - LIME explanations  

- `models/`  
  → Pre-trained model weights  
  ⚠️ Note: `pytorch_model.bin` required inside `bert_model/`

- `classes.txt`  
  → List of 14 ontology classes  

---

## ⚙️ Getting Started

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/interpretable-text-classification.git
cd interpretable-text-classification
```

### 2️⃣ Run Evaluation

Open the notebook And Run all cells to:

* Load trained models
* Generate evaluation metrics
* Visualize LIME explanations

⚠️ Ensure folder structure is intact (code uses relative paths)
---
👥 Contributors
Durgesh Premchand Bhirud
Debmalya Chatterjee
Thanusri Aenugula
John McWhirter
---
🎓 Academic Context

This project was developed as part of the ECEN 758 course at Texas A&M University.
