# DailyBikeCountPrediction
Machine learning model to predict daily bike rental counts based on weather conditions and time features built as a part of INFO BHARAT INTERNS program.

 📌 Overview

This project predicts daily bike rental counts using environmental and temporal factors.
It applies multiple regression models, compares their performance, and uses Gradient Boosting Regressor as the final choice after hyperparameter tuning.

📂 Dataset

Source: <a href="https://www.kaggle.com/datasets/lakshmi25npathi/bike-sharing-dataset">Bike Sharing Dataset</a>

File Used: day.csv

Target Variable: cnt – total bike rentals per day

🔍 Project Workflow
1️⃣ Data Preprocessing

Dropped columns that don’t influence prediction.

Created daycount as a sequential feature.

Handled missing values and converted data types.

2️⃣ Exploratory Data Analysis (EDA)

Checked distribution for skewness & outliers.

Plotted relationships of temp, hum, windspeed with cnt.

Created correlation heatmap for feature relationships.

3️⃣ Feature Scaling

Used StandardScaler for temp, hum, and windspeed due to different ranges.

4️⃣ Model Building & Evaluation

Models tested:

Linear Regression → RMSE ≈ 912.90

Decision Tree Regressor → RMSE ≈ 1052.32

Random Forest Regressor → RMSE ≈ 859.72

Gradient Boosting Regressor → RMSE ≈ 810.98 ✅ (Best)

Used cross-validation for fair comparison.

5️⃣ Hyperparameter Tuning

Performed GridSearchCV to find best parameters for Gradient Boosting Regressor.

6️⃣ Final Prediction & Visualization

Final RMSE on test set: 801.87

Plotted:

Scatter plot: Actual vs Predicted counts

Feature importance chart

Actual vs Predicted over time

📊 Technologies Used

Python

Pandas, NumPy – Data handling

Matplotlib, Seaborn – Visualization

Scikit-learn – Machine Learning

🚀 Usage
# Clone the repository
git clone https://github.com/username/BikeRentalPredictiveModel.git

# Install dependencies
pip install -r requirements.txt

# Run the model
python model.py

📈 Results Summary
Model	RMSE	Notes
Linear Regression	912.90	Simple baseline
Decision Tree Regressor	1052.32	Overfitted
Random Forest Regressor	859.72	Good performance
Gradient Boosting	810.98	Best model

Final Test RMSE: 801.87

👤 Author

Smriti Pandey
📌 Developed during internship at Info Bharat Interns
