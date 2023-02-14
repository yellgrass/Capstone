# Capstone

Link to notebook: https://github.com/yellgrass/Capstone/blob/main/Capstone%20.ipynb

Findings Summary:

Due to the format of the data, I initially selected a subset of features that appeared to be relevant to the survival months. After processing the data, representing all the features numerically, the data to various models, including Logistic Regresssion, K nearest neighbors, decision tree and SVC and comparing the model accuracies to determine which would best fit the data. Although no model was a truly good fit for the data, the best were KNN and Decision Tree. As neither of these were particularly high, I used permutation importance to determine which features had the greatest impact on the KNN model, and found that none of them had a tremendous effect. After running grid search on these two models to find best parameters, and found that the best score for these was still very low. As such, I began again with different features from the site and repeated the process. This time I also used Linear Regression with some polynomial features, and was still unable to get a very high train or test score. However, I did find that primary site of surgery appeared to have a fairly impact and whether or not number of tumors exceeded 989 appeared to play fairly influential roles in number of months survived.

Overall, I found that a first degree linear regression model performed the best, and surgery site and tumor number were the most influential features in determining how long patients survived.
