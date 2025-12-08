# DataScienceProject
Project in the Data Science course.

## INTRODUCTION
Spotify is the worlds largest music streaming platform. Understanding and predicting what made the top songs of the previous year can be of benefit to stakeholders as well as music enthusiasts. The main objective of this project was to use machine learning to predict:

Track Score - which Spotify calculates using a hidden algorithm

Explicit Track - which could automatically mark tracks as explicit

## DATA
- Data of the 4600 most streamed songs on Spotify was gathered
- Pregathered data was taken from Kaggle [1]
- Additional data was gathered using Spotify’s open API
- A total of 30 numerical, nominal and boolean features
- There were almost no linear correlations between metrics of different platforms

[1] https://www.kaggle.com/datasets/nelgiriyewithana/most-streamed-spotify-songs-2024/data

## METHODS USED

- Data processing methods: standardization, one- and multi-hot encoding, combining same metric features
- Methods of analysis: correlation matrices, frequency distributions, plotting of different features
- Features were predicted using statistical and neural link models
- Explicit Track was best modeled by Random Forest Classifier
- Track Score was best modeled by Linear Regression

## FINDINGS

Explicit Track prediction accuracy:
- Random Forest Classifier - 0.765
- Neural Link Model - 0.775
Track Score prediction MSE:
- Linear Regression - 0.374
- Neural Link Model - 0.141

# How to run

1. Kaggle.csv - dataset from
https://www.kaggle.com/datasets/nelgiriyewithana/most-streamed-spotify-songs-2024/data
2. InitialAnalysis.ipynb - contain the initial analysis for the validity of the dataset
3. DataMining.ipynb - uses Spotify’s open API to gather additional data on the songs artists genres (because Spotify does not have song genres). Add your Spotify Developer id and secret to authenticator to run.
4. Mined_data.csv - data gathered using Spotify’s open API
5. DataCombining.ipynb - combines the kaggle and mined datasets, combines features of the same metrics and applies initial data processing. Creates Standardized_data.csv, Normalized_data.csv and Averaged_data.csv which have the combined datasets respectively standardized, normalized and averaged together.
6. Standardized_data.csv, Normalized_data.csv and Averaged_data.csv are the complete datasets with which the analysis and modelling are done
7. Analysis.ipynb - contains the analaysis on the full data using graphs and plots
