# Carbon Dioxide Emission Prediction
## Introduction:
#### Global warming is one of the biggest challenges currently being faced by the human race, although correlation is not causation a likely cause of global warming is due to increased atmospheric carbon dioxide from human activities.

#### The Project Carbon Dioxide Emission Prediction based on features of Engines is an innovative approach to predicting carbon dioxide emissions from vehicles based on engine features. As the world continues to grapple with the challenges posed by climate change, the transportation sector has come under increasing scrutiny for its significant contribution to greenhouse gas emissions, particularly carbon dioxide.

#### This project aims to provide a more accurate and efficient way to estimate carbon dioxide emissions from vehicles, which can help governments, businesses, and individuals make more informed decisions about their transportation choices. By analyzing various engine features such as displacement, power, and fuel type, the project can predict carbon dioxide emissions with a high degree of accuracy.

#### Passenger cars produced approximately three billion metric tons of carbon dioxide emissions worldwide in 2020. The emissions produced by passenger cars have been steadily rising over the past two decades, increasing from 2.2 billion metric tons in 2000 to a peak of 3.2 million metric tons. Emissions fell roughly six percent in a 2020 as a result of the COVID-19 pandemic, which caused major disruptions to transportation.

#### Overall, the Project Carbon Dioxide Emission Prediction based on features of Engines has the potential to make a significant contribution to reducing greenhouse gas emissions from the transportation sector and promoting a more sustainable future for all.

## Deliverables:
#### The benefits of this project are significant. Firstly, it will help individuals and businesses make informed decisions when purchasing vehicles, by providing a clearer understanding of the carbon footprint associated with different engine types. Secondly, it will assist policymakers in developing more effective regulations and incentives aimed at reducing carbon emissions from the transportation sector.

#### Furthermore, this project can also be helpful for the automobile industry in a number of ways. It can assist manufacturers in developing more fuel-efficient and environmentally friendly engines, which can increase their market share and competitiveness. Additionally, it can help companies comply with increasingly stringent emissions regulations, thereby avoiding penalties and reputational damage.

## Objective:
#### The goal of this project is to predict CO2 emissions in g/km produced by any vehicle based on several car engine features.

## Raw Dataset:
#### https://drive.google.com/file/d/1lHO9-JDoDWiibbw3KUXAQfeC-UWHLuwQ/view?usp=share_link

## Cleaned Dataset:
#### https://drive.google.com/file/d/1ccnKkziNzDk4TeCihwal-q3uxp0RrwG0/view?usp=share_link

## Preprocessed Dataset:
#### https://drive.google.com/file/d/1OmfYRE-GlK4Cg64e4PxhYhhRkDr5ivWd/view?usp=share_link

## About Dataset:
### Content
#### This dataset captures the details of how CO2 emissions by a vehicle can vary with the different features. The dataset has been taken from Canada Government official open data website. This is a compiled version. This contains data over a period of 7 years.
#### There are total 7385 rows and 12 columns. There are few abbreviations that has been used to describe the features. I am listing them out here. The same can be found in the Data Description sheet.

#### Model:
####    1) 4WD/4X4 = Four-wheel drive
####    2) AWD = All-wheel drive
####    3) FFV = Flexible-fuel vehicle
####    4) SWB = Short wheelbase
####    5) LWB = Long wheelbase
####    6) EWB = Extended wheelbase


#### Transmission:
####    1) A = Automatic
####    2) AM = Automated manual
####    3) AS = Automatic with select shift
####    4) AV = Continuously variable
####    5) M = Manual


#### Gears:
####    3 - 10 = Number of gears


#### Fuel type:
####   1) X = Regular gasoline
####   2) Z = Premium gasoline
####   3) D = Diesel
####   4) E = Ethanol (E85)
####   5) N = Natural gas

#### Fuel Consumption City and highway fuel consumption ratings are shown in litres per 100 kilometres (L/100 km) - the combined rating (55% city, 45% hwy) is shown in L/100 km and in miles per gallon (mpg)

#### CO2 Emissions The tailpipe emissions of carbon dioxide (in grams per kilometre) for combined city and highway driving.

## Aknowledgements:
#### The data has been taken and compiled from the below Canada Government official link
####  https://open.canada.ca/data/en/dataset/98f1a129-f628-4ce4-b24d-6f16bf24dd64#wb-auto-6

## Tools:
#### Python: Jypyter Notebook

## Project Summary:
### 1. EDA
####    From the data I came to know that:                                There are some dupluicate values in the dataset                            There are no null values                                                      Quantitative data consists of outliers                                          There is multicollinearity problem in the data.
#### EDA Report: https://anilwaded-carbon-dioxide-emission-prediction--eda-report-8g01uh.streamlit.app/

### 2. Data Preprocessing
#### In this script
#### I have removed the duplicate values.                                      I have detected the outliers with the help of Z-Score and IQR method and treated them by Quantile based flooring and capping.

#### After preprocessing, data lookd like: https://drive.google.com/file/d/1ccnKkziNzDk4TeCihwal-q3uxp0RrwG0/view?usp=share_link

### 3. Feature Engineering
#### Since data is highly correlated within explanatory variables, I have used SelectKBest method and RFM method for feature selections.

#### After Feature Engineering, data looks like: https://drive.google.com/file/d/1OmfYRE-GlK4Cg64e4PxhYhhRkDr5ivWd/view?usp=share_link

### 4. Model building and Evaluation
#### I have build the model with 8 different ML Algorithms:
#### a) Linear Regression
#### b) Ridge Regression
#### c) Lasso Regression
#### d) Decission Tree Regressor
#### e) Random Forest Regressor
#### f) Gradient Boosting
#### g) Xtreme Gradient Boosting
#### h) Support vector Machine and also build with
#### i) Artificial Neural Networks
#### Among these Xtreme Gradient Boosting and ANN fits the best with R2 score of 99.8%.

### 5. Deployment
####      I have deployed Xtreme Gradient Boosting Model in Streamlit Cloud

####      Script: https://github.com/Anilwaded/Carbon_Dioxide_Emission_Prediction_Project_Deployment/blob/main/README.md


## Conclusion:
#### From the model performance metrics, it appears that 99.8% of the variance in the CO2 Emissions can be determined by the features within our model. While this model has good performance, we simplified the model by omitting several key categorical variables. It would be interesting to see if there is way to retain them within the model, and gain further insights.

