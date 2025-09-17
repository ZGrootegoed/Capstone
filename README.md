# Capstone
Zachary Grootegoed

This public repository was set up for storing the jobs csv file and the ipynb file so that it can get hosted on Binder then go into a hosted JuypterLab page.

Origin of csv data file:
https://www.kaggle.com/datasets/PromptCloudHQ/us-technology-jobs-on-dicecom/data

Google Colab Link:
https://colab.research.google.com/drive/1kssoga2Tt6zUFbQS-Ft1ByZ-Kt8lEgJL?usp=sharing

Binder Link:
https://2i2c.mybinder.org/v2/gh/ZGrootegoed/Capstone/main

# Capstone Project: US Technology Jobs Analysis

## Overview
This project performs data analysis and machine learning on a dataset of US technology job listings sourced from Dice.com via Kaggle. The goal is to extract insights about job titles, locations, and skills, and to build a predictive model for job categories based on skills.

## Dataset
- **Source:** [Kaggle: US Technology Jobs on Dice.com](https://www.kaggle.com/datasets/PromptCloudHQ/us-technology-jobs-on-dicecom/data)  
- **File:** `dice_com-job_us_sample.csv`  
- **Structure:** Includes columns such as `job_title`, `company`, `location`, `skills`, `date_posted`, and `job_description`.  
- **Size:** 22,000 rows

## Technical Approach

### 1. Data Preprocessing
- Loaded CSV data using **Pandas**.  
- Handled **missing values** and **data inconsistencies** in `skills` and `location`.  
- Standardized text fields (lowercasing, stripping whitespace).  
- Tokenized the `skills` column for frequency analysis.  

### 2. Exploratory Data Analysis (EDA)
- Generated distributions for **job titles**, **locations**, and **skills**.  
- Visualized top job titles and skills using **Matplotlib** and **Seaborn**.  
- Identified patterns and correlations between location, skills, and job types.

### 3. Feature Engineering
- Converted `skills` column into a **binary matrix** using **CountVectorizer**.  
- Encoded `job_title` or `job_category` as target labels using **LabelEncoder**.  
- Created **top-N skill frequency features** to reduce dimensionality.  

### 4. Machine Learning
- Split data into **training and testing sets**.  
- Trained a **multiclass classifier** (e.g., Logistic Regression or Naive Bayes) to predict job categories based on skills.  
- Evaluated model using **accuracy, precision, recall**, and **confusion matrix**.  
- Highlighted the top features (skills) influencing predictions.

### 5. Output & Visualization
- Displayed **most common job titles** and **skills distribution**.  
- Generated **plots for skill importance** in predicting job categories.  
- Provided interactive visualizations within **Jupyter Notebook**.

## Files & Notebooks
- `jobsML.ipynb` – Main notebook performing data preprocessing, EDA, and ML modeling.  
- `kernelRequirements.ipynb` – Notebook specifying Python dependencies.  
- `dice_com-job_us_sample.csv` – Raw dataset.

## How to Run
1. Clone repository:  
   ```bash
   git clone https://github.com/ZGrootegoed/Capstone.git
   cd Capstone
