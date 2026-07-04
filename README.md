# Breast Cancer Diagnosis using K-Nearest Neighbors Classification
## Project Overview
This project focuses on developing and evaluating a K-Nearest Neighbors (KNN) classifier for the accurate diagnosis of breast cancer. Utilizing the Breast Cancer Wisconsin (Diagnostic) Dataset, the primary goal is to build a robust and interpretable model capable of differentiating between benign and malignant cases. A comparative analysis with Logistic Regression is also performed to benchmark the KNN model's performance.

## Dataset
The Breast Cancer Wisconsin (Diagnostic) Dataset, obtained from sklearn.datasets, contains features computed from digitized images of fine needle aspirate (FNA) of breast masses. Each instance represents characteristics of cell nuclei in the image, classified as either malignant (class 0) or benign (class 1).

## Methodology
## Data Loading and Exploration
The dataset was loaded into a pandas DataFrame. Initial exploration confirmed no missing values and provided insights into the statistical distributions of features.

## Data Splitting
The dataset was split into training (80%) and testing (20%) sets to evaluate model performance on unseen data.
## Feature Scaling
Given KNN's distance-based nature, StandardScaler was applied to standardize features, ensuring all features contribute equally to distance calculations.
## KNN Model Optimization
The optimal k value for the KNN model was determined using 5-fold cross-validation on the training set, testing k values (1, 3, 5, 7, 9, 11). An optimal k of 5 was identified, yielding the highest cross-validation accuracy.
## Model Training and Evaluation (KNN) 
The KNN model was trained with the optimal k on the scaled training data. Its performance was thoroughly evaluated on the scaled test data using:
Accuracy  
Precision, Recall, and F1-score (with 'malignant' as the positive class)
Confusion Matrix
Reeceiver Operating Characteristic (ROC) curve and Area Under the Curve (AUC)
## Comparative Analysis (Logistic Regression): 
A Logistic Regression model was trained and evaluated using the same methodology and metrics to provide a benchmark for KNN's performance.
## Prediction on New Data
The trained knn_optimal model was demonstrated by making predictions on hypothetical new patient data points.
## Key Findings
Both KNN and Logistic Regression models demonstrated strong performance in classifying breast cancer. The KNN model, with an optimal k=5, achieved impressive metrics:

 KNN (k=5):
 Accuracy: 0.9474
 Precision (Malignant): 0.9302
 Recall (Malignant): 0.9302
 F1-Score (Malignant): 0.9302
 AUC: 0.9820

 The Logistic Regression model served as a strong benchmark, showing slightly superior performance across most metrics (e.g., Accuracy: 0.9737, AUC: 0.9974). However, the KNN model, the primary focus of this project, proved to be highly effective and robust, exhibiting a strong ability to correctly identify malignant cases while minimizing false negatives and false positives.

## Conclusion
This project successfully developed a highly effective K-Nearest Neighbors classifier for breast cancer diagnosis. The KNN model demonstrated strong classification capabilities, making it a valuable tool for pattern recognition in this critical medical context.

## Recommendations for Future Work
Explore advanced KNN variations (e.g., weighted KNN, different distance metrics).
Further hyperparameter tuning using techniques like GridSearchCV.
Investigate ensemble methods to potentially enhance model robustness.
Conduct more extensive feature engineering and selection.
Perform robustness testing with varying data conditions.
Validate the model with larger, more diverse clinical datasets for real-world deployment.
