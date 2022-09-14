<img width="560" alt="image" src="https://user-images.githubusercontent.com/77841272/185727220-aff202f3-b378-4497-88b8-5c8079613e9c.png">

# **CDC 500 Cities: Local data for better Health**
### Data 606 Capstone project
#### Team C
###### Hari Chandana Datla
###### Lakshmi Chandana Shaik
[Project link Youtube](https://youtu.be/vc3as84qhiM)

[Presentation link](https://github.com/HariChandana1116/harichandana_data606/blob/main/500%20Cities%20PPT.pptx)

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
Health is a foremost important factor in the society. In the current fast living culture people are falling prey for chronic diseases. Unhealthy behaviors and eating habits are leading to chronic diseases like high blood pressures, diabetes and unhealthy cholestrol levels. Along with these people are also looking for ways to prevent these diseases by adopting much healthier choices. This capstone project provides an insight into use of health care data, starting with generating a quality data, discovering patterns and extracting knowledge using various machine learning models.
In this project we have used various tools such as Matplotlib, Sweetviz, PySpark, PySparkSQL and python machine learning libraries.  

#### **Dataset Overview**
The source for this data is CDC(Centers for Disease Control and Prevention)., Division of Population Health, Epidemiology and Surveillance Branch and this project of making this dataset was funded by the Robert Wood Johnson Foundation (RWJF) in conjunction with the CDC Foundation. Data sources used to generate these measures include Behavioral Risk Factor Surveillance System (BRFSS) data (2016, 2015), Census Bureau 2010 census population data, and American Community Survey (ACS)
2012-2016, 2011-2015 estimates.

Link for the dataset : [Dataset](https://chronicdata.cdc.gov/500-Cities-Places/500-Cities-Local-Data-for-Better-Health-2018-relea/rja3-32tc)

Size of dataset is 224.276 MB.

The dataset has 810k rows and 24 columns.

Dataset has information from 500 cities from the US which helps in bringing out data for better health.

<img width="403" alt="image" src="https://user-images.githubusercontent.com/77841272/172907884-3216d0f2-f473-4fc8-9197-47b8d3231834.png">

### **Data Cleaning & preparation**

The first step in our project in data cleaning. There were null values and duplicate values in few columns of the dataset. We have checked in which columns were the null values existing. There were null values in the columns regarding data value footnotes and other columns which has least importance forour analysis. There fore we have dropped those columns from our dataset thus handling null values in our dataset too. 
Then we have found that the duplicate values are due to census tract data in our dataset. Therefore we have found more than one value for a city due to city FIPS number.
Also we have used Sweetviz to see the health of the dataset. And these Sweetviz output files can be seen [Sweetviz](https://github.com/HariChandana1116/harichandana_data606/tree/main/Sweetviz) folder in the repository.

### **EDA**

After the data cleaning process we have started our EDA by grouping the target feature "CategoryID" and pulled out the graphs for rest of the columns. We have carried out the EDA process on New York, California data. This EDA process was carried both in [Google colab notebook](https://github.com/HariChandana1116/harichandana_data606/blob/main/EDA%20and%20Machine%20Learning/EDA%20%26%20ML.ipynb) as well as in [Databricks PySpark](https://github.com/HariChandana1116/harichandana_data606/blob/main/EDA%20and%20Machine%20Learning/606-EDA%20Databricks%20(1).ipynb) and they can be seen in the repository.

<img width="809" alt="image" src="https://user-images.githubusercontent.com/77841272/185717343-1e652df9-3586-4ff9-9662-f05c20da3409.png">
<img width="813" alt="image" src="https://user-images.githubusercontent.com/77841272/185717398-ab84f425-dc69-4ddb-a3dd-d9bc6ba18d02.png">
Then after correlation matrix shows all the posible pairs of values correlated in the table and below is the visualization of it.
<img width="507" alt="image" src="https://user-images.githubusercontent.com/77841272/185717839-150ca134-f9d5-434f-8979-29443e9aeff8.png">
we have also plotted scatter plot for the relationship between obesity and high blood pressure.
<img width="323" alt="image" src="https://user-images.githubusercontent.com/77841272/185717688-6b630665-5be1-42d3-a587-6154ef83f083.png">

### **Data Processing & Encoding**

After EDA, the we had to further process our dataset in order to make it ready for our machine learning analysis. We have found a significant imbalance in our dataset. So we have performed resampling to balace our data as using imbalance data for machine learning analysis can produce biased results. Below is the image that shows the data before and after resampling.
<img width="571" alt="image" src="https://user-images.githubusercontent.com/77841272/185727245-6756ded7-260c-499e-a45f-254160f4737e.png">

After resampling we have started encoding all the categorical values using OneHotEncoder. As part of encoding we have encoded the Target variable values as the following
* Health Outcomes = 1
* Unhealthy Behavior =2
* Prevention = 3
The below is the final dataset that we have used for machine learning models.
<img width="542" alt="image" src="https://user-images.githubusercontent.com/77841272/185726822-6efac626-c9ee-49c5-b782-89ba3a60aec9.png">
We have split this final dataset into training and test dataset with 70% of the data in training and the remaininng 30% for testing.


### **Machine Learning Models**

We have decided to perform three regression models and two classifier models on our data.
1. Linear Regression
2. Ridge Regression
3. Lasso Regression
4. Decision Tree Classifier
5. Random Forest CLassifier

The three linear regression models Linear, Lasso and Ridge can be found in the [Regression](https://github.com/HariChandana1116/harichandana_data606/blob/main/EDA%20and%20Machine%20Learning/Regression_models.ipynb) notebook. Ridge and Lasso regression models fall into the same family of Linear regression model. But the difference is the model is penalized for its choice of the weights. In Lasso regression the absolute values of weight will be reduced, and many will tend to be zeros. Therefore it will avoid overfitting which generally happen in linear regression model. Similar to Lasso in Ridge regression the model is penalized for the sum of squared value of the weights.

Decision tree is a supervised machine learning algorithm that can be used for both classification and regression. And as the name suggests Random Forest is a tree-based machine learning algorithm that uses the power of multiple decision trees for making decisions.


### **Conclusion**
The analysis has given a good picture regarding the measures that are leading to various health outcomes along with various measures people are taking for preventing certain health outcomes. We have occured to the following conclusion that there are less number of people who are into prevention measures. Also there are more people who are depending on medications.
From our machine learning models performance scores, we have found out that the classification models i.e. Decision Tree classifier and Random Forest classifier are better suitable for our dataset than the three regression models. 

<img width="457" alt="image" src="https://user-images.githubusercontent.com/77841272/185714625-0319845d-e80a-46bd-a388-994df6a25729.png">

This analysis has further scope where each measure can be analysed seperately for specific geographic location. Such analysis will be useful for government agencies and digital health care application developers in designing new initiatives and business ventures in respect to each specific geographical location.

### **References**

[GitHub link](https://github.com/HariChandana1116/harichandana_data606)

[500 Cities- CDC](https://chronicdata.cdc.gov/500-Cities-Places/500-Cities-Local-Data-for-Better-Health-2018-relea/rja3-32tc)

[Regression models](https://towardsdatascience.com/whats-the-difference-between-linear-regression-lasso-ridge-and-elasticnet-8f997c60cf29)

[Classification models](https://www.analyticsvidhya.com/blog/2020/05/decision-tree-vs-random-forest-algorithm/)
