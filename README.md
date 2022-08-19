# **CDC 500 Cities: Local data for better Health**
### Data 606 Capstone project
#### Team C
###### Hari Chandana Datla
###### Lakshmi Chandana Shaik
#### **Contents**
* [Introduction & Overview](#introduction--overview)
* [Dataset Overview](#dataset-overview)
* [Data Cleaning & preparation](#data-cleaning--preparation)
* [EDA](#eda)
* [Data Processing & Encoding](#data-processing--encoding)
* [Machine Learning Models](#machine-learning-models)
* [Conclusion](#conclusion)
* [References](#references)

#### **Introduction & Overview**
Health is a foremost important factor in the society. In the current fast living culture people are falling prey for chronic diseases. Unhealthy behaviors and eating habits are leading to chronic diseases like high blood pressures, diabetes and unhealthy cholestrol levels. Along with these people are also looking for ways to prevent these diseases by adopting much healthier choices. We have looked into the health data to explore more on the chronic diseases and how many people are into prevention and how many are taking action based on their health outcomes.

#### **Dataset Overview**
The source for this data is CDC(Centers for Disease Control and Prevention)., Division of Population Health, Epidemiology and Surveillance Branch and this project of making this dataset was funded by the Robert Wood Johnson Foundation (RWJF) in conjunction with the CDC Foundation. Data sources used to generate these measures include Behavioral Risk Factor Surveillance System (BRFSS) data (2016, 2015), Census Bureau 2010 census population data, and American Community Survey (ACS)
2012-2016, 2011-2015 estimates.

Link for the dataset : [Dataset](https://chronicdata.cdc.gov/500-Cities-Places/500-Cities-Local-Data-for-Better-Health-2018-relea/rja3-32tc)

Size of dataset is 224.276 MB.

The dataset has 810k rows and 24 columns.

Dataset has information from 500 cities from the US which helps in bringing out data for better health.

<img width="403" alt="image" src="https://user-images.githubusercontent.com/77841272/172907884-3216d0f2-f473-4fc8-9197-47b8d3231834.png">

### **Data Cleaning & preparation**

Initially, in the process of data cleaning, existance of null values in the columns are checked and below is the graph that explains more clearly.

IMAGE1

Then data cleaning like removing/dropping the columns that will not help us in our analysis was finished. Below is the image that shows you regarding the same.

IMAGE2

Now, the process of Data preparation is done by checking out various metrics like finding out the unique states and cities from the dataset, checking on some specific states or categories or measures.


### **EDA**

To start with data analysis, we grouped the target feature "CategoryID" and pulled out the graphs for rest of the columns which can be seen below.

IMAGE3

Then after correlation matrix shows all the posible pairs of values correlated in the table and below is the visualization of it.
More visualization is done using a special application called SweetViz and the visuals created from that application are provided in the attached files.

As part of analysing the data more clearly, we have extracted various graphs. Firstly, the below graphs shows the states and cities that occupied top 10 positions in their occurence.

IMAGE4

Secondly, analysing New York and Oklahoma records on the basis of category.

IMAGES5

Then the below graph shows the health outcomes for the measures heart stroke and diabetes in adults from New York state.

IMAGE6

The nextone shows unhealthy behaviours due to measures like binge drinking and sleep deprivation.

IMAGE7

In the same way, some more analysis is continued for the state California that tells us about the health outcomes due to measures like obesity and chronic kidney diseases.

IMAGE8

The below graph explains health outcomes rate for the measures binge drinking and coronary heart diseases in adults from california.

IMAGE9

The next scatter plot gives you corelation between high blood plessure prevalence vs obesity prevalence.


### **Data Processing & Encoding**

There comes processing the data for further usage especially for the machine learning that will be used.
It was found that there is some imbalance in the target variable. SO we had to resample the data which means balancing any imbalances in the features that will be worked on. The below graphs show you how the target variable looks before and after resampling the data.

Now as the target variable is totally balanced, the taret variable is categorical variable as well. Therefore, onehot encoding is used to encode the required columns. Below are some snippets regarding the same.

IMAGE10

As the data is ready to face machine learning models, we began to split the data into training and testing dataset like below.

IMAGE 11

### **Machine Learning Models**

We have decided to perform three regression models and two classifier models on our data.
1. Linear Regression
2. Ridge Regression
3. Lasso Regression
4. Decision Tree Classifier
5. Random Forest CLassifier

Below image shows the scores of regression models.

IMAGE 12

Followed by the results of classification models.

IMAGE 13

To have a better understanding and comparision, we have compared all the results and put them together in the bar graph for better understanding.

IMAGE 14





### **Conclusion**

### **References**
