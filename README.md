# House-Price-Prediction-with-Multivariate-Linear-Regression-Model

![image](Image/realtor.png)

# Overview
The real estate market has grown significantly in recent years, given changes in the ways people are buying, selling, and financing their houses. Machine learning and artificial intelligence can make  revolutionary changes in the housing market. Machine learning  algorithms can rapidly organize large quantities of data, sorting through property values, debt information, key home factors, and even consumer information. For instance, through a price-prediction modle a home buyer or sellers have an oppurtunity to decide wisely.

# Business Understanding
Realtor.com is a real estate listing website operated by the News Corp subsidiary Move, Inc. It was relaunched in 1996 as a public website displaying property listings. Now they want to offer valuations of houses using machine learning techniques to their customers. The company asked to design a model that be used to predict house sales in King County, Washington State, USA using Multiple Linear Regression (MLR). The dataset consisted of historic data of houses sold between May 2014 to May 2015. They need this model to guide real estate investors who use the platform to have a better decision on which house is more valuable to invest.

# Methadology

When modeling for prediction, we are trying to accurately predict at all costs. Thus, we usualy use all available features (and most likely engineer new features). And, we are less concerned about the coefficients of these features and instead focus on the overall accuracy of our model.
The general research strategy in this project is to use OSEMN framework on the King County House Sales dataset. The process includes the below steps:

- Obtain data

- Scrub data

- Explore data

- Model data

- Interpret modle

## Obtain data

The very first step of the project is obtain data. We obtain the data that we need from 'kc_house_data.csv' file. Obtain data starts with importing needed libraries and modules in our framework. Our file is CSV (comma-separated values) file that can be opened using  `pd.read_csv()` method. 

## Scrub data

After obtaining data, the next immediate thing to do is scrubbing data that make them operational. In this way, dealing with messy data means dealing with missing values, inconsistent formatting, malformed records, or nonsensical outliers. The beginning of data cleaning is to print a concise summary of a DataFrame with `.info()` method and view a small sample of the DataFrame object with `.head()` method. Through the `.info()` method we access valuable information about missing values and datatype. `.isnull()` is a method that helps us determine the missing value and based on the percentage of them or necessity of them, decided on delete (`.dropna()` method) them or fill (`.fillna()` method) them with suitable values. With `.duplicated()` method we also check the duplications and drop them through `.drop_duplicates()` method.

## Explore data

Once our data is ready to be used, and right before jumping into AI and Machine Learning, we should examine the data to make sense of them. This step will help stackholders to get accurate, actionable insights from our data analytic.To achieve that, we will need to explore the data by inspecting some analytical questions. This step includes below substeps:

- Inspect the data and its properties: Different data types like numerical data, categorical data, ordinal and nominal data  require different treatments.
- Compute descriptive statistics:  Extract features and test significant variables
- Data visualisation: Identify significant patterns and trends in our data

The below questions might help better insight into our database.

### Question 1;  How does the age of the houses impact the house price?
To answer this question, house were categorized based on their age. Then their price and mean price were ploted based on age groups. 

![image](https://user-images.githubusercontent.com/101681195/193060953-1cab4d21-7d09-4ebe-917b-2dff19a910ca.png)

### Insights

The results from our exploration inform us that:
- Houses in different age groups have high distribution of prices. 
- Most of the houses in the market are younger than 45 years.
- Houses youger than 45 years have higher average price.
- By increase the age of the house more than 83 years the house average price increasing. 

### Recommendation

> Older houses have the potential to introduce as vintage houses. This could attract coustomers to this houses. 


### Question 2; How does house condition impact the house price? 
To answer this question, the relation of house prices with square footage of the house were ploted based on different house conditions.


![image](https://user-images.githubusercontent.com/101681195/193094547-f080d46c-1a81-4a31-97b3-e0873132b7c6.png)


### Insights

The results from our exploration inform us that:
- House price and square footage of the house have a relatively linear relation. 
- By increasing the square footage of the house the house prices increas
- Most of the house are in average condition
- Very good condition in comparison to square footage of the house has a lower impact on house prices

### Recommendation
> In all house conditions, square footage of the house has a direct impact on the house price. The average condition has a potential to be sell withoit needing to renovate the house. 

## Model Data
The first step was to bulid a "baseline model" from the dataset. Any decisions on how to change features was compared against a baseline model to see if the changes have improved the model or not. Below techniques were tried to improve the regression model was listed:

- Transform categorical variables
- Check outliers and remove them
- Check Multicollinearity of features and remove them
- Feature scaling and normalization
- Check intractions between features

After covering these modifications, multiple linear regressions was built using the Statsmodels and Scikit-Learn libraries. In the next step, below  metrics for evaluationin linear regression were assessed:
- Adjusted R^2: Measures variation explained by only the independent variables that actually affect the dependent variable
- Coefficients: Describe the mathematical relationship between each independent variable and the dependent variable.
- P-values: Indicate whether the relationships are statistically significant
- Mean Squared Error (MSE): The most common metric for regression tasks is MSE. It is the average squared difference between the estimated values and the actual value.

## Interpret modle

![image](https://user-images.githubusercontent.com/101681195/193163642-4c5c72fe-57da-4f6c-b4b5-d2b0e11b4ae6.png)

- Adjusted R^2:

We were able to increase the Adj R Sqaured value by an entire thousandth through rigorous experimentation. The basline model Adj R is 0.675. The final modle Adj R is 0.691 that means 69.1% of the variations in price 𝑦 are explained by the features in our model. It is not a strong R square. But the coefficients of the variables are quite strong.

- Coefficients:

The variables have high values for coefficients and grade_13_Mansion has highest coefficient. Other determiners for house price are waterfront views, condition, floors,age, and bathrooms.

- P-values:

All the p-values are quite low, that indicates there is sufficient evidence in the sample to conclude that a correlation exists.

- Mean Squared Error (MSE): 

The model underestimated 21.93% of house prices by over 100,000 and overestimated 26.32% house prices by over 100,000
