# Module_12_Challenge

---

## Classification of Creditworthiness of Borrowers

---

## Overview of the Analysis

This analysis uses historical lending activity from a peer-to-peer lending service to identify the creditworthiness of borrowers.
The information in the dataframe is predictably imbalanced due to healthy loans outnumbering risky loans.

The data within the database contains the following information: Loan Size, Interest Rate, Borrower Income, Debt to Income, Number of Accounts, Derogatory Marks, Total Debt, and Loan Status.  The Loan Status is reflected as Healthy = 0 and High Risk = 1.

The first portion of the analysis involves a regression model that takes into account imbalanced data to determine the creditworthiness of the borrowers.  The second portion of the analysis uses the same data and applies a RandomOversampler module to balance the data and evaluate the model's accuracey of predictions.

---

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models.

    *Machine Learning Model 1 - trained the original dataset:

        - The model's accuracy was 95%, average precision was 99% and average recall was 99%
        - The precision for healthy loans was 100% and 85% for unhealthy loans
        - The recall for healthy loans was 99% and 91% for unhealthy loans
        
    *Machine Learning Model 2 - trained on the resampled dataset:

        - The model's accuracy was 99%, average percision was 99% and average recall was 99%
        - The precision for healthy loans was 100% and 84% for unhealthy loans
        - The recall for healthy loans was 99% and 99% for unhealthy loans

---

## Summary

With the contrast of the number of healthy loans versus unhealthy loans in the dataset, I would recommend using Machine Learning Model 2.  As you can see, the accuracy improved from 95% in Model 1 to 99% in Model 2 and the f1 score improved from 88% to 91% on the unhealthy loans.  

    !(https://github.com/abolla04/Module_12_Challenge/blob/main/Images/Classification_Report_Imbalanced.png)

    !(Classification_Report_Resampled.png)

---

## Technologies

This analysis leverages Python 3.7 with the following packages:

    Pandas
    Numpy
    Pathlib
    SciKit Learn
    Imbalanced Learn

---

## Installation Guide

Prior to running the analysis, import the following:

    import numpy as np
    import pandas as pd
    from pathlib import Path
    from sklearn.metrics import balanced_accuracy_score
    from sklearn.metrics import confusion_matrix
    from imblearn.metrics import classification_report_imbalanced
    from sklearn.model_selection import train_test_split
    from sklearn.linear_model import LogisticRegression

    import warnings
    warnings.filterwarnings('ignore')

---

## Usage

To observe the model, simply clone the analysis from the repository.

---

## Contributors

This application has been brought to you by Abolla.

---

## License

MIT

---
