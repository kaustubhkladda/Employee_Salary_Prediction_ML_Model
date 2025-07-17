# Employee_Salary_Prediction_ML_Model

Employee Income Prediction (Classification Project)
This repository contains a complete, end-to-end data science project that predicts whether an individual's annual income is less than or equal to 50K INR or greater than 50K INR. The project covers the entire machine learning lifecycle, from data cleaning and exploratory data analysis to model building, evaluation, and deployment as an interactive web application using Streamlit.

📋 Table of Contents
Project Overview

Dataset

Project Workflow

Technologies Used

Setup and Installation

How to Run the Project

Streamlit App Features

🎯 Project Overview
The primary goal of this project is to build a robust classification model that can accurately predict an individual's income bracket based on a set of demographic and job-related attributes. This can be valuable for various applications, including targeted marketing, financial services, and socio-economic studies. The project emphasizes clean code, reproducibility, and a production-ready deployment.

📂 Dataset
The project uses the ABC.csv dataset, which is a structured file containing various attributes for individuals.

Features: age, workclass, fnlwgt, education, educational-num, marital-status, occupation, relationship, race, gender, capital-gain, capital-loss, hours-per-week, native-country.

Target Variable: income (Binary: <=50K or >50K).

🔄 Project Workflow
The project is structured into a series of well-defined steps:

Data Loading & Initial Exploration: The dataset is loaded, and its basic properties (shape, data types, missing values) are inspected.

Data Cleaning: Placeholder values (?) are handled, and redundant columns (education, fnlwgt) are dropped.

Outlier Detection & Treatment: Outliers in numerical features are visualized using boxplots and capped using the IQR method to prevent them from skewing the model.

Feature Encoding: All categorical features are converted into numerical format using LabelEncoder.

Model Building: Five different classification models (Logistic Regression, Random Forest, KNN, SVM, Gradient Boosting) are trained using scikit-learn Pipelines, which include a data scaling step.

Model Evaluation: The models are evaluated based on Accuracy, Precision, Recall, and F1-Score. Their performance is compared visually.

Model Selection & Saving: The best-performing model (with accuracy ≥ 85%) is selected and saved as best_model.pkl. The label encoders are also saved.

Deployment: The saved model is deployed as an interactive web application using Streamlit.

🛠️ Technologies Used
Programming Language: Python 3.x

Libraries:

pandas & numpy for data manipulation

matplotlib & seaborn for data visualization

scikit-learn for machine learning (modeling, preprocessing, evaluation)

joblib for saving and loading the model

streamlit for building the interactive web application

⚙️ Setup and Installation
Clone the repository:

git clone <repository-url>
cd <repository-directory>

Create a virtual environment (recommended):

python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

Install the required libraries:

pip install pandas numpy matplotlib seaborn scikit-learn joblib streamlit

🚀 How to Run the Project
There are two main components to this project:

1. Running the Jupyter/Colab Notebook
Ensure you have the ABC.csv dataset in the same directory.

Open the .ipynb file in Jupyter Notebook, JupyterLab, or Google Colab.

Run the cells sequentially from top to bottom to execute the entire data science workflow.

2. Running the Streamlit Web Application
Make sure you have the following files in your project directory:

app.py

best_model.pkl

label_encoders.pkl

Open your terminal or command prompt, navigate to the project directory, and run the following command:

streamlit run app.py

Your default web browser will open with the application running locally.

✨ Streamlit App Features
User-Friendly Interface: A clean and intuitive UI built for ease of use.

Two Prediction Modes:

Single Prediction: Users can input individual employee attributes via sliders and dropdowns to get an instant income prediction.

Batch Prediction: Users can upload a CSV file with multiple employee records to get predictions for all of them at once.

Downloadable Results: For batch predictions, the app provides a link to download the results (original data + predicted income) as a new CSV file.
