# DSA 210 Project 2026

## Project Title
Identifying the Key Factors That Maximize Fitness Performance Using Lifestyle and Workout Data

## Project Description
This project examines how workout-related, lifestyle, and health-related variables influence fitness performance and fitness status. The main goal is to identify which factors are associated with better physical performance and overall fitness using a data-driven approach.

## Datasets
This project uses two publicly available Kaggle datasets.

### 1. Gym Members Exercise Tracking Dataset
This dataset contains 1800 observations and focuses on workout-related variables such as:
- Session duration
- Calories burned
- Workout type
- Fat percentage
- Water intake
- Workout frequency
- Experience level
- BMI

### 2. Real-World Style Fitness Classification Dataset (Synthetic)
This dataset contains 2000 observations and includes lifestyle and health-related variables such as:
- Age
- Gender
- Height
- Weight
- Sleep hours
- Nutrition quality
- Activity index
- Heart rate
- Blood pressure
- Smoking status
- Fitness status

## Enrichment
The second dataset is used to enrich the project by adding sleep, nutrition, health, and demographic variables that are not available in the primary workout dataset.

## Current Progress
The following steps have been completed:
- Data collection
- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Hypothesis testing
- Machine learning model implementation

## Variables Used

### Fitness Dataset
- Session_Duration (hours)
- Calories_Burned
- Workout_Type
- Fat_Percentage
- Water_Intake (liters)
- Workout_Frequency (days/week)
- Experience_Level
- BMI

### Lifestyle Dataset
- age
- gender
- height_cm
- weight_kg
- sleep_hours
- nutrition_quality
- activity_index
- heart_rate
- blood_pressure
- smokes
- is_fit

## Hypothesis Test Results

### 1. Workout Frequency vs Calories Burned
- Test: Independent samples t-test
- p-value = 0.4181
- Result: Not statistically significant

### 2. Fitness Status vs Sleep Hours
- Test: Independent samples t-test
- p-value = 2.78e-06
- Result: Statistically significant

### 3. Smoking Status vs Heart Rate
- Test: Independent samples t-test
- p-value = 0.6620
- Result: Not statistically significant

### 4. Workout Type vs Calories Burned
- Test: One-way ANOVA
- p-value = 0.0546
- Result: Not statistically significant at the 0.05 level

### 5. Fitness Status vs Age
- Test: Independent samples t-test
- p-value = 3.78e-22
- Result: Statistically significant

### 6. Fitness Status vs Weight
- Test: Independent samples t-test
- p-value = 8.08e-05
- Result: Statistically significant

## Preliminary Findings
The preliminary analysis suggests that sleep duration, age, and weight are significantly associated with fitness status. In contrast, workout frequency does not show a significant relationship with calories burned, and smoking status does not show a significant relationship with heart rate. Workout type appears to have a borderline relationship with calories burned, but it is not statistically significant at the 5% level.

## Machine Learning Results

### Classification Models
Three classification models were applied to predict fitness status:
- Logistic Regression
- Random Forest Classifier
- K-Nearest Neighbors (KNN)

#### Logistic Regression
- Accuracy: 0.7725
- ROC AUC: 0.8459
- Cross-Validation Accuracy: 0.788

#### Random Forest Classifier
- Accuracy: 0.7600
- ROC AUC: 0.8119
- Cross-Validation Accuracy: 0.7775

#### KNN Classifier
- Best k: 18
- Accuracy: 0.7500
- ROC AUC: 0.8059

### Classification Conclusion
Logistic Regression achieved the best classification performance among the tested models, with the highest accuracy, ROC AUC, and cross-validation accuracy.

### Regression Models
Two regression models were applied to predict calories burned:
- Linear Regression
- Random Forest Regressor

#### Linear Regression
- R²: 0.0047
- RMSE: 316.79
- Cross-Validation R²: -0.0055

#### Random Forest Regressor
- R²: -0.0269
- RMSE: 321.79
- Cross-Validation R²: -0.0348

### Regression Conclusion
The regression models did not perform well in predicting calories burned. The very low and negative R² values suggest that the selected variables were not sufficient to explain calorie expenditure accurately.

## Feature Importance

### Lifestyle Classification
The most important variables for predicting fitness status were:
- activity_index
- nutrition_quality
- age
- smokes
- sleep_hours

### Fitness Regression
The most important variables for predicting calories burned were:
- BMI
- Fat_Percentage
- Session_Duration (hours)
- Water_Intake (liters)

## Repository Contents
- `dsa210_project.ipynb` — main project notebook
- `gym_members_exercise_tracking_synthetic_data.csv` — workout dataset
- `fitness_dataset.csv` — lifestyle dataset
- `README.md` — project overview and progress summary

## How to Run
1. Open the notebook in Jupyter Notebook or Google Colab.
2. Make sure both CSV files are in the same directory as the notebook.
3. Run all cells in order.
