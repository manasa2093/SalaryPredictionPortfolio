# SalaryPredictionPortfolio
Salary Prediction Project (Python)

**GOAL** : Predict salary based on Job Description

**INTRODUCTION:** The prediction of Salary structure in Human Resource department ( HR) of a company  contains two fold objectives, namely to  attract and retain the talented employees and show the door to the dead wood. <br />

On the other hand, Salary prediction can also help the job seekers. It helps job seekers to  take more informed decisions and update their skills/knowledge to maximize salary. <br />

**It is a win – win formula for both employers and job seekers.**  <br />

In this project, I am going to build predictive model for accurately predicting salaries based on three datasets.

**Train features and Train salaries-** This predictive model is trained using these 2 datasets consisting of 10 variables(including the target varibale) and 1 millon entries. <br />
**Test features-**  This dataset is used for predicting the model which is built. <br />

The tools I  used are Python and the libraries- numpy, pandas, matplotlib, seaborn and sklearn.

# Table of Contents- 4D Method

&nbsp; &nbsp; **Define Problem**  <br />
&nbsp; &nbsp; &nbsp; -Can we predict salary based on job description?  <br />
&nbsp; &nbsp; &nbsp; -objectives  <br />
  
&nbsp; &nbsp; **Discover data**  <br />
&nbsp; &nbsp; &nbsp; -Load data  <br />
&nbsp; &nbsp; &nbsp; -Exploratory Data Analysis(EDA)  <br />
&nbsp; &nbsp; &nbsp; -Data Visualization  <br />
  
&nbsp; &nbsp; **Develop solutions**  <br />
&nbsp; &nbsp; &nbsp; -Establish a baseline  <br />
&nbsp; &nbsp; &nbsp; -Machine Learning Models  <br />
&nbsp; &nbsp; &nbsp; &nbsp;**-Linear Regression**  <br />
&nbsp; &nbsp; &nbsp; &nbsp;**-Ridge Regression** <br />
&nbsp; &nbsp; &nbsp; &nbsp;**-Random Forest**  <br />
&nbsp; &nbsp; &nbsp; &nbsp;**-Gradient Boosting**  <br />
&nbsp; &nbsp; &nbsp;-Selecting the Best model  <br />
  
&nbsp; &nbsp; **Deploy model**  <br />
&nbsp; &nbsp; &nbsp; -Deploy solution  <br />
&nbsp; &nbsp; &nbsp; -Featuring importance  <br />

## **DEFINING THE PROBLEM-** <br />

**Can we predict salary based on Job Description?**

Why it is important to predict salary ? Well, the purpose is multifaceted.

Predicting salary based on Job location, skillset, experience and other factors is beneficial to both employers and employee purpose.

How this is useful to Jobseekers/employees? <br />
&nbsp; &nbsp; -Can know whether your current pay is accurate represenation of your qualifications ? <br />
&nbsp; &nbsp; -Take more informed decisions and update skills/knowledge to maximize salary. <br />
&nbsp; &nbsp; -Professional growth and personal satisfaction. <br />

For employers, it helps the company in reducing the unnecessary cost while retaining the best talent.

**Objectives**  <br />
&nbsp; &nbsp; -Help employees take right decision in chosing a particular job.

&nbsp; &nbsp; -Help employers chose the correct candidates and pay.

## **DISCOVER DATA-** <br />


This dataset contains both numeric and catergorical varibles.  <br />
**Numeric varibales -**  <br />
&nbsp; &nbsp; -yearsExperience: work experience in years <br />
&nbsp; &nbsp; -milesFromMetropolis: The distance from company's location to employee place.  <br />
&nbsp; &nbsp; -Salary: Target variable            <br />

**Categorical varibales-**  <br />
&nbsp; &nbsp; -jobType: Type of job.For example- CEO,CTO and manager. <br />
&nbsp; &nbsp; -major: Specific concentration  <br />
&nbsp; &nbsp;-degree:Educational qualification. eg. High school, masters <br />
&nbsp; &nbsp;-industry: The industry where the company is specilized in.  <br />

**Data Visualization** <br />

Below plot shows the distrubution of salary(target varibale). The salary range is high between 80 to 150.

[
<img width="765" alt="salary dist" src="https://user-images.githubusercontent.com/64856136/92647370-c701ae80-f2b5-11ea-9250-9aa7affc6013.png">
](url)

The below plot shows the corelation between numeric variables- yearsExperince and milesFromMetropolis with salary.  <br />

**Positive correlation-** Years of experience and salary -There is increase in salary with experience.  <br />
**Negative correlation-** miles from metropolis and salary -If miles increase , salary decreases.


<img width="657" alt="Screen Shot 2020-09-09 at 4 08 10 PM" src="https://user-images.githubusercontent.com/64856136/92647938-b69e0380-f2b6-11ea-9080-117500e55cbd.png">

## **CORRELATION MATRIX-** <br />

**Strong positive correlation -** with each of the variables - Jobtype, degree, major, industry, experience have positive correlation with salary(our target variable). <br />
**Negative correlation -** exist between miles from metropolis and salary. <br />
Weak correlation exists between company id and salary <br />

<img width="892" alt="Correlation matrix" src="https://user-images.githubusercontent.com/64856136/92650160-1d70ec00-f2ba-11ea-8056-eef4339c36ad.png">


## **MODEL EVALUATION AND SELECTION** <br />

Calculated the average salary per industry and  mean squared error as **baseline**. <br />

I created dummies for categorical variables, scaled data for numeric data and I used 70% of data for training  and 30% for testing.  <br />
Then, I developed the following 3 models and selected the best model. I chose mean square error as performance metric. <br />

<img width="316" alt="results" src="https://user-images.githubusercontent.com/64856136/92648909-32e51680-f2b8-11ea-9c50-cb0af4f77adc.png">

**GOAL-** To find the best model that has mean square error below 360. <br />

Since Gradient Boosting gave us the lowest mean square error, so I used this model to predict the results for test_features dataset and saved it to csv file.  <br />

Next, I checked the importance of each feature in the model. 

<img width="980" alt="feature importance" src="https://user-images.githubusercontent.com/64856136/92649198-a6872380-f2b8-11ea-9151-efd0e96f9856.png">

Notebook url - https://github.com/manasa2093/SalaryPredictionPortfolio/blob/master/SalaryPredictionPortfolio.ipynb
