### Prediction of Survival Time of Cancer Patients

**Timothy Yeh**

#### Executive summary
Cancer is prevalent in our daily lives, with most people either having or knowing someone that has cancer in their lives. Despite widespread awareness, the myriad of different types resulting from the nature of the disease make it incredibly difficult to treat and resulting in hundreds of thousands of cancer deaths in the United States yearly. 

The objective of this task will be to determine what types of cancer patients succumb more quickly to cancer, and what aspects of the cancer may be more indicative of this. To do so, this task will model various features of patients with cancer and attempt to predict patient survival months, comparing models to determine which features are most influential in predicting patient survival time in an attempt to elucidate important factors to either identifying dangerous cancers or best methods for treatment.

#### Rationale
This study will give an insight into what features of patients result in either a higher or lower survival time, potentially indicating what aspects of cancer are more dangerous or what treatments are most effective. This type of study could help guide future research into cancer research or patient prioritization. 

#### Research Question
How well can patient survival be determined by features of patients with cancer and their treatments?

#### Data Sources
SEER Registry Data (https://seer.cancer.gov/)

#### Methodology
In order to model and fit the data, techniques such as via Linear Regression, with methods to process the data by encoding categories numerically via OneHotEncoder or OrdinalEncoder, as well as expand the data via PolynomialFeatures. In addition, data visualization such as barplots from Seaborn will be used to compare models for predicting survival time.

#### Results
Due to the format of the data, I initially selected a subset of features that appeared to be relevant to the survival months. After processing the data, representing all the features numerically, I fit the data to various models. These models included Logistic Regresssion, K nearest neighbors, decision tree and SVC. The best model was selected by comparing the overall mean square error resulting from model predictions to determine which would most closely fit the data. Although no model was a truly good fit for the data, the best were KNN and Decision Tree. As neither of these were performed particularly well in terms of either accuracy or error, I used permutation importance to determine which features had the greatest impact on the KNN model, and found that none of them had a tremendous effect. After running grid search on these two models to find best parameters, I found that the best score for these was still very low. As such, I began again with different features from the site and repeated the process. This time I also used Linear Regression with some polynomial features, and was still unable to get a very high train or test score. However, I did find that primary site of surgery appeared to have a fairly high impact and whether or not number of tumors exceeded 989 appeared to play fairly influential roles in number of months survived.

Overall, I found that a first degree linear regression model performed the best, and surgery site and tumor number were the most influential features in determining how long patients survived.

#### Outline of project

https://github.com/yellgrass/Capstone/blob/main/Capstone%20.ipynb

##### Contact and Further Information
timmyyeh@gmail.com
