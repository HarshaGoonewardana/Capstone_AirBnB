# AirBnB
Capstone project for Data Science Immersive at General Assembly

## Capstone project – Inference and prediction on  Airbnb rental yields in New York City and Washington D.C 

### Overview ###
Airbnb is a peer to peer accommodation rental platform with 5 million listing across 191+ countries. The platform has more rooms available at a given time than top five hotel chains combined n 2018 . This project aims to first determine the feature importance of a number of variables to the rental yield followed by a deployment of a model to predict rental yields. 

The effects of Airbnb on the dynamics of the real estate market markets in the USA , especially with the pricing structure around short-term rentals is a particularly interesting areas. The factors which affect pricing decisions remain localized and opaque, the comparison study expects to identify structural differences between markets, especially since accommodation on aggregate has a perfectly inelastic demand curve. The supply is mutable as external supply shock is present in reserve in the form of extra unused capacity in existing dwellings.

This project will identify the features which have the most statistical significance on determining property values. Within that frame, the project will further isolate the significance of descriptive, geo-spatial and other features to understand the influence of each category. Finally, a predictive model will be deployed to advise hosts on strategies to maximize the yield disaggregated by neighborhoods

Yield as a dependent variable <b>
While academic research uses the listing price as the dependent variable, the approach is inadequate to capture the equilibrium price at which the transaction is made. As the supply and demand cycle needs to adjust over time , the supply-side variable necessitates the  presence of a tuning parameter. A new feature incorporating occupancy rate (estimated using length of stay and reviews) and listing price mitigates these issues and provides a more accurate measure of yield. 

### Dataset ###
Following the lead from number of researchers in the field, the project uses the dataset from insideairbnb.com for New York City. 
The Inside Airbnb dataset contains 47542 unique listing locations from on 20th January 2009 to 15 May 2018.There are 95 separate features in a variety of types and 18 have been selected for further examination (see Appendix I). New York Transit Authority dataset contains the longitude and latitude of each metro station within New York and will provide the distance to the closest transit point from each Airbnb rental location.

An active listing is defined as a property which has received at least one review in the last year and has availability for the next year . 

### Rental yield = Review_rate X  Occupancy_rateX Total_price ###

The influential study conducted by the San Francisco City Council incorporates 72% as the percentage of users leaving a review after a stay while Airbnb claims a 75% review rate. In the sake of conservatism, the former rate is used for the calculation .The average length of stay was used for the calculation along with the list price per night as advertised. The total price is the financial outlay per stay whuch included the variable lodging costs plus the fixed cost of cleaning . 

### Analytical Process ###
The dataset is quite noisy with a large number of null, mislabeled, and irrelevant features. The original 94 features were narrowed down to a shortlist of 26  for analysis.

Model which are prone to over-fitting were used on sparse datasets while more robust models were utilized on data augmented datasets with approximately 350 features. 

linear regression, Ridge and Enet parameter tuning and neural net were used for prediction.

### Results ###
Both the datasets were very noisy with both the price and the bnb_yield signals becoming lost in the noise, none of the models achieved more than a 0.68 Cross Validation score.

The model did not provide noticably better results than the baseline for prediction of yields. However the model was able to predict within $70 of the list price, which is an improvement on the dataset mean of $178

### Next steps ###

The project expects to tune the neural net further and also compare the results with an analysis of the Washington D.C dataset

datasource: http://insideairbnb.com/






# Capstone
