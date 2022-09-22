# Credit_Risk_Analysis

## Overview:

#### The purpose of this analysis is using Machine Learning statistical algorithms to make a predictions, the dataset we are focus in this module is from LendingClub, which is a P2P lending service company. and we are using our algorithms from Machine Learning to evaluate and predict the credit card risk. Because this program we need to employ different techniques to train and evaluate moduls with unbalanced classes.so we will use imbalanced-learn ad scikit-learn libraries to build and evaluate our moduls using resampling.
#### However we need to oversamle the data using the RandomOverSampler and SMOTE algorithms;
#### as well as undersample the data using the ClusterCentroids algorithm. and then using a combinatorial apprpach of over- and undersampl;ing using the SMOTEENN algorithm;
#### And the end compare two modles that erduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, in order to predict the credit risk.


## Results: 
#### in this case we using the Machine Learning to resample the dataset by using python libraries, scikit-learn and imbalanced-learn to evaluate the results and make it ready to compare our analysis



## The original: 
#### the original data contained loan application in Q1 of 2019. loan status is the key that we used by determine the application risk either "low" or "high". when this info show up current then we mark it as "low risk", other wise we mark it as "high risk"

####  this reuslts get 68,470 of 68,817 as "low risk", 347 as "high risk".
####  by using the 75% method to split the data for training vs. testing, 51,366 "low risk" and 246 "high risk" applications were categorized into the training set.

<img width="1017" alt="Screen Shot 2022-09-21 at 10 38 47 PM" src="https://user-images.githubusercontent.com/106010498/191667579-2308bf18-6b79-493f-9061-f804240d7c65.png">



### ------Deliverable 1------
## 1.RandomOverSampler Model
#### The results classified 51,366 records each as High Risk and Low Risk by randomly selects from the minority class
#### Balanced accuracy score: 66%.
#### The "High Risk" precision rate was only 1% with the recall at 71% giving this model an F1 score of 2%.
#### "Low Risk" had a precision rate of 100% and recall at 62%.

<img width="603" alt="Screen Shot 2022-09-21 at 10 51 02 PM" src="https://user-images.githubusercontent.com/106010498/191668543-78a35fbe-f43d-4ecf-a9b3-c990cbf6065e.png">

<img width="1002" alt="Screen Shot 2022-09-21 at 10 50 56 PM" src="https://user-images.githubusercontent.com/106010498/191668551-085e07e3-69bc-47a7-95b0-061fea3f7127.png">


## 2.SMOTE Model
#### like RandomOverSampler increases the size of the minority class by creating new values based on the value of the closest neighbors to the minority class instead of random selection.


#### The balanced accuracy score: 65.5%.


#### the "High Risk" precision rate again was only 1% with the recall degraded to 63% giving this model an F1 score of 2%.
#### "Low Risk" had a precision rate of 100% and an improved recall at 68%.


<img width="497" alt="Screen Shot 2022-09-21 at 10 57 29 PM" src="https://user-images.githubusercontent.com/106010498/191669419-c1a70153-026c-48d2-bc28-ece40f7826fa.png">

<img width="1034" alt="Screen Shot 2022-09-21 at 10 57 36 PM" src="https://user-images.githubusercontent.com/106010498/191669424-fba7303a-53d0-48f0-b5dc-f019e6567031.png">





#### 3.Undersampling-ClusterCentroids Model
#### an algorithm that identifies clusters of the majority class to generate synthetic data points that are representative of the clusters
####  The model classified 246 records each as High Risk and Low Risk.

#### Balanced accuracy score:65.6%.

#### The "High Risk" precision rate again was only at 1% with the recall at 63% giving this model an F1 score of 2%.
#### "Low Risk" had a precision rate of 100% and with a lower recall at 68% compared to the oversampling models.





<img width="778" alt="Screen Shot 2022-09-21 at 11 06 31 PM" src="https://user-images.githubusercontent.com/106010498/191670683-23000f2f-a5ed-465b-a162-8363e94b20cd.png">

<img width="1077" alt="Screen Shot 2022-09-21 at 11 06 36 PM" src="https://user-images.githubusercontent.com/106010498/191670698-a446cdad-c6e2-432c-8644-a1c26106d45d.png">


### ------Deliverable 2------
#### 4.SMOTEENN Model

#### The model classified 68,460 records as High Risk and 62,011 as Low Risk.


#### The balanced accuracy score improved to 65.6% when using a combined sampling model.
SMOTEENNacc

#### The "High Risk" precision rate was only 1% again, however the recall increased to 63% giving this model an F1 score of 2%.
#### "Low Risk" still showed a precision rate of 100% with the recall at 68%.

<img width="768" alt="Screen Shot 2022-09-21 at 11 13 34 PM" src="https://user-images.githubusercontent.com/106010498/191671782-639512bd-047d-42c4-a777-f7673f29c96b.png">

<img width="1053" alt="Screen Shot 2022-09-21 at 11 13 38 PM" src="https://user-images.githubusercontent.com/106010498/191671799-943c6533-68d4-4a10-8ee4-0e110d0eaa22.png">



### ------Deliverable 3------
#### 5.BalancedRandomForestClassifier Model
#### Two trees of the same size and equal size to the minority class are constructed to represent one for the majority class and one for the minority class.

#### The balanced accuracy score increased to 78.9% for this model.
balanceacc

#### The "High Risk precision rate increased to 3% with the recall at 70% giving this model an F1 score of 6%.
#### "Low Risk" still had a precision rate of 100% with the recall at 87%.
The top feature by importance was "total_rec_prncp" at 7.9% of the total.



<img width="865" alt="Screen Shot 2022-09-21 at 11 17 51 PM" src="https://user-images.githubusercontent.com/106010498/191672354-ab6e1316-793b-49fc-817a-2103c7be8cf7.png">
<img width="634" alt="Screen Shot 2022-09-21 at 11 21 35 PM" src="https://user-images.githubusercontent.com/106010498/191672960-4ac3e1f5-99dc-40e0-8547-349074e57c4d.png">



#### 6.EasyEnsembleClassifier Model
#### a set of classifiers where individual decisions are combined to classify new examples.

#### The balanced accuracy score increased to 93.2% with this model.


#### The "High Risk precision rate increased to 9% with the recall at 92% giving this model an F1 score of 16%.
#### "Low Risk" still had a precision rate of 100% with the recall now at 94%.




<img width="846" alt="Screen Shot 2022-09-21 at 11 23 23 PM" src="https://user-images.githubusercontent.com/106010498/191673224-8f5af58c-214b-4b55-a55b-7c23c90c11e0.png">


## Summary: 
#### As we program going, we should be notice that original dataset have 99% of the applications classified as "low Rick" and only 1% of the data as "High Risk" category .this can make the results unstablily and greatly , and so that the Machine Learning algorithms can help us to predict the results more actual. the company might not be able to comfortable accepting the result with this margin of risk. 

#### However the Machine Learning has more and more info that i don't that i don't, at this moment i just trying to do it without knowing that Elements. but still it can help us to predicting and get the result more and more actually. 






