# Activity Identification of Wearable Technologies

## Introduction
In this project, I investigated and analysed the popular PAMAP2 dataset.I built and compared different models to capture the underlying functions of how various data points can be used to correctly predict activities being carried out.
The dataset is made up of observations captured through the use of 4 Activity Monitoring sensors. These sensors are attached to the hands, chest, ankle and another to monitor heart rate while performing 12 different physical activities. 
These readings were taken by having 9 different subjects, 8 men and 1 woman, carry out various activities while wearing the sensors.

## Goal
The goal of this project is draw insights into how measurements and readings taken from the subjects while carrying out the various activities can tell us how active an individual is, what activity is being carried out as well as using this information in creating a marketable product.
We will focus on these three targets for this report:
* Thoroughly explore data through analysis and appropriately handle missing or dirty data.
* Produce and Accept or Reject at least one hypothesis for a relationship between a single pair of attributes.
* Develop and test at least one model which uses multiple attributes to make predictions.

## Results
### Hypothesis Testing
`*If a higher change in heart rate is a good representation of how intensive an activity is, then activities that increase heart rate a lot are more physically intensive than activities that increase heart rate by little change.*`

**Is Ascending stairs significantly physically more intensive than Descending stairs i.e On average, does Ascending stairs cause a higher change in heart rate than Descending stairs?**

$H_0$ : The mean heart rate while Ascending stairs is **NOT** higher than the average heart rate change while descending stairs.

$$
\begin{align}
\mu_a =< \mu_d \\
\mu_a - \mu_d <= 0
\end{align}
$$

$H_a$ : The average heart rate change while Ascending stairs is higher than the average heart rate change while descending stairs. 

$$
\begin{align}
\mu_a > \mu_d\\
\mu_a - \mu_d > 0  
\end{align}
$$

The p-value of 0.0006891572262405221 was gotten leading to rejecting the null hypothesis that Descending stairs is more intensive physically than Ascending stairs. Even at significance level as low as
0.1% , we shall still reject the null hypothesis. This actually backs the logical assumption that Ascending stairs is harder than Descending stairs.

### Modelling
In the modeling stage, I fitted and tested a linear regression model on the training data to predict heart rate change while varying the number of components using Principal Component Analysis, testing on test/unseen data. 
The model achieved best RMSE score of 5.031, best MAE of 4.065 and obtained best R^2 score of 0.3359, indicating poor prediction performance. Both linear and logistic regression models were used, with logistic regression performing better with an accuracy of 82% and precision of 79.9%. It was also found that dimensionality reduction did not improve the performance of the models. Other modelling techniques were attempted like Polynomial Regression, KMeans and KNN, these algorithms appeared to be to powerful for my machine and either took too long to run or crashed my computer by running out of RAM memory.
