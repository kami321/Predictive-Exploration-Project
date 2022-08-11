# Predictive Exploration Project

Selects appropriate variables to train the model that predicts the target using SQL and R for business clients. (SQL, R)

Author: Yinhui (Kami) Yang

## Introduction 

In the multiverse of madness, on one Earth: With increasing purchasing power in King County, an ambitious NoMaj (i.e. muggle), Jacob Kawalski, decided to begin a real estate business following Queenie wishes to join the dark side. He may indeed need to be familiar with the current estate industry. We will investigate a sample from the broader dataset 'kc house data 2.csv' in order to solve this problem. We will establish and select an acceptable model for the business information from a sample, predicting real estate values in King County. The 'house 2.csv' dataset contains thousands and thousands of records from customers, including year, price, number of bathrooms, number of bedrooms, zip code, square metres, and other characteristics, etc.

### Data import and preparation

We determined to remove those variables that have been deemed unnecessary from the data. We decided to eliminate factors like day of the week and day of the sale depending on domain knowledge considering we rarely understand when a person will wish to sell. We also eliminated sqft living and sqft lot since the sqft living15 and lot15 variations contain post-renovation measurements and are therefore more contemporary. Customers care about something like a house's condition and location, thus we retained characteristics like condition and zipcode. We transformed all categorical variables in and out of factors and eliminated those missing values in addition to removing variables.

### Building regression model & Evaluating the model

Now is the process for developing the model after cleaning and transforming the data. We selected a linear regression model for the model because we believe it is the best fit for this situation and would tell us which variables are most important in forecasting house prices. We utilized seed number 669 and a 60/40 training validation split for the actual training. This means that 60% of the data is used to train the model, and 40% of the data is used to validate if the model is still good when presented with new data.

<img width="580" alt="pic12" src="https://user-images.githubusercontent.com/81647911/158213538-e54084cf-4b3d-4dd5-8859-757b8c1c56bf.png">

Correlogram:Explore the relationship between the variables

![pic 1](https://user-images.githubusercontent.com/81647911/158101526-b6045a15-e54c-42af-84b6-874019039630.png)

Living room area in 2015 has the strongest relationship with price


![pic2](https://user-images.githubusercontent.com/81647911/158101581-1b3c3dcb-845b-4713-8d3c-558dda7f2cff.png)

![pic3](https://user-images.githubusercontent.com/81647911/158101599-131e8328-8fd6-4b61-b800-5704b3792e1f.png)

##### We could determine the following from the summary:
We may conclude that this model is significant based on the F stat and p-value. The Adjusted R-squared is likewise rather high, at 80.87 %, indicating a reasonably strong matching. There are 10 variables that have a significant impact on price prediction: Year, bathroom, floors, waterfront, grade, sqft_basement, yr _built, yr_ renovated, zipcode, and sqft_living15 are all important factors to consider. 

The RMSE of the validation set is slightly higher compared to the training set, which doesn't suggest overfitting. The RMSE is relatively low, which indicates a good model.

![pic4](https://user-images.githubusercontent.com/81647911/158102358-5a09d6dd-3756-4f99-b0ab-3a176d9a3d23.png)

![pic5](https://user-images.githubusercontent.com/81647911/158102369-73b637d0-ebdd-41e9-a0cf-cb9a507dbd99.png)

##### Discussion & Evaluation
Because of RMSE was low and the corrected R-squared was correspondingly high, the final model was fairly accurate. Many of these characteristics, such as grade, may be used in the actual world. A good grade indicates that the home can be sold for a greater price. Although a grading system may not have been accessible in all counties, other factors such as condition, bathroom, and zipcode are all important and can influence property pricing.

### Predict new prices for new houses

![pic6](https://user-images.githubusercontent.com/81647911/158102826-8a770b8e-b500-4feb-af69-9b79fcfffc68.png)

![pic7](https://user-images.githubusercontent.com/81647911/158102833-3c908ba7-d280-4b20-81e8-4e6799c17de5.png)


Predict record 1: The price of the first record is $410,910.1

![pic8](https://user-images.githubusercontent.com/81647911/158102863-54035432-97ba-48cb-9331-ffb9756ae678.png)

Predict record 2: The price of the second record is $331,777.3

![pic9](https://user-images.githubusercontent.com/81647911/158102870-fdea77b0-c055-4cbe-b887-60959f233e28.png)

Predict record 3: The price of the last record is $343,520.8

![pic10](https://user-images.githubusercontent.com/81647911/158102877-cebb4552-bb3e-4060-83c8-879ffae53ec5.png)
