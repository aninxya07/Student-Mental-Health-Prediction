# Student Mental Health Prediction

This repository contains a machine learning project aimed at predicting the mental health status of students, specifically whether a student is depressed or not. It uses a Random Forest Classifier to analyze various features such as academic pressure, work pressure, CGPA, sleep duration, and other demographic details to predict the depression status.

## Files in this Repository

- **`app.py`**: A Streamlit application for predicting a student's depression status based on user input.
- **`random_forest_model.pkl`**: The trained Random Forest model serialized using `joblib` that is used for predictions in `app.py`.
- **`student_depression_dataset.csv`**: The dataset used for training the model. It contains various features and a target variable indicating whether a student is depressed or not.
- **`student-mental-health.ipynb`**: A Jupyter notebook that demonstrates the data preprocessing, model training, and evaluation steps performed on the dataset.
- **`gitignore`**: A file specifying which files or directories should be ignored by Git.
- **`license`**: The license file for this repository.

## Project Overview

The dataset includes features such as:
- **Gender**
- **Age**
- **Academic Pressure**
- **Work Pressure**
- **CGPA**
- **Study Satisfaction**
- **Job Satisfaction**
- **Sleep Duration**
- **Suicidal Thoughts History**
- **Work/Study Hours**
- **Financial Stress**
- **Family History of Mental Illness**
- **City**
- **Profession**
- **Dietary Habits**
- **Degree**

The target variable is `Depression`, indicating whether the student is depressed or not.

## Installation

To run the project locally, you will need the following Python libraries:

```bash
pip install -r requirements.txt
