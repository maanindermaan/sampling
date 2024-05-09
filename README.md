# sampling
---

# Credit Card Fraud Detection

This project involves the analysis and prediction of credit card fraud using machine learning algorithms. The dataset used contains transactions made by credit cards, where each transaction is labeled as fraudulent or genuine.

## Dataset

The dataset includes a range of features derived from the original data to maintain confidentiality. The 'Class' column indicates whether a transaction is fraudulent (`1`) or genuine (`0`).

## Data Preprocessing

### Feature Selection
- The 'Time' feature was dropped as it was deemed unnecessary for the analysis.

### Sampling Techniques
To address the class imbalance evident in the dataset, the following resampling techniques were applied:
- **SMOTE (Synthetic Minority Over-sampling Technique)**
- **Random Under Sampling**
- **Random Over Sampling**
- **ADASYN (Adaptive Synthetic Sampling)**

## Models

Multiple machine learning models were trained using both the original and resampled datasets:
- **Random Forest Classifier**
- **K-Nearest Neighbors Classifier**
- **XGBoost Classifier**
- **LightGBM Classifier**
- **Gradient Boosting Classifier**

## Training and Testing

Models were trained on the original dataset as well as on datasets created using different sampling techniques:
1. **Original Dataset**
2. **Upsampled Dataset (using SMOTE)**
3. **Downsampled Dataset (using Random Under Sampling)**

## Results

Model performance was evaluated based on accuracy scores obtained from predictions on the test datasets:
- **Original Dataset**: Best accuracy achieved was ~99.2% using most models.
- **Upsampled Dataset**: Best accuracy achieved was ~99.6% using XGBoost.
- **Downsampled Dataset**: Best accuracy achieved was ~83.3% using XGBoost, Gradient Boosting, and KNN.

## Usage

To run the analysis, ensure you have the necessary libraries installed as listed in the requirements section below. Load the dataset and execute the script.

## Requirements

This project requires the following Python libraries:
- pandas
- numpy
- seaborn
- matplotlib
- imbalanced-learn
- xgboost
- lightgbm
- sklearn

Install these using pip:

```bash
pip install pandas numpy seaborn matplotlib imbalanced-learn xgboost lightgbm scikit-learn
```

## Conclusion

The choice of sampling technique significantly affects model performance, particularly in imbalanced datasets like this one. Further tuning of model parameters and exploration of other features might improve model accuracy and robustness.

---
