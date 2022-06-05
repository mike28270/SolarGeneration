# SolarGeneration

## Introduction
With the increase of renewable energy generation and decentralized in power grids for instance wind farms and solar plants, dynamical stability of power grids becomes more important and challenging. In order to maintain stability of power grids, the data will be analyse and focus on the prediction of the values.

## Description
• The data collected from two solar power plants in India over a 34 day period.
• Each of the plants consists of two datasets which are a power generation dataset recorded by inverters and a weather dataset gathered by sensors at solar panels.
• The task is to predict energy produced daily by solar power plants.

## Data source
The dataset can be found and download at Kaggle via a topic called Solar Power Generation Data. [link](https://www.kaggle.com/anikannal/solar-power-generation-data)

1. Power generation dataset contains seven columns.

| Columns     | Data Type | Description                                                  |
| ----------- | --------- | ------------------------------------------------------------ |
| DATE_TIME   | String    | Date and time recorded every 15 minutes                      |
| PLANT_ID    | String    | Solar power plant ID                                         |
| SOURCE_KEY  | String    | Inverter ID                                                  |
| DC_POWER    | Float     | DC power generated by the inverter                           |
| AC_POWER    | Float     | AC power generated by the inverter                           |
| DAILY_YIELD | Float     | Energy generated by the inverter on that day until DATE_TIME |
| TOTAL_YIELD | Float     | Total Energy generated by the inverter                       |

2. Weather Sensor dataset contains six columns.

| Columns             | Data Type | Description                                           |
| ------------------- | --------- | ----------------------------------------------------- |
| DATE_TIME           | String    | Date and time recorded every 15 minutes               |
| PLANT_ID            | String    | Solar power plant ID                                  |
| SOURCE_KEY          | String    | Inverter ID                                           |
| AMBIENT_TEMPERATURE | Float     | Ambient temperature at the plant                      |
| MODULE_TEMPERATURE  | Float     | Solar panels temperature                              |
| IRRADIATION         | Float     | Amount of radiation which solar panels was exposed to |

## Steps
The process consists of 3 steps.
1. [Initialize Database](./01_InitializeData.ipynb):
- Create table
- Import Data
2. [Data Cleaning](./02_CleaningData.ipynb):
- Dealing with Null
- Merge tables
- Dealing with Data type
3. [Data analyzation](./03_Analyse_202112062348.ipynb): 
- Inverter optimization
  - Find efficiencies of the inverters
  - Find the faulty inverter
- Prediction of AC_POWER
