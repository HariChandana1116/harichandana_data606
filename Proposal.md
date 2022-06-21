# Capstone Data Science 606 
##### Proposal By :
##### Hari Chandana Datla
##### Lakshmi Chandana Shaik
### 500 Cities: Local Data for Better Health

#### Issue of interest
Health is a foremost important factor in the society. In the current fast living culture people are falling prey for chronic diseases. Unhealthy behaviors and eating habits are leading to chronic diseases like high blood pressures, diabetes and unhealthy cholestrol levels. Along with these people are also looking for ways to prevent these diseases by adopting much healthier choices. We have looked into the health data to explore more on the chronic diseases and how many people are into prevention and how many are taking action based on their health outcomes.

#### Issue importance
By working on this health data, we can get to know the quality of public health in these practical situations. The analysis of this health data will be useful in understanding the trend of the chronic diseased and the unhealthy behaviors leading to them. Also this data will be useful for introducing new health policies and other preventive measures like digitalized health applications that can target people from a specific demography. 

#### What questions do you have in mind and would like to answer?
* The main objective is to analyze the unhealthy behaviors, health outcomes and prevention (3 variables) responsible for chronic diseases in major cities.
* Which cities are more into prevention?
* Predicting cities which are more prone to chronic diseases?
* Identifying which machine learning model gives the best accuracy score for our analysis

#### Data source 
The source for this data is CDC(Centers for Disease Control and Prevention)., Division of Population Health, Epidemiology and Surveillance Branch and this project of making this dataset was funded by the Robert Wood Johnson Foundation (RWJF) in conjunction with the CDC Foundation. Data sources used to generate these measures include Behavioral Risk Factor Surveillance System (BRFSS) data (2016, 2015), Census Bureau 2010 census population data, and American Community Survey (ACS)
2012-2016, 2011-2015 estimates.

Link for the dataset : [Dataset](https://chronicdata.cdc.gov/500-Cities-Places/500-Cities-Local-Data-for-Better-Health-2018-relea/rja3-32tc)

This dataset was first created on December 4th, 2019.

Last release was on December 5th, 2019.

Size of dataset is 224.276 MB.

The dataset has 810k rows and 24 columns.

Dataset has information from 500 cities from the US which helps in bringing out data for better health.
<img width="403" alt="image" src="https://user-images.githubusercontent.com/77841272/172907884-3216d0f2-f473-4fc8-9197-47b8d3231834.png">

* Dataset has information from 500 cities from the US which helps in bringing out data for better health.
* Each row represents an estimate from various cities with a unique ID and on what measures it was taken with a measureID as well from the years 2015 and 2016. It was provided with a geographical location and geographical level like US or City or Census tract, from where the estimate was collected.
* In this dataset, we have found that the measures that cause chronic diseases were categorized into three major grades like Unhealthy behaviors, Health outcomes and Preventions. These brands are labelled under the column named Category. This Category column has these three sections of measures that cause chronic diseases.
Below is a pie chart that exhibits the break down of those categories.

<img width="490" alt="image" src="https://user-images.githubusercontent.com/77841272/172450415-248c823a-6880-4b50-9169-6c7d5f1c7e7d.png">

#### Unit of analysis
Our unit of analysis would be category which comprises of unhealthy behaviors, health outcomes and prevention. For example, we will analyse the rate of unhealthy behaviours in a particular state and the rate of their usage of preventive measures.

#### What variables/measures do you plan to use in your analysis (variables should be tied to the questions in #3)?
We plan to use cities, state, measure and measure id in our analysis. The target variable that we will be predicting is Category.

#### What kinds of techniques/models do you plan to use (for example, clustering, NLP, ARIMA, etc.)?
* Decision Tree
* Logistic Regression
* Cross Validation
* Grid Search
* KNN classifier
#### How do you plan to develop/apply ML and how you evaluate/compare the performance of the models?
We are planning to evaluate the metrics such as recall, accuracy, precision, f-1 score and  confusion matrix. 
#### What outcomes do you intend to achieve (better understanding of problems, tools to help solve problems, predictive analytics with practicle applications, etc)?
We will be visualizing data with the help of Tableau. We are also contemplating in using Plotly to develop dashboards stating the health status of the population in major cities.
#### Work Distribution
##### Hari Chandana Datla
* Data Cleansing and pre processing
* Logistic Regression
* KNN classifier
* Grid Search
* Metrics
##### Lakshmi Chandana Shaik
* Data EDA
* Decision Tree
* Cross Validation
* Data visualization 
