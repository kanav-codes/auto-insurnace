# 🚗 Auto Insurance Claims Analysis & Predictive Modeling (2024)
🚗 Auto Insurance Claims Analysis & Predictive Modeling (2024)An end-to-end data analysis and machine learning project built on the AutoInsuranceClaims2024.xlsx dataset. This repository covers data cleaning, exploratory data analysis (EDA), customer segmentation, customer churn prediction, and Customer Lifetime Value (CLV) modeling.  
# 📂 Dataset Information
I have provided the AutoInsuranceClaims2024.xlsx file used in this project directly in the repository. However, if you would like to access the source dataset or explore the original data, you can find it here:
[(https://www.kaggle.com/datasets/thebumpkin/auto-insurance-claims-updated-to-2024)] 

# 🛠️ Setup & Installation
To run this project locally, ensure you have Python installed along with the required libraries.Clone the repository or download the project files.Install the required dependencies:Bashpip install pandas numpy matplotlib seaborn openpyxl

Ensure dataset placement:

Place the dataset file named AutoInsuranceClaims2024.xlsx in the root directory of your project folder.  🚀 How to Run the ProjectOpen your terminal or Jupyter Notebook.Load the main script or notebook file.Run the data preprocessing and visualization blocks sequentially:Pythonimport pandas as pd
import numpy as np

# Load the dataset
df = pd.read_excel("AutoInsuranceClaims2024.xlsx")
Execute the visualization blocks to generate the clean charts for your report or dashboard.

# 📋 Project Decisions & Methodology1. 
Data Cleaning & Feature Engineering

Feature Reduction: Dropped redundant identifier columns (such as customer IDs and index columns) to streamline the feature space and avoid data leakage.

Addition of Derived Columns (Feature Engineering):

Binary Churn Column: Derived from the original categorical Response column using a mapping logic (Yes = 1, No = 0) to convert response status into a numeric target format for classification and churn modeling.

Claim_to_Income_Ratio: Calculated as Total Claim Amount / Income to measure financial stress and claim burden relative to a policyholder's income level.

Policy_Age_Ratio: Calculated as Months Since Last Claim / Customer Lifetime Value to capture historical claim recency relative to overall customer value.

Handling Missing Values & Outliers: Checked data types and standardized distributions to ensure reliable modeling results.

2. Core Research Questions AddressedCustomer Segmentation: Segmented policyholders to identify high-risk versus stable customer clusters for targeted retention.  
Churn Prediction: Assessed factors contributing to customer churn, focusing on early-tenure policyholders and high monthly premiums.  CLV Drivers: Analyzed primary features (such as Monthly Premium Auto and Total Claim Amount) impacting Customer Lifetime Value.  

3. Design & Communication ChoicesHonest Visualizations: Built clean, uncluttered charts using matplotlib and seaborn with explicit labels, units ($), and removed chart-junk to make insights consumable for non-technical stakeholders.

Font Compatibility Fallback: Configured standard system font families (sans-serif) to ensure cross-platform compatibility without missing font warnings.
