# Predictive Exploration Project

Selects appropriate variables to train the model that predicts the target using SQL and R for business clients. (SQL, R)

Author: Yinhui(Kami) Yang

## Introduction

In the multiverse of madness, on one Earth: With increasing purchasing power in King County, an ambitious NoMaj (i.e. muggle), Jacob Kawalski, decided to begin a real estate business following Queenie wishes to join the dark side. He may indeed need to be familiar with the current estate industry. We will investigate a sample from the broader dataset 'kc house data 2.csv' in order to solve this problem. We will establish and select an acceptable model for the business information from a sample, predicting real estate values in King County. The 'house 2.csv' dataset contains thousands and thousands of records from customers, including year, price, number of bathrooms, number of bedrooms, zip code, square metres, and other characteristics, etc.

### Data import and preparation
We determined to remove those variables that have been deemed unnecessary from the data. We decided to eliminate factors like day of the week and day of the sale depending on domain knowledge considering we rarely understand when a person will wish to sell. We also eliminated sqft living and sqft lot since the sqft living15 and lot15 variations contain post-renovation measurements and are therefore more contemporary. Customers care about something like a house's condition and location, thus we retained characteristics like condition and zipcode. We transformed all categorical variables in and out of factors and eliminated those missing values in addition to removing variables.

