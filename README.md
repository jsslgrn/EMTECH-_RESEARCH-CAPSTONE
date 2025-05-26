# EMTECH-_RESEARCH-CAPSTONE
A Capstone Project about Lifestyle and Learning – Predicting Student Performance dataset


This project explores how students’ lifestyle habits—such as sleep, screen time, diet, and study hours—affect their academic performance. Using a simulated dataset of 1,000 student records, we apply data analysis and machine learning techniques to identify behavior patterns, group students based on similarities, and predict their final exam scores.

**PROJECT GOALS**

- Understand relationships between lifestyle behaviors and exam scores

- Group students with similar habits using clustering

- Build regression models to predict final exam performance

- Optionally, classify students into performance levels (Low, Average, High)

- Generate insights to inform academic improvement strategies


Dataset:
Name: student_habits_performance.csv

Source: Kaggle

Size: 1,000 records

**KEY FEAUTRES:**

- Lifestyle metrics (e.g., study_hours_per_day, sleep_hours, screen time, health indicators)

- Final exam score (target for regression)

- Derived features (e.g., total_screen_time, health_score, engagement_score)

**METHODS AND WORKFLOW**

1. **Data Preprocessing**
Handled missing values and encoded categorical variables

Scaled numerical features using StandardScaler

Engineered new features such as health_score and engagement_score


2. **Exploratory Data Analysis (EDA)**
   
Plotted histograms, boxplots, and scatterplots to explore distributions and relationships

Computed correlation heatmaps to identify key influencing factors

3. **Clustering**
   
Applied K-Means clustering (with scaled lifestyle features only)

Determined optimal K using Elbow Method and Silhouette Scores

Identified 3 meaningful clusters and profiled each group


4. **Regression Models**
   
To predict the final exam score:

Model	MAE (CV)	RMSE (CV)	R² (CV)
Linear Regression	4.28	5.39	0.90
Decision Tree Regressor	6.68	8.57	0.74
Random Forest Regressor	4.69	5.90	0.88
Linear Regression performed the best overall with the highest R² and lowest error.


5.**Classification Models (Optional)**

Converted exam scores into 3 performance levels:

Low (bottom 33%)

Average (middle 34%)

High (top 33%)

Model	Accuracy (CV)	F1 Score (CV)
Logistic Regression	0.79	0.78
Decision Tree	0.72	0.70
Random Forest	0.84	0.82
**Random Forest Classifier gave the best classification results.**


**Insights and Interpretations**


**A. Top Features Affecting Performance**

Across all models, the most impactful features were:

study_hours_per_day

health_score

total_screen_time

engagement_score

attendance_percentage

- Students who studied more, maintained good health, and limited screen time consistently performed better.

**B. Cluster Profiling**

- Cluster 0: Low engagement and poor health; lowest exam scores

- Cluster 1: Balanced lifestyle; average performance

- Cluster 2: High effort and strong wellness; highest scores Trends showed that high screen time correlated with lower scores, while more sleep and studying led to better outcomes.

**C. Model Performance**

- Linear Regression (regression) and Random Forest Classifier (classification) performed best.

Tree-based models had higher accuracy but lower interpretability compared to linear models.

**D. Real-World Implications**

- Students are advised to focus on consistent study habits, reduce screen time, and prioritize health and wellness. Surprisingly, health_score was nearly as predictive as study time, emphasizing the importance of a balanced lifestyle.



**Repository Contents**


- **CapstoneProject.ipynb** – Complete Jupyter Notebook with code, outputs, and interpretations

- **student_habits_performance.csv**– Dataset

- **README.md** – Project summary

- **Visuals/**– Folder containing all saved plots
