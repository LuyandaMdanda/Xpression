# Xpression

Project Xpression: A winning hackathon project I worked with a team on to win The Teradata Labs Artificial Intelligence and Cognitive Services Hackathon 2017 as a freshman at UC San Diego. This is my personal copy. I specialized on the implementation of Aster analytics software. I created two classification models using two different techniques, General Linear Model and A Support Vector Machine. Once we identified that the SVM yield the most accurate results, we used that to classify the drivers into one of ten categories of distraction levels.


--------------------------------------------------------------------------------
             _   _ _____ _____ _____ _____ _____ _____ _____ _____              
            \ \ / /  _  |  _  \  ___|  ___|  ___|_   _|  _  |  _  |             
             \ v /| |_| | |_| / |___| |___| |___  | | | | | | | | |             
              | | |  ___|  _  \  ___|___  |___  | | | | | | | | | |             
             / ^ \| |   | | | | |___ ___| |___| |_| |_| |_| | | | |             
            /_/ \_\_|   |_| |_|_____|_____|_____|_____|_____|_| |_|             
--------------------------------------------------------------------------------
Machine Learning application using AWS Rekognition and Teradata Aster used to 
classify drivers into one of ten categories, each representing different levels
of distraction.
--------------------------------------------------------------------------------
Dependencies:
  - AWSCLI
    - Access to AWS Rekognition
  - Teradata Services
    - Access to Teradata Aster
    - Access to TDBMS
--------------------------------------------------------------------------------
Program Overview:
  There are several portions of the pipeline that need to be run in order to
  preprocess data, store it, and then operate on it using Aster. 

  1. Preprocessing
  - Ensure AWSCLI is set
    up with the proper credentials.
  - Run utility.py's functions as appropriate. It uses RekognitionInterface's 
    definitions to use pass images through AWS Rekognition. The returned
    results can be placed in a CSV file for easy importing into a Teradata
    database.

  2. Storing data
  - Once the database is set up, run TestImages.py to place the data into the
    database using a SQL query.

  3. Using Aster
  - Use the SVM function on the imported data to classify image features.
--------------------------------------------------------------------------------
