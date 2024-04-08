# Pima Indian Diabetes Analysis

This project utilizes different ML model to model the "Pima Indians Diabetes" dataset, aiming to predict individuals likely to develop diabetes. The dataset originates from the National Institute of Diabetes and Digestive and Kidney Diseases and contains diagnostic measurements used to predict the presence of diabetes in patients. Notably, all patients in the dataset are females aged at least 21 years old of Pima Indian heritage.

## Objective

The primary objective of this analysis is to develop a logistic regression model capable of accurately predicting the likelihood of diabetes based on diagnostic measurements. 
Determine the key factor contributiing 
Key evaluation metrics include Accuracy, Recall, Precision, and F1-score.

## Data Description


The dataset includes 768 entries with the following features:
- Preg: Number of times pregnant
- Plas: Glucose concentration 2 hours after an oral glucose tolerance test
- Pres: Blood pressure (mm Hg)
- Skin: Skin fold thickness (mm)
- Test: 2-Hour serum insulin (mu U/ml)
- Mass: Body mass index (BMI)
- Pedi: Pedigree function
- Age: Age (years)
- Class: Binary variable indicating diabetes status (0 or 1)

## Approach

The project follows these steps:
1. Data Pre-processing: Treat hidden missing values and handle zero values appropriately.
2. Data Splitting: Utilize 80% of the data for training and 20% for testing.
3. Modeling: Employ logistic regression, Random forest, Decision three and gradient boost model to build the predictive model.
4. Model Evaluation: Assess model performance using Accuracy, Recall, Precision, and F1-score.

## Results

### Logistic Regression Model

The initial logistic regression model yielded the following performance metrics:
- Accuracy: 77.27%
- Recall: 51.85%
- Precision: 75.68%
- F1-score: 61.54%

### Model Improvement

Several strategies were employed to enhance model performance:
1. Threshold Adjustment: Modifying the classification threshold from 0.5 to 0.8 and 0.8 to 0.2 improved specific performance metrics.
2. Data Balancing: Implementing Synthetic Minority Over-sampling Technique (SMOTE) to balance the dataset improved recall, precision, and F1-score.
3. Ensemble Modeling: Utilizing Random Forest and Gradient Boosting classifiers improved overall model performance compared to Decision Tree.

### Comparing the performance of the different three based models 

![Performance Evaluation of Three Base Models](https://github.com/adewoleaj/Pima-Indian-Diabetes-Analysis/blob/main/performance%20evaluation%20of%20three%20base%20model.png?raw=true)

Based on these results:

- Random Forest and Gradient Boosting classifiers perform similarly and outperform the Decision Tree classifier in terms of accuracy, precision, recall, and F1-score.

- Random Forest and Gradient Boosting classifiers have higher precision, recall, and F1-score compared to the Decision Tree classifier, indicating their better performance in correctly identifying positive cases while minimizing false positives.

Overall, Random Forest and Gradient Boosting classifiers appear to be more suitable for this classification task compared to the Decision Tree classifier


### Factor contributing to diabetes prediction 

![Factor Contribution](https://github.com/adewoleaj/Pima-Indian-Diabetes-Analysis/blob/main/factor%20contribution.png?raw=true)

it's evident that two factors significantly contribute to the occurrence of diabetes: high blood glucose concentration (plas) and high body (mass) index (BMI). These factors demonstrate a positive correlation with the likelihood of diabetes occurrence, meaning that higher values of blood glucose concentration and BMI are associated with a greater probability of diabetes.


### Final Model

The final Random Forest model achieved an accuracy of approximately 87% and accurately predicted diabetes status in 84 individuals. Notably, the model demonstrated a recall of 93%, indicating its ability to correctly identify individuals with diabetes while minimizing false negatives.

![Final Random Forest Model](https://github.com/adewoleaj/Pima-Indian-Diabetes-Analysis/blob/main/final%20rf.png?raw=true)



## Conclusion

Overall, the developed logistic regression and ensemble models show promising performance in predicting diabetes status based on diagnostic measurements. Adjusting classification thresholds, balancing data, and leveraging ensemble techniques significantly improved model accuracy, recall, precision, and F1-score. This analysis provides valuable insights for diabetes prediction and underscores the importance of data preprocessing and model selection in healthcare analytics.

---

This README provides a comprehensive overview of the Pima Indian Diabetes Analysis project, highlighting the methodology, results, and implications of the analysis.
