# Homesite-Quote-Conversion <br>
Predicting whether customers will purchase a given quote from Homesite.
![image](https://user-images.githubusercontent.com/112804900/198905803-57a4617d-176a-4003-8658-24b3aee554fa.png)

## Background <br>
This dataset represents the activity of a large number of customers who are interested in buying policies from Homesite. Each QuoteNumber corresponds to a potential customer and the QuoteConversion_Flag indicates whether the customer purchased a policy. <br>
The provided features are anonymized and provide a rich representation of the prospective customer and policy. They include specific coverage information, sales information, personal information, property information, and geographic information. Your task is to predict QuoteConversion_Flag for each QuoteNumber in the test set.

### Accuracy Comparison (using train_test_split on Train_df)
#### Individual Modes and Stacked Model

|S No.| Model Name | Type of Model | SMOTE strategy | HyperParameter Tuning | Accuracy  |
|:-:| :---- | :---: | :---: |:---: |:---: |
|1.| Decision Tree M1 | Individual |1|None| 0.87 |
|2.| Random Forest Classifier M2 | Individual |1|None| 0.89 |
|3.| LinearSVC Classifier M3 | Individual |1|None| 0.34 |
|4.| KNeighborsClassifier M4 | Individual |1|None| 0.57 |
|5.| MLP Classifier M5 | Individual |1|None| 0.80 |
| | | | | | |
|6.| **RandomForestClassifier** | **Stacked** |**1**|**None**| **0.89** |

### Kaggle Score Comparison

| Model Name | Type of Model |SMOTE strategy|HyperParameter Tuning| Kaggle Score |
| :---: | :---: | :---: |:---: |:---: |
| Decision Tree M6 | Individual | 1 |RandomizedSearchCV| 0.90 |
| Random Forest M7 | Individual | 1 |RandomizedSearchCV| 0.94 |
| Linear SVC M8 | Individual | 1 |RandomizedSearchCV| 0.64 |
| KNN Classifier M9 | Individual |1|RandomizedSearchCV| 0.50 |
| MLP Classifier M10 | Individual |1|RandomizedSearchCV| 0.68 |
| | | | |
| **Decision Tree** | Stacked |1|RandomizedSearchCV| 0.85 |
| **Random Forest** | Stacked |1|RandomizedSearchCV| 0.85 |

## Note
Main Testcode : HomesiteQuoteConversion.ipynb <br>
Datasets available in Data folder <br>
