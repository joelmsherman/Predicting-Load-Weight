# Predicting Vehicle Load Weights
![image](https://github.com/joelmsherman/Predicting-Load-Weight/blob/master/Images/ReadmeTitle.png)

## Background
ABC Waste Inc's revenues depend largely on the ability to apply an accurate weight (in tons) to established specific tonnage fees, transaction fees, and and government taxes.  To do this, ABC uses certified vehicle scales (to within +/- .01 tons, or 20lbs) to record weights. In addition to weight, ABC's scalehouse attendants collect additional information about each load, including information about the vehicle (truck number, type), customer, station, and its timestamp (date and time of arrival).  Since mid-2012, ABC's database contains well over 4 million records.

## Objective
The objective of this analysis is to train, validate, test and deploy a machine learning (ML) model that will predict load weight in the event of a temporary scale outage or malfunction, based on readily observable features of the load.  The end product must be accessible to scalehouse staff on battery-powered devices, be easy to use, performant, and accurate.  

## Methods
The analysis is conducted in the following steps.

### Data Extraction and Prep
Over 4 million records were extracted from ABC's point-of-sale system between June 1, 2012 and January 31, 2023, for analysis of feature distributions, and the variation of those distributions with respect to load weight.  

### Data Analysis
An exploratory analysis of the data is available [here](https://app.hex.tech/5b266aaf-b343-4ae7-bdea-218e8fe3001f/app/ebbe87e0-62ac-4086-b362-3a2fada84f9b/latest).

### Machine Learning
A baseline and 4 alternative regression models were trained and tested.  The goal was to find a most parsimonious, best-fitting model that accurately predicted weights.  Parsimony will be important when the model is deployed into the field, as they will allow staff to make minimal observations and generate predictions very quickly. An analysis of the ML experiments, including pre-processing steps, test harness and experiment results are available [here]().

## Results
The final model was able to accurately predict load weight.  The Mean Absolute Error (MAE) of the 277K holdout loads was about .03 tons.  On a total tonnage basis, the model predicted 382,200 tons, in comparison to the 382,000 actual tons in the sample. A consolidated summary presentation of the analysis is available [here](https://www.beautiful.ai/player/-NXNAsMpTJbK0JcUkRhR).

## Value Proposition
ABC can deploy and immediately rely on the model to predict weights and collect fees reliably and accurately, saving ABC and its customers significant costs during scale outages, over guessing.  ABC's transfer stations receive over 1,200 customers and 1,800 tons of material every day, which translates to well over $120,000 in revenue per day.  If a scale goes down for a single day, and ABC assigns weights arbitrarily or through guesswork, signifcant opportunity costs are at stake.  These include forgone revenue for ABC if weights are under-assigned, and sigificant costs for customers if over-assigned.  This model can predict weight to within .03, and represents an immediate value-add to ABCs operational assets.   
 

