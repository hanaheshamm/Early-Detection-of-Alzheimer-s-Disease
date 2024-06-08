# Early-Detection-of-Alzheimer-s-Disease
This project explores the application of machine learning techniques to detect Alzheimer's disease using MRI scan data. The primary focus is on evaluating different algorithms' effectiveness and improving diagnostic accuracy.

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Methods](#methods)
    - [Logistic Regression](#logistic-regression)
    - [Random Forest](#random-forest)
    - [Support Vector Machine](#support-vector-machine)
    - [Decision Tree](#decision-tree)
4. [Preprocessing](#preprocessing)
5. [Experiments and Results](#experiments-and-results)
6. [Conclusion](#conclusion)

## Introduction

Alzheimer's disease (AD) is a progressive neurodegenerative disorder that significantly impacts cognitive function, memory, and behavior. The early detection of Alzheimer's disease is crucial for effective management and treatment. By leveraging machine learning techniques, this project aims to develop a diagnostic tool that can analyze MRI data quickly and accurately.

## Dataset

The dataset used in this project is the OASIS-2 dataset, an open-access series of imaging studies provided by Washington University in St. Louis. The dataset includes MRI and associated clinical data for 150 subjects aged 60 to 96.

### Features

- **EDUC**: Years of Education
- **SES**: Socioeconomic Status
- **MMSE**: Mini Mental State Examination
- **CDR**: Clinical Dementia Rating
- **eTIV**: Estimated Total Intracranial Volume
- **nWBV**: Normalize Whole Brain Volume
- **ASF**: Atlas Scaling Factor

## Methods

### Logistic Regression

Logistic Regression is used for binary classification tasks. The objective is to model the probability that a given input point belongs to a particular class based on one or more independent variables.

### Random Forest

Random Forest is an ensemble method that constructs multiple decision trees during training and outputs the class that is the mode of the classes predicted by individual trees. It effectively reduces the overfitting problem common with decision trees.

### Support Vector Machine

SVM is used for classification and regression analysis. It finds a hyperplane in an N-dimensional space that distinctly classifies the data points.

### Decision Tree

Decision Trees are used for classification and regression tasks. They work by recursively splitting the data into subsets based on the value of input features, creating a tree-like structure of decision rules.

## Preprocessing

1. **Removing Duplicates**: Duplicate entries were removed to prevent redundant data.
2. **Handling Null Values**: Missing values in the "SES" and "MMSE" columns were imputed.
3. **Group Label Adjustment**: The "Converted" label was replaced with "Demented".
4. **Visit Selection**: Only the first visit for each patient was included.
5. **Label Encoding**: Categorical data in the "Group" and "M/F" columns were converted to numerical format.
6. **Dropping Irrelevant Columns**: Columns not relevant to the analysis were removed.
7. **Outlier Removal**: Outliers were identified and removed based on the interquartile range (IQR) method.
8. **Standardization**: Feature data was standardized using the StandardScaler from the sklearn.preprocessing library.

## Experiments and Results

### Evaluation Metrics

- **Accuracy**: Ratio of correctly predicted observations to the total observations.
- **Precision**: Ratio of correctly predicted positive observations to the total predicted positives.
- **Recall (Sensitivity)**: Ratio of correctly predicted positive observations to all observations in the actual class.
- **F1-Score**: Weighted average of Precision and Recall.
- **Confusion Matrix**: A table showing the true positive, true negative, false positive, and false negative counts.

## Conclusion

The results of this study show promising directions for future research in automated Alzheimer's detection. Machine learning algorithms can identify complex patterns and subtle changes in brain structure that may be indicative of AD, providing a more objective and consistent approach to diagnosis.

For more details, please refer to the paper "Early Detection of Alzheimer's Disease" by Habiba Mohsen Ateya, Hana Hesham, Hazem Raafat, and Malak Nasser.
