# Berlin Airbnb Project

## Data

The data for the project can be found on [kaggle]https://www.kaggle.com/brittabettendorf/berlin-airbnb-data .
The data was from 6 different csv files:

- Listings Summary
- Listings Detailed
- Neighbourhoods
- Calendar Summary
- Reviews Summary
- Reviews Detailed

The data should be downloaded and put in a file inside data/raw.

## Purpose

The purpose of this project is to create a model that estimates the price an accomodation should be advertised for on AirBnb. The goal would be to create a resource that airbnb hosts could input the information of their property and the model would predict how much the property should be placed on airbnb for.

## Process

### Exploratory Data Analysis

I began by exploring the data to find useful columns and discover missing values. I create visualisations of the categorical columns and try to visualise the spread of the price of the properties. After perfoming exploritory data analysis of each table, I decided to only use the detailed listings table for my modelling. 

### Data Cleaning

I removed many columns I felt were not needed in the model or would have caused data leakage. Then I filled in missing data using other columns where possible or by using the data already in the column. 

### Feature Engineering

- Using the latitude and longitude columns I calculated the distance from the centre and popular tourist attractions.
- Using the amenities column I created binary columns of amenities I felt may increase/decrease the value of the accomodation.

## Modelling

I created 3 different models to predict the price:

- Multiple Linear Regression
- Random Forest
- K Nearest Neighbours

I used K fold cross validation to prevent overfitting in the multiple linear regression model.

## Findings

All models didn't perform within a desirable mean squared error. My explanation for this is that either I did not feature engineer enough important information (e.g. size of property) or the data wasn't there for important factors. 

I predict that a properties value is based upon the images a host posts of the property. From these images an interested party can judge how nice a property is and therefore it's value. 
