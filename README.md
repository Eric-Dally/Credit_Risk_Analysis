# Overview of the loan prediction risk analysis:

The purpose of this project is test different machine learning models to analyze credit card risk. By importing the imbalanced-learn and scikit-learn libraries, I was able to explore how oversampling, undersampling, SMOTE, SMOTEENN, balanced random forest, and Easy Ensemble AdaBoost models fit the data. Because the data was unbalanced (more low risk data than high risk data), I had to build and evaluate models using resampling. With these machine learning tools I was able to determine whether someone is at high risk of defaulting on their credit card loans. 

# Results:

### RandomOversampler Algorithm:

* Worst results
* Accuracy Score : 0.5295 -- the worst
* Did a slightly better than 50% for credit risk prediction
* F-score
    Avg : 0.56
* high-risk prediction : 0.01 -- very poor

<img width="737" alt="Screen Shot 2021-08-17 at 7 49 03 PM" src="https://user-images.githubusercontent.com/82424250/129819968-da862794-7015-419b-9f2c-9d1d87d1c3b5.png">

### SMOTE Oversampler Algorithm:

<img width="731" alt="Screen Shot 2021-08-17 at 7 49 36 PM" src="https://user-images.githubusercontent.com/82424250/129819972-f34ffd12-0846-4433-b44d-6e5dcf54d56a.png">

### Cluster Centroids Sampling Algorithm:

<img width="721" alt="Screen Shot 2021-08-17 at 7 50 17 PM" src="https://user-images.githubusercontent.com/82424250/129819981-6fda0acc-e82f-46e1-98c3-44387e868680.png">

### Over and Undersampling using the SMOTEENN Sampling Algorithm:

<img width="722" alt="Screen Shot 2021-08-17 at 7 50 45 PM" src="https://user-images.githubusercontent.com/82424250/129819995-07d69f7f-cee8-426c-9d3c-244e4afb264f.png">

### BalancedRandomForest Ensemble Algorithm:

<img width="736" alt="Screen Shot 2021-08-17 at 7 52 15 PM" src="https://user-images.githubusercontent.com/82424250/129820003-0cb2c1fb-6319-4ce0-9064-379162db4518.png">

### Easy Ensemble AdaBoost Ensemble Algorithm:

<img width="722" alt="Screen Shot 2021-08-17 at 7 58 31 PM" src="https://user-images.githubusercontent.com/82424250/129820016-2df32c2d-0bc9-45af-b7ee-5ad721300c4e.png">


# Summary:

There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
