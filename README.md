# Associating measles vaccine uptake classification and its underlying factors using an ensemble of machine learning models

Measles is one of the significant public health issues responsible for the high mortality rate around the globe, especially for developing countries. Using nationally representative demographic and health survey data, measles vaccine utilization has been classified, and its underlying factors are identified through an ensemble Machine Learning (ML) approach. Firstly, missing values are imputed employing various approaches, and then several feature selection techniques have been applied to identify the crucial attributes for predicting measles vaccination. A grid search hyperparameter optimization technique has been applied for tuning the critical hyperparameters of different ML models, such as Naive Bayes, random forest, decision tree, XGboost, and lightgbm. The categorization performance of the individual optimized ML model as all as their ensembles have been reported utilizing our proposed BDHS dataset.  Individually, the optimized lightgbm provides the highest precision and AUC of 79.90% and 77.80%, respectively. This result improved when the optimized lightgbm is ensembled with XGboost, providing the precision and AUC of 84.60% and 80.0%, respectively. Our result reveals that the statistical median imputation technique with the XGboost-based attribute selection method and the lightgbm classifier provides the best individual result. The performance has been improved when the proposed weighted ensemble of the XGboost and lightgbm approach has been adapted with the same preprocessing and recommended for measles vaccine utilization. The significance of our proposed approach is that it utilizes minimum attributes collected from the child and their family members and yielded 80.0% accuracy making it easily explainable by caregivers and healthcare personnel. Finally, our predictive model provides an early detection procedure to help national policymakers enforce new policies with specific rules and regulations.

The complete workflow of the study is given below, where the training dataset is further divided to perform grid search optimization for finding the best hyperparameters of the ML models.

![Block](https://user-images.githubusercontent.com/32570071/127675455-6a7453cf-622a-46c3-8e6e-a6b91ded6c86.png)

Description of the independent attributes (categorical and continuous) utilized in this research is presented in the following table. A Chi-test is used for categorical attributes to describe the significant relationship with the dependent variable measles uptake, whereas the Mean+/-std is used to describe continuous variables. Respondent denotes the mother of the child who is considering vaccine utilization.
| SN |         Attributes         |                       Short Description                      | Chi-Test (P-Value) |
|:--:|:--------------------------:|:------------------------------------------------------------:|--------------------|
| 1  | Division (A1)              | On which division the respondents’ lives?                    | 12.076 (0.098)     |
| 2  | Residence place (A2)       | Respondents’ living place (Urban/Rural)                      | 0.170 (0.68)       |
| 3  | Respondent education (A3)  | Respondent’s current education status                        | 24.827 (0.000)     |
| 4  | Religion (A4)              | Religion of the respondent                                   | 5.857 (0.118)      |
| 5  | Reading newspaper (A5)     | Frequency of reading newspaper of the respondent per week    | 7.342 (0.025)      |
| 6  | Listening radio (A6)       | Frequency of listening radio of the respondent per week      | 3.375 (0.185)      |
| 7  | Watching television (A7)   | Frequency of watching television of the respondent per week  | 23.916 (0.000)     |
| 8  | Wealth index (A8)          | Economic status of the respondent                            | 21.377 (0.000)     |
| 9  | Husband Education (A9)     | Respondent’s husband’s education                             | 8.536 (0.074)      |
| 10 | Working (A10)              | Current working status of the respondent                     | 39.905 (0.000)     |
| 11 | Sex of child (A11)         | Sex of the child who are taking the vaccine                  | 0.135 (0.713)      |
| 12 | Household head sex (A12)   | Sex of the household head                                    | 0.188 (0.664)      |
|    |                            |                                                              |    Mean +/- Std    |
| 13 | Respondent age (A13)       | Respondent’s current age                                     | 24.951 +/- 5.541   |
| 14 | Household members  (A14)   | Total household member                                       | 6.120 +/- 2.695    |
| 15 | Household head age (A15)   | Current age of the household head                            | 43.038 +/- 15.128  |
| 16 | Children ever born (A16)   | Total children ever born on that household                   | 2.117 +/- 1.250    |
| 17 | First birth age (A17)      | Respondent’s age at first birth                              | 18.629 +/- 3.259   |
| 18 | Birth order (A18)          | Birth order of the respondent                                | 2.117 +/- 1.250    |
| 19 | Antenatal visits (A19)     | Total number of Antenatal care visit during pregnancy period | 3.939 +/- 2.878    |
