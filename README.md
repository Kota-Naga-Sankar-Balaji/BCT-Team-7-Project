🚀 AI-Powered Detection of Fraudulent Cryptocurrency Transactions
📌 Overview
This project applies "Machine Learning (ML) techniques" to detect fraudulent cryptocurrency transactions using the "Elliptic dataset". By classifying transactions as "licit" or "illicit", 
the model supports "blockchain security" and "anti-money laundering (AML)" efforts.
The implementation is done in "Python on Google Colab" and includes baseline models ("Random Forest" and "XGBoost") with evaluation metrics and visualizations.

🎯 Aim

To build an AI-based model that detects fraudulent cryptocurrency transactions by analyzing transaction-level features and classifying them into licit or illicit categories.

📂 Dataset

* Source: [Elliptic Dataset (Kaggle)](https://www.kaggle.com/datasets/ellipticco/elliptic-data-set)
* Files Used:

  * `elliptic_txs_features.csv` → Transaction features
  * `elliptic_txs_classes.csv` → Labels (licit/illicit/unknown)
  * `elliptic_txs_edgelist.csv` → Graph edges between transactions
* Size:\~203K transactions (\~46K labeled)

⚙️ Methodology

1. Data Loading & Preprocessing

   * Merge features with class labels
   * Remove unknown transactions
   * Normalize features using `StandardScaler`

2. Train/Test Splitting

   * Time-based split (train: timesteps 0–33, test: 34–49)

3. Class Imbalance Handling

   * Applied **SMOTE** to balance licit and illicit transactions

4. Model Training

   * Random Forest Classifier
   * XGBoost Classifier

5. Evaluation

   * Metrics: Accuracy, Precision, Recall, F1-Score, ROC-AUC
   * Confusion Matrix & ROC Curves
   * 
📊 Results

<img width="838" height="179" alt="image" src="https://github.com/user-attachments/assets/88f27ab6-d1d7-47cd-8cfc-17a6006c2396" />

* Random Forest achieved **higher recall**, detecting more fraud cases.
* XGBoost achieved **better precision**, reducing false positives.
🚀 How to Run

1. Clone this repository

```bash
git clone https://github.com/your-username/fraudulent-crypto-detection.git
cd fraudulent-crypto-detection
```

2. Open in Google Colab

* Upload the notebook file (`fraud_detection.ipynb`)
* Upload dataset CSVs (from Kaggle) or configure Kaggle API

3. Install dependencies

```bash
!pip install xgboost imbalanced-learn scikit-learn pandas matplotlib seaborn
```

4. Run the Notebook

Execute cells step by step to:

* Load and preprocess data
* Train ML models
* Evaluate fraud detection results

🔮 Future Enhancements

* Use "Graph Neural Networks (GCN, GAT)" to exploit transaction graph topology
* Apply "temporal models" (LSTMs, Temporal GNNs) for evolving fraud detection
* Integrate "Explainability tools (SHAP, LIME)" for interpretability
* Build a "real-time fraud detection dashboard"

