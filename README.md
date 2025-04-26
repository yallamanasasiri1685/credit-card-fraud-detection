# 💳 Credit Card Fraud Detection

**Author:** Yalla Manasa Siri - 3rd Year Engineering Student  
**Repository:** credit-card-fraud-detection

## 🎯 Task Objectives

- Build a Machine Learning model to distinguish fraudulent (`is_fraud = 1`) and legitimate (`is_fraud = 0`) credit card transactions.  
- Preprocess raw transaction data (timestamps, categorical encoding, feature scaling).  
- Train and tune a Random Forest classifier (with optional XGBoost) to maximize fraud detection accuracy while minimizing false positives.  
- Evaluate model performance using precision, recall, F1-score, ROC-AUC, and precision-recall curves.  
- Explain misclassifications by identifying false positives and false negatives.  
- Compute feature importance to interpret model decisions.  
- Support new data prediction: upload a new test file and output fraud predictions.  

## 📁 Repository Structure

```
credit-card-fraud-detection/
├── fraudTrain.csv               # Training dataset
├── fraudTest.csv                # Example test dataset (for prediction)
├── src/
│   └── fraud_detection.py       # Main Python script with preprocessing, training, evaluation, and prediction functions
├── notebooks/
│   └── Fraud_Detection.ipynb    # Jupyter notebook version of the analysis and code
├── outputs/
│   ├── models/                  # Saved model artifacts (.pkl files)
│   └── figures/                 # Evaluation plots and charts
├── requirements.txt             # Python dependencies
└── README.md                    # Project overview and instructions
```

## 🧰 Prerequisites

- Python 3.7+  
- Libraries listed in `requirements.txt`  

Install dependencies using:

```
pip install -r requirements.txt
```

- Make sure `fraudTrain.csv` and `fraudTest.csv` are placed in the root directory.

## 🚀 Steps to Run the Project

### 1. Clone the Repository

```
git clone https://github.com/yourusername/credit-card-fraud-detection.git
cd credit-card-fraud-detection
```

### 2. Install Required Libraries

```
pip install -r requirements.txt
```

### 3. Run the Main Python Script

Make sure the file paths in `src/fraud_detection.py` are correct.  
Run:

```
python src/fraud_detection.py
```

This script will:

- Load and preprocess `fraudTrain.csv`
- Train and evaluate the fraud detection model
- Save results and display evaluation metrics
- Prepare for predictions on new data

## 🔍 Predict on New Test Data

1. Place `fraudTest.csv` in the root directory.  
2. Use the following Python snippet in a script or notebook:

```python
from src.fraud_detection import predict_on_new_data

results_df = predict_on_new_data("fraudTest.csv")
print(results_df.head())
```

This will return a DataFrame including the column `fraud_prediction`.

## 📊 Review Outputs

- Models saved in: `outputs/models/`  
- Evaluation plots (ROC, PR Curve, etc.) saved in: `outputs/figures/`

## 🧹 Code Quality

- ✅ Well-structured: Modular functions for preprocessing, training, evaluation, and prediction  
- ✅ Well-commented: Code sections include explanations  
- ✅ Reproducible: Fixed random seed, clear data splits, and artifact saving  

## 🔧 Future Enhancements

- Try different ML models like XGBoost, LightGBM  
- Use class balancing techniques (SMOTE, class weights)  
- Build a web UI with Streamlit to upload and test new files  
- Add logging, configuration, and packaging for deployment 
