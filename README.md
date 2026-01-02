# # Job Cost & Completion Time Prediction
Predicting job cost and completion time using Python scikit- learn,  Random forest, XGBoost

## Overview
This project predicts the **cost** and **completion time** of bespoke woodworking jobs using machine learning. 
The goal is to improve quoting accuracy, project planning, and delivery scheduling for bespoke projects.

---

## Dataset
The dataset is synthetic but designed to reflect real-world woodworking jobs. Features include:

- **job_type:** Kitchen, Wardrobe, Table, Cabinetry  
- **material:** Oak, Walnut, MDF, Plywood  
- **length_mm, width_mm, height_mm:** Dimensions of the job  
- **complexity:** Scale 1–5, indicating difficulty  
- **finish_type:** Paint, Oil, Lacquer  
- **labour_hours, machine_hours:** Estimated work hours  

**Targets:**
- `job_cost` – predicted cost in GBP  
- `completion_days` – predicted project duration in days  

---

## Methods
1. **Data Generation & Cleaning** – Generated realistic project data, checked for missing values  
2. **Exploratory Data Analysis (EDA)** – Visualised relationships between features and target variables  
3. **Feature Engineering** – One-hot encoded categorical variables; used numerical features as-is  
4. **Modeling** –  
   - Random Forest Regressor  
   - XGBoost Regressor  
5. **Evaluation** –  
   - Mean Absolute Error (MAE)  
   - R² Score  
   - Cross-validation  
6. **Robustness Testing** – Tested model performance removing key features (e.g., labour_hours)  

---

## Results

| Model             | Target       | MAE         | R² Score |
|------------------|------------|------------|----------|
| Random Forest     | Job Cost    | £101.81    | 0.973    |
| XGBoost           | Job Cost    | £95–105    | ~0.975   |
| Random Forest     | Completion Days | 0.85 days | 0.94     |

**Key Insights:**
- Labour hours and material choice are the strongest predictors of cost  
- Model predicts job costs within ~£100 on average, suitable for quoting  
- Completion time predictions help optimise scheduling and delivery  

---

## Usage
1. Clone the repository:
```bash
git clone https://github.com/kingsleyanim2021-pixel/job-cost-prediction.git

