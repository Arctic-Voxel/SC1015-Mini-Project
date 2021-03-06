# SC1015 Mini Project - Identifying factors relating to Heart Disease

## About

This is a Mini Project for SC1015 (Introduction to Data Science and Artificial Intelligence) which focuses on factors relating to Heart Disease. The heart disease dataset is originally generated by the [Centers for Disesase Control and Prevention US (CDC)](https://www.cdc.gov/brfss/annual_data/annual_2020.html). The dataset was then cleaned and published into a CSV file on [Kaggle](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease?select=heart_2020_cleaned.csv).

## Contributors

- Samuel Ong Jing Siang @sojs-coding
- Ong Jun Heng @Miizy
- Leong Jun Yi @Arctic-Voxel

## Problem Definition

Based on the dataset are we able to predict heart disease based on certain health attributes?
Which factors would be most effective in predicting heart disease?

## Tools Used

As our dataset is highly Categorical, we used two preprocessing tools such as the OrdinalEncoder and the LabelEncoder to prepare our train and test.

The categorical predictors in our train and test would be transformed into numerical categories beginning from 0 such as 0 and 1 for Binary Predictors which helps the model to better predict the classification of Heart Disease.

Afterwards, we used the SelectKBest tool that is capable of selecting features according to the k highest scores using the Chi function. This helps us to find the features that are the highly like to be irrelevant for classification.

## Models Used

Logistic Regression - Models the probability of a discrete outcome, in our case binary (Yes / No to Heart Disease)

## Conclusion

Based on the correlation we calculated, we removed the variables that did not contribute to the model whilst recording the model accuracy. These variables include 'Mental Health', 'Sleep Time', 'BMI', 'Physical Activity' and 'General Health'. Though 'Race' had a low correlation, when removed from the model, the accuracy had a considerable deprovement, as such we decided to keep it in the model. Through this, we can see that variables such as 'Physical Health' and 'Age Category' are good predictors for Heart Disease.

One important fact gained from this, is that age is a very important factor in predicting Heart Disease as we can see an obvious relation in the Heart Disease - Age Category Graph, and the results gained from our correlation and the model further supports this.

We are able to predict the possibility of a Heart Disease with an accuracy of around 76% with fewer predictors at the end.

## Learning points

1. Representing minority data through log scale
2. Upsampling to prevent statiscal bias when there is an imbalance in the number of entries for each variable
3. Methods of finding correlation against a binary variable (HeartDisease)
  - Tetrachoric Correlation (Binary to Binary)
  - Spearman's Rank Order Correlation (Ordinal to Binary)
  - Cramer's V (Nominal to Binary)
 4. Selection Technique (Chi-Squared Statistics)

## References

- <https://www.statology.org/correlation-between-categorical-variables/>
- <https://statistics.laerd.com/statistical-guides/spearmans-rank-order-correlation-statistical-guide.php>
- <https://machinelearningmastery.com/feature-selection-with-categorical-data/>
