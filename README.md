# Thermal Demand Modelling
### Household Space Heating Demand Modelling using Simplified Black-Box Models

This repository houses the source code and results of developing a household thermal demand prediction model 


## Table of Contents

- [Project Overview](#projectoverview)
- [Data Description](#datadescription)
- [Technical Overview](#technicaloverview)
- [Results](#results)

***

<a id='projectoverview'></a>
## Project Overview

This research aims at applying a novel idea of utilizing an ANN (Artificial Neural Network) black-box model to predict the space heating demand of households in Toronto, Ontario, Canada.

This research was conducted as a continuation of an ongoing study at the Ryerson Centre for Sustainable Energy Systems (CSES).

Being able to model and predict the space heating needs of a household can help reduce energy consumption, and in turn, reduce the total greenhouse gas emissions from households. 
This can be done by leveraging such information to increase efficiency of heating systems used.

<a id='datadescription'></a>
## Data Description

Ecobee, a Canadian home automation company that produces smart thermostats, sensors for temperature & occupancy detection, smart light switches, smart cameras etc. are one of the players in the market for cutting edge smart-home automation services.

Their advanced smart thermostats in tandem with the smart sensors are capable of detecting occupants in a room, set smart comfort schedules, adjust heating/cooling sources, all according to the user’s preferences in order to boost efficiency and save energy.

The data used is gathered as a part of the Ecobee Donate Your Data program and focusses on a few sample houses from Toronto, Ontario, Canada. The thermostats collect data at a regular interval of 5 minutes.

The raw data for the houses can be referred to here. [Raw Data](https://github.com/ankit-dhall/thermal_demand_modelling/tree/master/raw_data)

Additionally, external weather information from https://climate.weather.gc.ca/ was used and can be found here. [Raw Weather Data](https://github.com/ankit-dhall/thermal_demand_modelling/tree/master/raw_weather_data)

<a id='technicaloverview'></a>
## Technical Overview

Several approaches were used in order to undertand the data and build a predictive model. 

First, an exploratory analysis is conducted using descriptive analytics and data visualization to try and find patterns, or relationships that could help give insight into the data. 
Further, multiple approaches and techniques such as data aggregation and inclusion of time-lag information are applied to model and predict the space-heating demands of any house using basic, easy to record features only. 

In addition, experiments are conducted to gauge the practical viability of the black-box model developed.

The project has been divided into various steps which include:
* Exploratoy Data Analyis & Visualizations [Data Visualization.ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/preprocessing_code/Data%20Visualization.ipynb)
* Pre-Processing & Feature Engineering [Data Wrangling & Pre-Processing.ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/preprocessing_code/Data%20Wrangling%20%26%20Pre-Processing.ipynb)
* Feature Selection [EDA & Feature Selection.ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/preprocessing_code/EDA%20%26%20Feature%20Selection.ipynb)
* Model Training
  * Simple ANN [Simple ANN.ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/modelling_code/Simple%20ANN.ipynb)
  * Data Aggregation
    * Hourly [Hourly Data Analysis House 1.ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/modelling_code/Hourly%20Data%20Analysis%20House%201.ipynb)
    * 2 Hourly [2 Hourly Data Analysis House 1.ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/modelling_code/2%20Hourly%20Data%20Analysis%20House%201.ipynb)
  * Using Previous Time Steps & Treating Bias [ANN Using Previous Time Steps & Treating Bias.ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/modelling_code/ANN%20Using%20Previous%20Time%20Steps%20%26%20Treating%20Bias.ipynb)
  * Including External Weather Information [ANN Testing on Different Houses (Different Model) (30 Minute Time Lag) Extra Weather Sample.ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/modelling_code/ANN%20Testing%20on%20Different%20Houses%20(Different%20Model)%20(30%20Minute%20Time%20Lag)%20Extra%20Weather%20Sample.ipynb)
* Model Tuning
  * Hyperparameter Tuning using Grid Search [ANN Testing on Different Houses (Different Model) (30 Minute Time Lag)-Grid Search.ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/modelling_code/ANN%20Testing%20on%20Different%20Houses%20(Different%20Model)%20(30%20Minute%20Time%20Lag)-Grid%20Search.ipynb)
  * Activation Function Cross Validation [ANN Testing on Different Houses (Different Model) (30 Minute Time Lag)-Cross Validation Activation Funcs.ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/modelling_code/ANN%20Testing%20on%20Different%20Houses%20(Different%20Model)%20(30%20Minute%20Time%20Lag)-Cross%20Validation%20Activation%20Funcs.ipynb)
* Model Testing
  * Final Model Testing [ANN Testing on Different Houses (Different Model) (30 Minute Time Lag).ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/modelling_code/ANN%20Testing%20on%20Different%20Houses%20(Different%20Model)%20(30%20Minute%20Time%20Lag).ipynb)
  * Monthly Improvement of Model [Monthly Improvement House 1 January - December.ipynb](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/modelling_code/Monthly%20Improvement%20House%201%20January%20-%20December.ipynb)

<a id='results'></a>
## Results

The space-heating demand was successfully predicted using black-box ANN models using simple, easy to observe features and including time-lag information for the past half-hour. 
In addition, the model was able to portray a practical learning capability as additional data was added.

For a detailed project report, please refer [Thermal Demand Modelling Report.pdf](https://github.com/ankit-dhall/thermal_demand_modelling/blob/master/Thermal%20Demand%20Modelling%20Report.pdf)