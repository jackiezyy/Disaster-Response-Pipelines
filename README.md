# Disaster-Response-Pipelines

## File Descriptions
1. models/process_data.py:
The script takes the file paths of the two datasets and database, cleans the datasets, and stores the clean data into a SQLite database in the specified database file path.

2. models/train_classifier.py:
The script takes the database file path and model file path, creates and trains a classifier, and stores the classifier into a pickle file to the specified model file path.

3. Flask Web App is the web application the employees can use during emergencies to classify messages into respective categories. The web app also displays visualizations of the data.

4. models/ETL Pipeline Preparation.ipynb: ETL python notebook to generate process_data.py

4. ML Pipeline Preparation.ipynb: ML python notebook to generate train_classifier.py


### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python models/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db model.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
