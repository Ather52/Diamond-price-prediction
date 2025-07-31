# Diamond Price Prediction

## 📌 Project Overview
This project aims to predict diamond prices using various regression-based machine learning models. Based on key physical and quality attributes like *carat*, *cut*, *color*, *clarity*, and dimensions, it builds and evaluates multiple models, selecting the one with the highest cross-validated R² score for final prediction.

## 📂 Dataset Information
The dataset includes key features that influence diamond pricing:
- **carat** – weight of the diamond  
- **cut** – quality of the cut (e.g., Ideal, Premium, Good, Fair)  
- **color** – color grade (from D to J, with D being best)  
- **clarity** – clarity grade (e.g., SI1, VS1, IF)  
- **depth** – total depth percentage  
- **table** – width of the top of the diamond relative to its widest point  
- **x (renamed as length_mm)** – length in mm  
- **y (renamed as width_mm)** – width in mm  
- **z (renamed as depth_mm)** – depth in mm  
- **price** – target variable in USD  

The data is cleaned and refined by handling outliers and encoding categorical values.

## 🔄 Data Preprocessing
- Renamed dimension columns for clarity: `x → length_mm`, `y → width_mm`, `z → depth_mm`
- Removed outliers in width, depth, and proportions
- Encoded categorical variables using LabelEncoder
- Normalized features using RobustScaler

## 📊 Exploratory Data Analysis (EDA)
- Plotted distributions of all variables
- Identified *carat* as the strongest predictor of price
- Used correlation heatmaps and pairplots to understand interdependencies

## 🏗 Model Training & Evaluation
Evaluated four regression models using 5-fold cross-validation:
- Linear Regression  
- Random Forest Regressor  
- XGBoost Regressor  
- MLP Regressor (Neural Network)  

**Performance Metrics Used:**
- **R² Score**  
- **Mean Squared Error (MSE)**  
- **Mean Absolute Error (MAE)**  

The model with the highest average R² score during cross-validation was selected and tested.

## 🎯 Results
The best-performing model showed strong predictive capability on the test set:

- **R² Score:** 0.9612  
- **Mean Absolute Error (MAE):** 0.1043  
- **Mean Squared Error (MSE):** 0.0281  

These results demonstrate that the model captures complex relationships in the data and can accurately predict diamond prices, making it practical for real-world pricing tools or recommendation systems.

## ⚙️ How to Set Up and Run the Project
To run this project locally:

```bash
### ⿡ Clone the Repository
git clone https://github.com/ather52/Diamond-Price-Prediction.git
cd Diamond-Price-Prediction

### ⿢ Install Dependencies
pip install -r requirements.txt

### ⿣ Run the Jupyter Notebook
jupyter notebook

### 📦 Dependencies
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost

### 📢 Contributions Welcome!
Feel free to fork, enhance, or raise issues.

👤 Author: Muhammad Ather  
📧 Contact: athertahir52@gmail.com
```

