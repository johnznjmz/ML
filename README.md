# WNS Machine Learning Challenge

# XGBoost model with parameter tuning with bayesian Optimization with 5 Kfolds.
# Things Tried

    Need to do binning of the age features.
    Apply the mean encoding on the feature having text value and frequency more than 3.
    Avg points * no. of comp to get the total points.
    mean encoding or median encoding instead of label.
    normalize or scale and then check the distribution it should be same.
    Use the data imputation technque like(mean,median) for missing values in (education & previous_year_ratings.)
    Add the (awards_won;KpIs_met & previous_year_rating) features,multiply the avg_training_score and no_of_training to get total training score.
    convert education into number's where mtech>btech>other.
    Remove the recruitment_channel that have no effect on the Target result.
    (age - length_of_service) for gettng the joining age.
    GradientBoostingClassifier with parameter tuning
    RandomForestClassifier with parameter tuning
    KNN and LinearRegression , Voting Classifier

# Final Solution Summary

    The missing values in the education is imputed by mode which was the "Bachelor's" & the missing value in the previous_year_rating is imputed by mode . After Correlation matrix analysis,the features like previous_year_rating,length_of_service,KPIs_met have higher correlation with the Target value.
    The count of promotion vs no promotion is unbalanced.
    Pca on the train set and their target values show overlapping decision boundary which can't be separated by the Linear Models.for this tye of overlapping target values Decision Trees are best. Different type of scaling on input features giving different distribution of the target values during Pca.
    XGBoost model with parameter tuning with bayesian Optimization with 8 stratifiedKfolds.

# Newly created Features

    avg_score was a result of avg_mean_score divided by a mean score for the particular region and department.
    recruitment_channel have no impact on the promotion so removed that.
    age of joining by age - years of service

# To try

    Apply the Pca on the input set and get the single column which summarized the input features in the 1 Dimension and used that as a new features.helps to improve the score by 0.5 percent.
    OOF predictions were used for finding the right threshold value.
    kNN imputation, Random Forest imputation , MICE

# What didn't worked

    Linear models and Neural networks gave low scores as compared to the Decision Trees.
    mean encoding of missing values, one hot encoding of categorical values almost gave the same score.
    blindly addition,multiplication and division of features gave low score.
    additional features creation with Variance threshold gave same score.
    Ensembling using Voting Classifier not gave any improvement over the single model.

# Predict Rain or Not
# Initial-Step

Logistic Regression with Python and Scikit-Learn and build a classifier to predict whether or not it will rain tomorrow in Australia. I train a binary classification model using Logistic Regression. I have used the Rain in Australia dataset for this project
