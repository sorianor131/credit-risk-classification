# credit-risk-classification
Module 20 Homework Assignment - Supervised Learning Challenge

## Overview of the Analysis

The objective of this study is to employ machine learning techniques for forecasting credit risk in the context of peer-to-peer lending. The lending dataset provided encompasses various features such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and loan status. The primary aim is to build a model that can identify the creditworthiness of borrowers.

The dataset comprises information on 75,036 healthy loans and 2,500 high-risk loans. To conduct the analysis, the dataset underwent an initial split into training and testing sets. Subsequently, a logistic regression model was instantiated and fit by using the training data. Predictions were than made for the testing data labels by using the testing feature data and the fitted model.

Finally, the model's performance was to be evaluated by generating a confusion matrix and print the classification report.

## Results

* Machine Learning Model 1:
    * Model 1 predicted healthy loans 100% of the time and predicted non-healthy loans 85% of the time. It had an accuracy score of 95%. 
    ![Model 1](Resources/Model%201%20Classification%20Report.png)

   * The model has excellent performance in predicting healthy loans (0), with high precision, recall, and F1-score.

    * For high-risk loans (1), the model performs well with good recall but has a slightly lower precision, leading to a slightly lower F1-score.

Overall, Model 1 demonstrates strong predictive capabilities for both healthy and high-risk loans, with particularly impressive performance for healthy loans.

* Machine Learning Model 2:
    * Model 2 predicted healthy loans 100% of the time and predicted non-healthy loans 84% of the time. It had an accuracy score of 99%.
    ![Model 2](Resources/Model%202%20Classification%20Report.png)

    * The model has excellent performance in predicting healthy loans (0), with high precision, recall, and F1-score.

    * For high-risk loans (1), the model demonstrates strong recall and reasonably good precision, resulting in a high F1-score.

Overall, Model 2 demonstrates strong predictive capabilities for both healthy and high-risk loans, with impressive performance across key metrics.

## Summary

Both models exhibit robust performance in predicting healthy loans. Notably, the second model, leveraging resampled data, demonstrates substantial enhancements in accuracy and recall, achieving nearly perfect scores.

The choice between precision and recall depends on the specific goals and requirements of the application. If the goal is to minimize false positives (misclassifying healthy loans as high-risk is costly), Model 1 with higher precision might be preferred. If the goal is to minimize false negatives (missing high-risk loans is costly), Model 2 with higher recall might be preferred.

My recommendation is to favor Model 2. Given that both models accurately predict healthy loans, prioritizing a model that excels in correctly classifying high-risk loans is prudent. The potential consequences of misclassifying a healthy loan as high-risk are deemed lower than the risks associated with failing to identify a high-risk loan.

# References

* [RandomOverSampler](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.RandomOverSampler.html#imblearn.over_sampling.RandomOverSampler)
