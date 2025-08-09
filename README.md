# IEEE-CIS Fraud Detection

Predict the probability that an online transaction is fraudulent using real-world e-commerce transaction data from **Vesta Corporation** in collaboration with the **IEEE Computational Intelligence Society (IEEE-CIS)**.

## 📜 Project Description
Imagine standing at the check-out counter with a long line behind you, and the cashier announces that your card has been declined. Moments later, your bank sends a message:  
> "Press 1 if you really tried to spend $500 on cheddar cheese."

While perhaps inconvenient (and sometimes embarrassing), fraud prevention systems like this save consumers millions of dollars every year. This competition aims to improve fraud detection accuracy, reducing false positives and minimizing losses for businesses.

The dataset used in this competition is provided by **Vesta Corporation**, a global leader in guaranteed e-commerce payment solutions, processing over **$18B** in transactions annually. The challenge is to build a machine learning model to predict whether a given online transaction is fraudulent (`isFraud`).

---

## 📂 Dataset Description
The dataset is split into **two main files**:

- **Transaction data** (`train_transaction.csv`, `test_transaction.csv`)
- **Identity data** (`train_identity.csv`, `test_identity.csv`)

These can be merged using the `TransactionID` key.  
Not all transactions have corresponding identity information.

### Target Variable
- `isFraud`:  
  - `1` → Fraudulent transaction  
  - `0` → Non-fraudulent transaction  

### Categorical Features
**Transaction Table**
- `ProductCD`
- `card1` – `card6`
- `addr1`, `addr2`
- `P_emaildomain`, `R_emaildomain`
- `M1` – `M9`

**Identity Table**
- `DeviceType`
- `DeviceInfo`
- `id_12` – `id_38`

**Special Feature**
- `TransactionDT`: timedelta from a reference datetime (not an actual timestamp)

---

## 📁 Files in Repository
- `train_transaction.csv` → Training transaction-level data
- `train_identity.csv` → Training identity-level data
- `test_transaction.csv` → Test transaction-level data
- `test_identity.csv` → Test identity-level data
- `sample_submission.csv` → Sample prediction file format

---

## 🎯 Project Goals
- Build a high-performing fraud detection model.
- Explore various ML techniques including feature engineering, feature selection, and ensemble models.
- Reduce false positives while maintaining high fraud detection rates.

---
