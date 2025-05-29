Here is a full `README.md` file written specifically for your thesis project, based on the content and structure of your defense and paper:

---

````markdown
# 🧠 Semantic Trajectories for Bot Detection in Low-Resource Languages

This repository contains the code, data samples, and methodology for the M.Sc. thesis project:  
**"Semantic Trajectories Analysis in Natural Languages for Spotting the Bots"**  
by **Syed Taqi Ali**, Faculty of Computer Science, HSE University.

---

## 📌 Overview

This project presents an **unsupervised approach** to distinguish AI-generated (bot) text from human-written content using **semantic trajectory clustering**. The focus is on **low-resource languages**, specifically **Lao** and **Luxembourgish**, which lack mainstream NLP toolkits.

The core pipeline combines **trigram embeddings** (via FastText and Word2Vec), **dimensionality reduction**, and **Wishart clustering** to detect differences in semantic flow between human and bot texts.

---

## 🧪 Dataset

Two corpora were created per language:

- **Human Corpus**: Literary and religious texts  
- **Bot Corpus**: GPT-4o generated responses based on the human dataset topics

| Language       | Human Tokens | Bot Tokens |
|----------------|--------------|------------|
| Lao            | 170k         | 27k        |
| Luxembourgish  | 420k         | 27k        |

Custom tokenizers and lemmatizers were built for both languages.

---

## 🔍 Methodology

**Pipeline:**

1. **Preprocessing** – Cleaning, lemmatization, trigram extraction  
2. **Embedding** – Word2Vec and FastText comparison  
3. **Dimensionality Reduction** – PCA, t-SNE  
4. **Clustering** – Wishart algorithm  
5. **Evaluation** – Calinski–Harabasz (CH Index), silhouette, Davies-Bouldin  
6. **Entropy-Complexity Analysis** – To assess structural differences

---

## 💡 Key Findings

- **FastText outperformed Word2Vec** in vocab coverage and clustering
- Bot text showed **simpler, more uniform patterns**
- Clusters from human text were **semantically richer and more dispersed**
- **CH score:** FastText (CH=92) significantly higher than Word2Vec (CH=5) for Luxembourgish
- Method is language-agnostic and **requires no labeled data**

