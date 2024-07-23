# Time Series Analysis and PM2.5 Forecasting using Air Quality Monitoring Data in Athens Greece
## Overview
This repository contains the project that serves as the finals for our machine learning class. The project involves monitoring air quality data in Athens, Greece, with a focus on time series analysis and multivariate forecasting of PM2.5 levels using various machine learning and deep learning algorithms.

## Main Objectives
- Analyze air quality data from Athens as time series data.
- Evaluate and compare the performance of different models on various schemes.

## Data Description
The dataset used is "Regional Datasets for Air Quality Monitoring in European Cities" published at the 2024 IEEE IGARS-24 or IEEE International Geoscience and Remote Sensing conference on July 7-12 in Athens, Greece. The dataset is also available via the [Kaggle](https://www.kaggle.com/datasets/yekenot/air-quality-monitoring-in-european-cities) platform by the user Vladimir Demidov. The data features details are also provided in the data card.

## Methods
The project workflow more or less follows the given flowchart:
![image](https://github.com/user-attachments/assets/c1c5e5bb-e206-475d-ad84-196c414bf7c2)

Explanation:
1. Data Analysis, self-explanatory.
2. Data Preprocessing, create temporal features and handle outliers.
3. Model Construction/Initialization, models used are Linear Regression, Random Forest, XGBoost, and LSTM with the given architecture:
![image](https://github.com/user-attachments/assets/4c0a39ef-e1f6-48fa-a5b6-643078e07e02)

5. Compare and Evaluate models on various schemes, most of the schemes are pretty straightforward but there is one scheme that is worth noting, namely scheme 4.

![image](https://github.com/user-attachments/assets/32e0c64b-17f6-489a-b6d6-788e3346b033)

After a bit of testing, we found out that the model is having a hard time predicting fluctuations or extreme values in the data. So the intention here is that, by using bagging, we can compensate for the tendency of the model to underpredict the values without going off too much from the ground truth.

- w/o bagging

![image](https://github.com/user-attachments/assets/582bd82a-dd1d-4892-a6db-abb9f0d0066e)

- with bagging

![image](https://github.com/user-attachments/assets/8e784ae9-7cc8-4e37-ad99-c250f0554402)

## Acknowledgments
Special thanks to my colleagues, [Keanu Fortuna Taufan](https://github.com/keanutaufan) and [Zelvan Abdi Wijaya](https://github.com/zelvann), and to our machine learning class lecturer, Dini Adni Navastara, S.Kom, M.Sc., and the teaching assistants for their support and guidance throughout this project.
