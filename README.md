# 🎯**Anomaly Detection in Credit Card Transactions**

## 🧠 Objective

- Detect suspicious transactions **without using labels** during training.
- Handle a **highly imbalanced dataset**.
- Evaluate model performance using **Precision**, **Recall**, and **F1-score**.

---

## 📦 Dataset

- **Source:** [Kaggle – Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)  
- **Rows:** 284,807 transactions  
- **Features:**  
  - `V1` … `V28` (anonymized PCA components)  
  - `Amount`, `Time`  
- **Label (`Class`):**  
  - `0` = normal, `1` = fraud  
  - Hidden during model training; used only for evaluation.

---

## 🛠️ Project Workflow

### 1️⃣ Data Exploration
- Analyze distributions of `Amount` and `Time`.
- Identify patterns and **class imbalance**.

### 2️⃣ Preprocessing
- Scale numerical features using **MinMaxScaler**.
- Apply **PCA** for dimensionality reduction and visualization.

### 3️⃣ Modeling
- Train **unsupervised models**:  
  - **Isolation Forest**  
  - **One-Class SVM**

### 4️⃣ Evaluation
- Reveal hidden labels.
- Compute **Precision**, **Recall**, and **F1-score**.
- Assess detection of rare fraud cases.

---

## 🔑 Key Insights

- **Unsupervised models (SVM, Autoencoder):** Very high recall (caught most frauds) but generated many false positives.  
- **Isolation Forest:** More balanced detection but missed some frauds.  
- **Logistic Regression (baseline):** Best compromise (~92% recall), though precision remained low.  

> Fraud detection is always a trade-off between **recall** (catching all frauds) and **precision** (avoiding false alarms).

---

## 📌 Learning Outcomes

- Understand how **unsupervised models** detect rare events.  
- Gain experience handling **imbalanced datasets**.  
- Learn to validate unsupervised model results using **hidden labels**.

