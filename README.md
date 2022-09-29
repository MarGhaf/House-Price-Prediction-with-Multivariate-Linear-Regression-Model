# Home-Price-Prediction-with-Multivariate-Linear-Regression-Model

![image](Image/realtor.png)

## Overview
The real estate market has grown significantly in recent years, given changes in the ways people are buying, selling, and financing their houses. Machine learning and artificial intelligence can make  revolutionary changes in the housing market. Machine learning  algorithms can rapidly organize large quantities of data, sorting through property values, debt information, key home factors, and even consumer information. For instance, through a price-prediction modle a home buyer or sellers have an oppurtunity to decide wisely.

## Business Understanding
Realtor.com is a real estate listing website operated by the News Corp subsidiary Move, Inc. It was relaunched in 1996 as a public website displaying property listings. Now they want to offer valuations of houses using machine learning techniques to their customers. The company asked to design a model that be used to predict house sales in King County, Washington State, USA using Multiple Linear Regression (MLR). The dataset consisted of historic data of houses sold between May 2014 to May 2015. They need this model to guide real estate investors who use the platform to have a better decision on which house is more valuable to invest.

## Methadology

When modeling for prediction, we are trying to accurately predict at all costs. Thus, we usualy use all available features (and most likely engineer new features). And, we are less concerned about the coefficients of these features and instead focus on the overall accuracy of our model.
The general research strategy in this project is to use OSEMN framework on the King County House Sales dataset. The process includes the below steps:

. Obtain data
. Scrub data
. Explore data
. Model data
. iNterpret

### Obtain data

The very first step of the project is obtain data. We obtain the data that we need from 'kc_house_data.csv' file. Obtain data starts with importing needed libraries and modules in our framework. Our file is CSV (comma-separated values) file that can be opened using  `pd.read_csv()` method. 

## Scrub data
