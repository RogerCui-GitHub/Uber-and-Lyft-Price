# Analysis and Prediction of Uber and Lyft Price
Author: Yujie Cui

## Ⅰ. Introduction
Unlike public transportation, Uber and Lyft’s ride prices are not constant and fluctuate greatly. And their demand is more dispersive and uncertain. In our project, we want to analyze the cab demand and predict the ride price based on given conditions. Our final goal is to give suggestions to drivers and passengers. The driver could find the location where may have higher demand; and the passenger may avoid a high ride-price situation. Python is used as our data analysis tool, which is popular in the field of data mining and machine learning. To predict the ride price, we build a random forest model using the given conditions. Besides, we also employ some packages in Python to show the relationship between cab demand and different features. 


## Ⅱ. Problem Description
There are three main problems we try to solve: 
1. Can we accurately predict the cab price? 
2. What features are more important on cab prices? 
3. When and where is the cab demand higher? 

Our main goal is to build a model to predict the ride price based on given conditions. As we all know, distance, time, car type, and so on, may impact on cab price. If we know a certain condition, can we use it to predict the right ride price? Besides, we also wonder which features are more important on cab price. As costumers, we always want to reduce our cost. If we know what conditions may cause a high cost, we can avoid them and save money. For drivers, they are more concerned for earning money. As a result, increasing cab order will benefit to drives. Then where and when the cab demand higher is important and it is our third problem.
 
 ## Ⅲ. Methodology
To solve those problems, we visualize the relationship between each feature and build a model to predict the cab price. To evaluate the results, we employ R2 score in the prediction of model. 

The visualization tools include pie chart, box plot and scatter plot. Pie chart is a great tool to visualize the proportion of different parts in a given feature, which could tell us which one is largest and which one is the smallest. Box plot, in our project, is used to display the relationship between two features. One is a category feature and the other one is a numerical feature. We can see the 25%, 50% and 75% of the numerical feature in a certain category. Finally, we also employ a scatter plot to visualize the relationship between two numerical features. 

The model in our project is random forest. Random forest is an ensemble tree-based model for classification and regression. The difference between random forest and general decision tree is that random forest contains multiple decision trees and its final model is based on the average of those trees, which reduces the variance and increases the accuracy of prediction. Besides, the package of random forest in python have a build-in feature called “feature importance” , which can help us directly visualize the importance of all of those feature we use. 

## Ⅳ. Dataset Description
In our project, we choice cab and weather dataset from Kaggle predict cab prices against given features. This dataset is real-time data using Uber and Lyft api queries and corresponding weather conditions in Boston [1]. The cab ride data contains many types of cabs for Uber and Lyft and their price for some popular locations. Weather data contains weather features, such as temperature, rain, cloud, etc. for all the locations taken into consideration. 

In cab ride dataset, there are 10 colums and 693071 rows; in the weather dataset, there are 8 columes and 6276 rows. The types of features contain continuous numeric, drecrete numeric and category features. 

To predict cab price conprehensively, we need to combine the cab ride dataset and weather dataset. Firsly, we chance the “time_stamp” into “date_time” by function, “pd.to_datetime". Secondly, we create a new feature called “merge_date” to refelect same time for a location in both cab ride dataset and weather dataset. Thridly, we merge those two dataset based on the “merge_date” and create a new dataset which contains all the important features we need. There are 15 columes and 1164996 rows. 

The data in new dataset is not clean and there are many missing values. For the rows without “price”, we drop those rows because our goal is to predict the cab price. For the 2964 rows without temperature, clouds, humidity and wind value, we also drop them because their proportion in the total 1164996 are really small. Finally, for the 1061692 rows without rain value, we fill the missing values into 0 to assume there are no raining. 


