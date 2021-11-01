# Neural_Network_Charity_Analysis

## Overview

The purpose of this analysis was to create a machine learning model to predict whether charities applying for funding from Alphabet Soup will be successful. The target performance for the model was 75% accuracy. To accomplish this, categorical data was preprocessed using bucketing and one-hot encoding. The data was then split into training and testing sets and to fit and test a neural network model. After evaluation, a second, more optimized model was created from the first and evaluated.

## Results

* ### Data Preprocessing
  * Each charity in the data had a "IS_SUCCESSFUL" variable to be used as the target for the model
  * The APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT variables were all used as features for the model.
![Dropped Variables](https://github.com/deklund76/Neural_Network_Charity_Analysis/blob/main/Resources/dropped_variables.png)
  * The EIN (Ids) and NAME variables were unnecessary for the model and were removed
* ### Compiling, Training, and Evaluating the Model
 * The target performance of 75% could not be achieved in either the first or second interations of the model.
![Model1 Performance](https://github.com/deklund76/Neural_Network_Charity_Analysis/blob/main/Resources/model1_performance.png)
![Model2 Performance](https://github.com/deklund76/Neural_Network_Charity_Analysis/blob/main/Resources/model2_performance.png)
![Model1](https://github.com/deklund76/Neural_Network_Charity_Analysis/blob/main/Resources/model1.png)
  * The initial model used 80 first layer nodes and 30 second layer nodes with relu activation functions. 80 since that was about double the number of input nodes (43) and 30 on the second since that was just under half of the first layer following simple rules of thumb.
![Model2](https://github.com/deklund76/Neural_Network_Charity_Analysis/blob/main/Resources/model2.png)
  * The optimized model attempted to increase performance by changing (in different combinations before finally all together) the number of hidden layers to 3 with 120, 60, and 30 nodes respectively; the activation functions to hyperbolic tangent functions; and dropping the ASK_AMT variable since it contained large outliers. This unfortunately failed to improve model performance.

## Summary
Overall the results were promising, but fell just short of the performance target. It's recommened that different models are tried to achieve higher performance while also using fewer resources. A good place to start would be with a random forest classifier model as the analysis of feature importance could prove useful in further optimization.
