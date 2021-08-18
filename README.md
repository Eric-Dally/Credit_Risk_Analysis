# Overview of the loan prediction risk analysis:

The purpose of this project is test different machine learning models to analyze credit card risk. By importing the imbalanced-learn and scikit-learn libraries, I was able to explore how oversampling, undersampling, SMOTE, SMOTEENN, balanced random forest, and Easy Ensemble AdaBoost models fit the data. Because the data was unbalanced (more low risk data than high risk data), I had to build and evaluate models using resampling. With these machine learning tools I was able to determine whether someone is at high risk of defaulting on their credit card loans. 

# Results:

### RandomOversampler Algorithm:

* Accuracy Score: 0.67
* F-score Avg : 0.75
* Precision Avg: 0.99
* Recall Avg: 0.61
* Accuracy is poor, F-score is poor, Precision is good, and recall is poor.

<img width="737" alt="Screen Shot 2021-08-17 at 7 49 03 PM" src="https://user-images.githubusercontent.com/82424250/129819968-da862794-7015-419b-9f2c-9d1d87d1c3b5.png">

### SMOTE Oversampler Algorithm:

* Accuracy Score: 0.66
* F-score Avg : 0.81
* Precision Avg: 0.99
* Recall Avg: 0.69
* Accuracy is poor, F-score is poor, Precision is good, and recall is poor. However, results are better than the RandomOversampler Algorithm.

<img width="731" alt="Screen Shot 2021-08-17 at 7 49 36 PM" src="https://user-images.githubusercontent.com/82424250/129819972-f34ffd12-0846-4433-b44d-6e5dcf54d56a.png">

### Cluster Centroids Sampling Algorithm:

* Accuracy Score: 0.57
* F-score Avg : 0.73
* Precision Avg: 0.99
* Recall Avg: 0.58
* Accuracy is poor, F-score is poor, Precision is good, and recall is poor. With a recall close to 50 percent, these were the worst. 

<img width="721" alt="Screen Shot 2021-08-17 at 7 50 17 PM" src="https://user-images.githubusercontent.com/82424250/129819981-6fda0acc-e82f-46e1-98c3-44387e868680.png">

### Over and Undersampling using the SMOTEENN Sampling Algorithm:

* Accuracy Score: 0.66
* F-score Avg : 0.81
* Precision Avg: 0.99
* Recall Avg: 0.69
* Accuracy and F-score are improved, but the recall is still to low. 

<img width="722" alt="Screen Shot 2021-08-17 at 7 50 45 PM" src="https://user-images.githubusercontent.com/82424250/129819995-07d69f7f-cee8-426c-9d3c-244e4afb264f.png">

### BalancedRandomForest Ensemble Algorithm:

* Accuracy Score: 0.79
* F-score Avg : 0.93
* Precision Avg: 0.99
* Recall Avg: 0.87
* Accuracy is good, F-score is great, precision is good, and recall is more reliable. 
* total_rec_prncp, total payment, total payment invoice, total_rec_int, last payment amount, and interest rate were the biggest factors contributing to whether the client was considered low/high risk for credit card loans.

<img width="736" alt="Screen Shot 2021-08-17 at 7 52 15 PM" src="https://user-images.githubusercontent.com/82424250/129820003-0cb2c1fb-6319-4ce0-9064-379162db4518.png">

### Easy Ensemble AdaBoost Ensemble Algorithm:

* Accuracy Score: 0.93
* F-score Avg : 0.97
* Precision Avg: 0.99
* Recall Avg: 0.94
* This algorithm had the best results. The 94% recall is by far the highest among all the models. 

<img width="722" alt="Screen Shot 2021-08-17 at 7 58 31 PM" src="https://user-images.githubusercontent.com/82424250/129820016-2df32c2d-0bc9-45af-b7ee-5ad721300c4e.png">


# Summary:

<img width="450" alt="Screen Shot 2021-08-17 at 10 08 34 PM" src="https://user-images.githubusercontent.com/82424250/129830662-b4b9a4b3-54e9-432b-8ed7-9cd7f5e25c47.png">

When evaluating loans precision is the most important metric. I would rather have a slightly less accurate model with higher precision than a more accurate model with lower precision. The reason being, it is better to identify a low risk loan as high risk than identify a high risk loan as low risk (i.e., having a low false positive rate). If a high risk loan is labeled as low risk, the bank will likely lose money. On the contrary, if a low risk loan is labeled as high risk, the bank may annoy their customer but will not risk losing money on a defaulted loan. This is not to say that other metrics are not important as they are still key in comparing different models; however, precision carries more weight in this specific situation. That being said, all the models had the same precision score of 99% forcing me to use different metrics to pick the best model. 

Based on my results, the Easy Ensemble AdaBoost Ensemble Algorithm was the best model. It had the highest Accuracy Score (93%), F-score (97%), precision (99%), and recall 94%. 



There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
