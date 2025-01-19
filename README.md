EXAMPLE INPUT  :  0.0,0.1,0.2,...,22.0

# Fraud Detection System Using Random Forest

This project demonstrates a fraud detection system using the **Credit Card Fraud Detection Dataset**. The dataset contains highly imbalanced data, with most transactions being non-fraudulent. To address this, the model uses **SMOTE (Synthetic Minority Oversampling Technique)** to handle the imbalance and trains a **Random Forest Classifier** for classification.

---

## Dataset

The dataset used is the **Credit Card Fraud Detection Dataset**:
- It has 284,807 transactions, where:
  - Class `0` = Non-fraudulent transactions.
  - Class `1` = Fraudulent transactions.

---

## Steps Performed

### 1. Data Preprocessing
- The dataset is read using `pandas`, and the `Class` column is identified as the target variable.
- **Train-Test Split**: The data is split into training (70%) and testing (30%) sets, ensuring stratified sampling to preserve the class distribution.

### 2. Handling Class Imbalance
- The dataset is highly imbalanced, with fraudulent transactions making up only a small fraction.
- **SMOTE** is applied to oversample the minority class (fraudulent transactions) in the training set.

### 3. Model Training
- A **Random Forest Classifier** with 100 estimators is trained on the balanced dataset.

### 4. Model Evaluation
- The model is evaluated on the test set using:
  - **Confusion Matrix**
  - **Classification Report** (Precision, Recall, F1-Score)

### 5. Fraud Detection Interface
- A simple command-line interface allows users to test individual transactions by entering their feature values.

---

## Installation and Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/fraud-detection-system.git
   cd fraud-detection-system


•	Model Performance:
o	Precision: 1.00 for non-fraudulent and 0.88 for fraudulent transactions.
o	Recall: 1.00 for non-fraudulent and 0.80 for fraudulent transactions.
o	F1-Score: 1.00 for non-fraudulent and 0.84 for fraudulent transactions.
o	Accuracy: ~100% on the test set.
•	The model performs exceptionally well for non-fraudulent transactions, but there is a slight drop in recall for fraudulent transactions due to their low frequency in the dataset.
•	Challenges:
o	The imbalance in the dataset is a significant challenge, addressed by SMOTE.
o	Real-world systems may require periodic retraining to adapt to new patterns in fraud.

