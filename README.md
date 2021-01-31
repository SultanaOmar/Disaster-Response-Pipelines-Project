# Disaster-Response-Pipelines-Project

## Project Overview:
In this project, I'll apply data engineering to analyze disaster data from Figure Eight to build a model for an API that classifies disaster messages.

## Project details:
1. ETL Pipeline
File data/process_data.py is data cleaning pipeline that:
* Loads the messages and categories dataset
* Merges the two datasets
* Cleans the data
* Stores it in a SQLite database

2. ML Pipeline 
File models/train_classifier.py is machine learning pipeline:
* Loads data from the SQLite database
* Splits the data into training and testing sets
* Builds a text processing and machine learning pipeline
* Trains and tunes a model using GridSearchCV
* Outputs result on the test set
* Exports the final model as a pickle file

## Running
* The first step:
python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
* Then 
python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl
* Then
python app/run.py 

