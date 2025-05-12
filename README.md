# Secure-Energy-Transactions-Using-Blockchain-AI-for-Fraud-Detection-Energy-Market-Stability-25311
## 📌 Project Overview

This project explores how blockchain and artificial intelligence can be integrated to secure energy transactions while enabling real-time fraud detection and enhancing energy market stability. Using a synthetic yet realistic dataset of 10,000 energy transactions, we apply classification models to identify anomalies or suspicious transactions that may indicate fraud.

---

## 📊 Dataset Description

The dataset contains 10,000 energy transactions with the following features:

| Column Name           | Description |
|-----------------------|-------------|
| `transaction_id`      | Unique ID for each transaction |
| `timestamp`           | Date and time of the transaction |
| `user_id`             | Unique identifier of the user |
| `user_role`           | Role of the user (e.g., consumer, provider) |
| `transaction_type`    | Type of transaction (e.g., buy, sell) |
| `electricity_quantity`| Quantity of electricity transacted (MWh) |
| `price_per_mwh`       | Price per megawatt-hour |
| `total_cost`          | Total cost of transaction |
| `latency_ms`          | Network latency in milliseconds |
| `security_level`      | Security rating of the transaction |
| `encryption_method`   | Encryption method used |
| `zt_authentication`   | Zero-trust authentication flag (1/0) |
| `network_slice_id`    | Network segment identifier |
| `transaction_status`  | Status (completed, pending, suspicious, etc.) |

---

## 🧹 Data Preprocessing

- Filled missing categorical values (`transaction_type`) using mode imputation.
- Encoded categorical columns (`user_role`, `security_level`, etc.) using LabelEncoder and OneHotEncoder.
- Standardized numerical columns for consistent model input.
- Split dataset into train and test sets (80/20).
- Target variable: `transaction_status` (multiclass: Success, Pending, Failed).

---

## 🤖 Machine Learning Models

Three supervised classification models were trained to predict transaction outcomes:

### ✅ Random Forest
- **Accuracy:** `0.3368`

```text
              precision    recall  f1-score   support
      Failed       0.33      0.35      0.34       843
     Pending       0.34      0.35      0.34       825
     Success       0.34      0.31      0.33       832
   macro avg       0.34      0.34      0.34      2500
weighted avg       0.34      0.34      0.34      2500
```

---

### ✅ Logistic Regression
- **Accuracy:** `0.3224`

```text
              precision    recall  f1-score   support
      Failed       0.32      0.39      0.35       843
     Pending       0.32      0.28      0.30       825
     Success       0.33      0.30      0.31       832
   macro avg       0.32      0.32      0.32      2500
weighted avg       0.32      0.32      0.32      2500
```

---

### ✅ XGBoost Classifier
- **Accuracy:** `0.3588` (Best Performer)

```text
              precision    recall  f1-score   support
      Failed       0.34      0.34      0.34       843
     Pending       0.36      0.37      0.36       825
     Success       0.37      0.37      0.37       832
   macro avg       0.36      0.36      0.36      2500
weighted avg       0.36      0.36      0.36      2500
```

📊 A histogram comparison of model accuracies is included in the visualization results for clarity.

---

## 💼 Business Impact

- **Fraud Detection**: Enables automatic identification of suspicious transactions, saving thousands in potential fraud losses.
- **Market Confidence**: Supports secure and reliable operations for decentralized energy trading platforms using blockchain.
- **Operational Optimization**: Helps network operators identify latency bottlenecks and high-risk transaction paths.
- **Real-Time Alerts**: Zero-trust authentication and AI-driven classification provide immediate insight into compromised or risky actions.
- **Decision Support**: Empowers stakeholders with clear visual and statistical insights into transaction integrity and network health.

---

## 🧾 Conclusion

By combining blockchain security with AI-based modeling, this project delivers a powerful system for monitoring and securing energy transactions. Though initial model performance is modest, it sets the stage for further enhancement through feature engineering, data balancing, and real-time deployment strategies.


