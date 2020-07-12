# Analysis and Prediction of Uber and Lyft Price
Author: Yujie Cui

## Ⅰ. Introduction:
Unlike public transportation, Uber and Lyft’s ride prices are not constant and fluctuate greatly. And their demand is more dispersive and uncertain. In our project, we want to analyze the cab demand and predict the ride price based on given conditions. Our final goal is to give suggestions to drivers and passengers. The driver could find the location where may have higher demand; and the passenger may avoid a high ride-price situation. Python is used as our data analysis tool, which is popular in the field of data mining and machine learning. To predict the ride price, we build a random forest model using the given conditions. Besides, we also employ some packages in Python to show the relationship between cab demand and different features. 


## Ⅱ. Problem Description:
There are three main problems we try to solve: 
1. Can we accurately predict the cab price? 
2. What features are more important on cab prices? 
3. When and where is the cab demand higher? 

Our main goal is to build a model to predict the ride price based on given conditions. As we all know, distance, time, car type, and so on, may impact on cab price. If we know a certain condition, can we use it to predict the right ride price? Besides, we also wonder which features are more important on cab price. As costumers, we always want to reduce our cost. If we know what conditions may cause a high cost, we can avoid them and save money. For drivers, they are more concerned for earning money. As a result, increasing cab order will benefit to drives. Then where and when the cab demand higher is important and it is our third problem.
 
 ## Ⅲ. Methodology
To solve those problems, we visualize the relationship between each feature and build a model to predict the cab price. To evaluate the results, we employ R2 score in the prediction of model. 

The visualization tools include pie chart, box plot and scatter plot. Pie chart is a great tool to visualize the proportion of different parts in a given feature, which could tell us which one is largest and which one is smallest. Box plot, in our project, is used to display the relationship between two features. One is category feature and the other one is numerical feature. We can see the 25%, 50% and 75% of the numerical feature in certain category. Finally, we also employ scatter plot to visualize the relationship between two numerical features. 

The model in our project is random forest. Random forest is an ensemble tree-based model for classification and regression. The difference between random forest and general decision tree is that random forest contains multiple decision trees and its final model is based on the average of those trees, which reduces the variance and increase the accuracy of prediction. Besides, the package of random forest in python have a build-in feature called “feature importance” , which can help us directly visualize the importance of all of those feature we use. 


