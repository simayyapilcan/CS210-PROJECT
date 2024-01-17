# Apple Health Data Analysis 🏥

![Image](/header.jpg)

## This project aims to analyze Apple Health data to gain insights and extract meaningful information from personal health and fitness metrics.

## Table of Contents 📋

- [Introduction](#introduction)
- [Motivation](#motivation)
- [Features](#features)
- [Data Source](#data-source)
- [Data Preprocessing](#data-preprocessing)
- [Data Analysis](#data-analysis)
- [Results](#results)
- [Limitations and Future Work](#limitations-and-future-work)
- [License](#license)

## Introduction 🎬

In this project, we leverage Apple Health data to explore various aspects of personal health and fitness. By analyzing the data, we aim to uncover patterns, trends, and correlations that can provide valuable insights into our well-being.

## Motivation 🚀
Most of us have the health app pre-installed on our mobile phones, However, we do not look in to our data in depth. Also most of the health apps, does not show the entire data visually for the sake of simplicity. Hence, we are limited to insights created by those applications. This project aims to dive deeper into the personal health data and gain insights by applying various techniques.

## Data Source 💿
Apple Health App is used to extract the data. This app has various sources. The main one is my iPhone, others are my Apple Watch and other well-being apps connected to Apple Health app such as YAZIO.

## Data Preprocessing 🤖

Extracted data from the Apple Health App comes as an XML format file. Hence, I used extractor Python file made by community. After extracting all the events as a CSV file, manually checked them for the data sufficiency. Since, data length can vary across different events, manually checking the files seems the bes option to determine the value of the data.

After identifying necessary datas, I started to remove irrelevant columns from the dataset, handle the data formats and converted the  to datetime objects and lastly grouped the session datas daily in order to visualize them properly.

## Data Analysis 🧐

I used exploratory data analysis and visualization techniques to gain insights about my health. Due to inconsistency among the timeframes of the datas made the common date range so narrow that training a ML model would be meaningles due to lack of data. 

## Features 🕹️

- Data import and preprocessing
- Exploratory data analysis
- Visualization of health metrics
- Statistical analysis and modeling
- Findings and conclusions


## Results 📇

In this section, we will summarize the key findings and insights obtained from the analysis of the Apple Health app data. The analysis focused on [mention the specific metrics or aspects you analyzed, e.g., steps, heart rate, sleep patterns].

1. Hearth Rate Analysis ❤️

- The analysis of heart rate data aimed to uncover patterns and relationships with other health activities. A key finding is that most heart rate readings fall within normal ranges, with only one exceptionally low value at 40 bpm.
- A comprehensive "Health Score" was developed using metrics like Steps, Heart Rate, Burned Energy Active, and Flights Climbed. This score, ranging between 0 and 100, reflects overall health. The Gradient Boosting Regressor, after comparing various models, was found to be the best in predicting this health score.

2. Physical Activities Analysis 🏃🏼‍♀️

- The analysis reveals that my average daily steps are quite sufficient, reflecting my active engagement in sports activities. This is further supported by the average calories spent each day.
- Notably, when examining outliers in the step count data, I realized these instances corresponded to specific events, indicating higher than usual physical activity during these times.

3. Audio Exposure Analysis 🔊

- An examination of the red zones in my audio exposure data showed that these higher exposure levels mostly occurred during periods of study or sports activities.
- Overall, my audio exposure levels are not excessively high, suggesting a balanced auditory environment in my daily life.

4. Sleep Analysis 😴

- Due to limited data availability, a comprehensive analysis of my sleep patterns was challenging. However, from the available data and my personal experiences, it seems that my sleep quality is not optimal.
- The preliminary observations indicate irregularities in sleep duration and possibly quality, which may be an area for further investigation and improvement.




## Limitations and Future Work 💼

The major problem which constrained my analysis was inconsistency among the data intervals. Until now I did not realized the quality of my health data since the app handles it. However, after I got my hands dirty with the data, I realized that it would be more beneficial If I were checking my health app on regular basis and use it every day to check the success of the data collection and input manual data such as nutritions. Hence, after collecting data every day for one year, I will be able to concatenate all my health data in one dataframe and then make future predictions on my health using various machine learning and ai.
