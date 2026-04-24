# 🛡️ Intrusion Detection System Using Machine Learning Algorithms

A machine learning-based Network Intrusion Detection System (IDS) that classifies network traffic as normal or malicious using the KDD Cup 1999 dataset.

---

## 📌 Project Overview

Network security is a critical concern in today's digital world. This project builds and compares multiple machine learning models to detect network intrusions by classifying connections into five categories: **Normal, DoS, Probe, R2L, and U2R**.

---

## 📂 Dataset

- **Name:** KDD Cup 1999 Data
- **File Used:** `kddcup.data_10_percent_corrected`
- **Records:** ~494,021
- **Features:** 41
- **Source:** [Kaggle](https://www.kaggle.com/datasets/galaxyh/kdd-cup-1999-data) | [UCI Archive](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html)

---

## 🤖 Algorithms Used

Gaussian Naive Bayes, Decision Tree, Random Forest, Support Vector Machine (SVM), Logistic Regression, and Gradient Boosting.

---

## ⚙️ Preprocessing Steps

- Label encoding of categorical features (`protocol_type`, `flag`)
- Dropped low-value columns (`service`, `is_host_login`, `num_outbound_cmds`)
- Removed 8 highly correlated features using correlation heatmap
- Applied MinMaxScaler normalization to scale features to [0, 1]
- Train-test split: 67% train / 33% test

---

## 📊 Results

| Model | Train Accuracy | Test Accuracy |
|---|---|---|
| Naive Bayes | ~88% | ~87.90% |
| Decision Tree | ~99.5% | ~99.38% |
| Random Forest | ~99.99% | ~99.97% |
| SVM | ~99.9% | ~99.88% |
| Logistic Regression | ~99.4% | ~99.36% |
| Gradient Boosting | ~99.95% | ~99.91% |

✅ **Best Model: Random Forest** with 99.97% test accuracy.

---

## 🚀 How to Run

1. Open [Google Colab](https://colab.research.google.com/)
2. Download dataset from [Kaggle](https://www.kaggle.com/datasets/galaxyh/kdd-cup-1999-data)
3. Upload arhive.zip for unziping `kddcup.data_10_percent_corrected` to Colab
4. Run each cell step by step:
   - Install & import libraries
   - Load and explore data
   - Preprocess features
   - Train-test split
   - Train all 6 models
   - Compare results

---

## 🛠️ Libraries Used

```
pandas, numpy, matplotlib, seaborn, scikit-learn
```

---

## 📁 Project Structure

```
├── IDS_ML.ipynb          # Main Colab notebook
├── README.md             # Project documentation
└── kddcup.data_10_percent_corrected  # Dataset file
```

---

## 📝 Conclusion

Machine learning models, especially ensemble methods like Random Forest and Gradient Boosting, are highly effective for network intrusion detection and significantly outperform traditional signature-based detection systems.
