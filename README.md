# Activity Identification of Wearable Technologies

## Introduction
In this project, I investigated and analysed the popular PAMAP2 dataset.I built and compared different models to capture the underlying functions of how various data points can be used to correctly predict activities being carried out.
The dataset is made up of observations captured through the use of 4 Activity Monitoring sensors. These sensors are attached to the hands, chest, ankle and another to monitor heart rate while performing 12 different physical activities. 
These readings were taken by having 9 different subjects, 8 men and 1 woman, carring out various activities while wearing the sensors.

## Goal
The goal of this project is draw insights into how measurements and readings taken from the subjects while carrying out the various activities can tell us how active an individual is and use this information into creating a marketable product.
We will focus on these three targets for this report:
* Thoroughly explore data through analysis and appropriately handle missing or dirty data.
* Produce and Accept or Reject at least one hypothesis for a relationship between a single pair of attributes.
* Develop and test at least one model which uses multiple attributes to make predictions.

## Results
#### Hypothesis Testing
A Z-test was used to compare ascending stairs and descending stairs activities. I observed that on average while Ascending, subjects heart rate increased by 96.5885% compared to Descending, for which subjects experienced an increase in heart rate by 94.7385% implying that while close, Ascending Stairs is the more stressful. Percentage change in heart rate is used, because a subject's heart rate change will be the best representation of how physically demanding an activity is.  
   *If a higher change in heart rate is a good representation of how intensive an activity is, then activities that increase heart rate a lot are more physically intensive than activities that increase heart rate by little change.*

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

