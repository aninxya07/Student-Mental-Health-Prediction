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

```
## Running the App
After installing the necessary dependencies, you can run the Streamlit app to interact with the model. Follow these steps:

Navigate to the project directory in your terminal.
Run the following command to start the Streamlit app:
```bash
streamlit run app.py
```
Streamlit will start the local server and provide a URL like http://localhost:8501 where you can access the app in your web browser.

## Using the App
Once the app is running, you will be prompted to input several features such as:

Age: The student's age.
Gender: The student's gender.
Sleep Duration: The student's typical sleep duration (mapped to numerical values like 1, 2, 3, 4).
Academic Pressure: The perceived level of academic pressure.
Work Pressure: The perceived level of work pressure.
CGPA: The student's current CGPA.
Financial Stress: The perceived level of financial stress.
The model will use these inputs to predict whether the student is likely to suffer from depression, and the result will be displayed as "Depressed" or "Not Depressed."

## Training the Model
If you wish to retrain the model with new data or update the existing model, follow these steps:

Open the Jupyter Notebook student-mental-health.ipynb.
Ensure that the Student Depression Dataset.csv is located in the same directory as the notebook or provide the correct path to the dataset.
The notebook performs the following actions:
Loads the dataset.
Handles missing values.
Encodes categorical variables.
Scales numerical features.
Trains the RandomForestClassifier model.
Saves the trained model as random_forest_model.pkl.
Once the model is trained and saved, you can use it in your Streamlit app by loading the random_forest_model.pkl file.

## Example of Data Preprocessing
Here’s an overview of the key preprocessing steps performed in the notebook:

## Handle Missing Values:
The column Financial Stress is filled with the median value for missing entries.
Encode Categorical Variables:
Binary categorical variables (Gender, Have you ever had suicidal thoughts?, Family History of Mental Illness) are label-encoded.
Multi-category features like City, Profession, Dietary Habits, and Degree are one-hot encoded.
Scale Numerical Features:
The features such as Age, Academic Pressure, CGPA, Work Pressure, and others are scaled using StandardScaler for uniformity and optimal performance during training.

## Train the Model:
A RandomForestClassifier is trained on the preprocessed data.
The trained model is saved as random_forest_model.pkl using joblib.

License
This project is licensed under the MIT License - see the LICENSE file for details.
