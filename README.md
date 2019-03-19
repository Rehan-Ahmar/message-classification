# Disaster Response Pipeline Project - Multi-label Classification of Messages

## Table of Contents

1. [Project Motivation](#motivation)
2. [Installation](#installation)
3. [File Structure](#files)
4. [Usage Instructions](#usage)
5. [Output](#output)
6. [Acknowledgements](#acknowledgements)


<a name="motivation"></a>
## Project Motivation
This project was created as part of Udacity's Data Scientist for Enterprise nanodegree.

The main objectives of this project were the following:
  - An ETL pipeline for loading data from csv files, transforming and cleaning the data, and finally storing it to an sqlite database.
  - A Machine learning pipeline to predict the categories of different messages recorded during natural disasters.
  - A web app that displays few visualisations of the data and classifies new input messages into multiple categories.


<a name="installation"></a>
## Installation

The code should run using any Python versions 3.*. I used python 3.6.

Libraries Used : numpy, pandas, sklearn, nltk, sqlalchemy, plotly, flask, bootstrap


<a name="files"></a>
## File Structure

    - app
    | - template
    | |- master.html  # main page of web app
    | |- go.html  # classification result page of web app
    | - run.py  # Flask file that runs app, contains code for visualization and prediction.
    
    - data
    |- disaster_categories.csv  # data to process
    |- disaster_messages.csv  # data to process
    |- process_data.py   # ETL Pipeline
    |- DisasterResponse.db   # database to save clean data
    
    - models
    |- train_classifier.py   # Machine Learning Pipeline
    |- classifier.pkl  # saved model
    
    - notebooks   # contains Jupyter notebooks used to create ETL and ML Pipelines.
    - README.md


<a name="usage"></a>
### Usage Instructions
    1. Run the following commands in the project's root directory to set up your database and model.
        - To run ETL pipeline that cleans data and stores in database
            `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
        - To run ML pipeline that trains classifier and saves
            `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

    2. Run the following command in the app's directory to run your web app.
        `python run.py`
    
    3. Go to http://localhost:3001


<a name="output"></a>
### Output
In the web app, user can input a new message and get the predicted categories.

![alt text](https://github.com/Rehan-Ahmar/message-classification/blob/master/assets/1.PNG)
![alt text](https://github.com/Rehan-Ahmar/message-classification/blob/master/assets/2.PNG)

The web app also shows some visualizations for the training data in database.

![alt text](https://github.com/Rehan-Ahmar/message-classification/blob/master/assets/3.PNG)
![alt text](https://github.com/Rehan-Ahmar/message-classification/blob/master/assets/4.PNG)
![alt text](https://github.com/Rehan-Ahmar/message-classification/blob/master/assets/5.PNG)


<a name="acknowledgements"></a>
## Acknowledgements
Thanks to [Figure Eight](https://www.figure-eight.com/) for the data, and [Udacity](https://in.udacity.com/) for course material.