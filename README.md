# Credit Card Fraud Detection

## Overview
This project focuses on detecting fraudulent credit card transactions using machine learning techniques. The dataset used is highly imbalanced, making it an excellent case for exploring techniques like Synthetic Minority Over-sampling Technique (SMOTE) to balance classes and enhance model performance.

## Dataset
The dataset contains transaction records, with features including:
- **Time**: Elapsed time since the first transaction
- **V1 to V28**: Principal components obtained using PCA
- **Amount**: Transaction amount
- **Class**: Target variable (0 for non-fraudulent, 1 for fraudulent)

The dataset includes 284,807 transactions, of which only a small fraction are fraudulent.

## Methodology
### Preprocessing
- **Feature Scaling**: Min-max scaling to normalize features.
- **SMOTE**: Used to address class imbalance by generating synthetic samples of the minority class.

### Model Training
1. **Naive Bayes Classifier**: A probabilistic model used for baseline performance.
2. **Random Forest Classifier**: An ensemble learning method used to achieve higher accuracy and robustness.

### Model Evaluation
Models were evaluated using:
- **Precision, Recall, and F1-Score**: To understand the balance between false positives and false negatives.
- **Accuracy**: Overall correctness of the model predictions.

### Performance Highlights
- **Naive Bayes Classifier**:
  - Precision: ~79% for non-fraudulent transactions.
  - Recall: ~99% for non-fraudulent transactions.
  - F1-Score: ~86% overall.
- **Random Forest Classifier**:
  - Achieved near-perfect precision and recall on the balanced dataset.
  - Total training time: ~352 seconds.

## Results
The Random Forest Classifier significantly outperformed the baseline model, achieving an overall accuracy of 100% on the test dataset after applying SMOTE.

## Tools and Libraries
- **Python**
- **Pandas, NumPy**: Data manipulation and analysis
- **scikit-learn**: Machine learning models and SMOTE

## How to Use
1. Clone the repository.
2. Run the Jupyter Notebook to explore the data, preprocess it, and train models.
3. Adjust model parameters in the notebook for further experimentation.

## Future Work
- Implement additional algorithms like Gradient Boosting Machines (XGBoost, LightGBM) for comparative analysis.
- Explore real-time fraud detection using streaming data.