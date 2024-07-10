# Credit Card Fraud Detection 💳

## Table of Contents
- [Project Overview](#project-overview)
- [Project Statement](#project-statement)
- [Description](#description)
- [Dataset](#dataset)
- [Approach](#approach)
  - [Data Preprocessing](#data-preprocessing)
  - [Model Training](#model-training)
  - [Combined Prediction](#combined-prediction)
- [Evaluation](#evaluation)
  - [Metrics](#metrics)
  - [Results](#results)
  - [Visualization](#visualization)
- [Files](#files)
- [How to Run](#how-to-run)
- [Dependencies](#dependencies)
- [Future Work](#future-work)
- [Acknowledgments](#acknowledgments)
- [License](#license)

## Project Overview
This project aims to detect fraudulent credit card transactions using machine learning techniques. It combines anomaly detection and classification to identify potentially fraudulent transactions in real-time.

## Project Statement
Detect fraudulent transactions and minimize financial losses for businesses.

## Description
Fraudulent transactions can cost businesses millions. With Python and Scikit-learn, you'll develop a credit card fraud detection system. This project combines anomaly detection and classification to identify potentially fraudulent transactions in real-time.

## Dataset
The dataset used in this project is a highly imbalanced credit card transaction dataset with the following attributes:

- **Time**: Number of seconds elapsed between this transaction and the first transaction in the dataset.
- **V1-V28**: Principal components obtained with PCA.
- **Amount**: Transaction amount.
- **Class**: Target variable (0 for non-fraud, 1 for fraud).

## Approach
### Data Preprocessing
1. Load the dataset.
2. Separate features and target variable.
3. Split the data into training and testing sets.
4. Scale the features using `StandardScaler`.
5. Handle class imbalance using SMOTE (Synthetic Minority Over-sampling Technique).

### Model Training
1. **Anomaly Detection**: 
   - Train an Isolation Forest to identify anomalies.
2. **Classification**: 
   - Train a Logistic Regression model to classify the anomalies detected by the Isolation Forest.

### Combined Prediction
1. Use the Isolation Forest to identify potential fraud cases (anomalies).
2. Apply the Logistic Regression model to the identified anomalies to classify them as fraud or non-fraud.

## Evaluation
### Metrics
- **Accuracy**: Overall correctness of the model.
- **Precision**: Correctness of the positive predictions.
- **Recall**: Ability of the model to identify positive instances.
- **F1 Score**: Harmonic mean of precision and recall.

### Results
- **Accuracy**: 99.51%
- **Precision**: 23.92%
- **Recall**: 84.69%
- **F1 Score**: 37.30%

### Visualization
Confusion matrix visualization provides a clear understanding of the model's performance.

## Files
- `credit_card_fraud_detection.ipynb`: Jupyter notebook containing the code for the project.
- `dataset.csv`: Dataset used for training and testing the model.
- `README.md`: Project description and details.

## How to Run
1. Clone the repository.
   ```bash
   git clone https://github.com/yourusername/credit-card-fraud-detection.git

2. Navigate to the project directory.
   ```bash
   cd credit-card-fraud-detection
  
3. Install the required dependencies.
   ```bash
    pip install -r requirements.txt

4. Run the Jupyter notebook.
   ``` bash
   jupyter notebook credit_card_fraud_detection.ipynb


## Dependencies
- Python 3.x
- Pandas
- Scikit-learn
- Imbalanced-learn
- Matplotlib
- Seaborn
  
## Future Work

- Experiment with different models and ensemble methods.
- Tune model parameters for better performance.
- Implement the model in a real-time detection system.

## Acknowledgments

- Thanks to the authors of the dataset for making it publicly available.
- Inspiration from various online resources and tutorials on credit card fraud detection.

## License
This project is licensed under the MIT License.

