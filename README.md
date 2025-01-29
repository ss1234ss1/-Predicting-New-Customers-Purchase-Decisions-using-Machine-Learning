
# **Energy Sector Purchase Prediction**
**BA305 Team 5 Project**

## **Overview**
This project focuses on **predicting new customers' purchase decisions** in the energy sector using **machine learning models**. The goal is to **optimize marketing campaigns** by identifying key factors that influence purchase behavior, ultimately increasing revenue.

We utilized various **classification models**, including:
- **Random Forest**
- **Logistic Regression**
- **K-Nearest Neighbors (KNN)**
- **Neural Networks**

The dataset includes **31,480 customers** with demographic, financial, and marketing campaign-related features.

## **Dataset**
The dataset was obtained from **Kaggle** and includes **20 features** such as:
- **Demographic Information**: Age, Education, Job, Marital Status
- **Financial Data**: Account Balance, Credit History
- **Marketing Campaign Data**: Contact Type, Duration of Call, Last Campaign Result

A key challenge was handling **imbalanced data**, as only **11.75% of customers made a purchase**.

## **Data Processing**
### **1. Data Cleaning**
- Renamed target variable **"target" → "purchase"**
- Dropped unnecessary features (**daySinceLastCampaign, lastCampaignResult**)
- Filled missing values
- One-hot encoded categorical variables

### **2. Exploratory Data Analysis (EDA)**
- **Identified important features**:
  - Longer call durations increased purchase likelihood.
  - Higher account balance correlated with higher purchase probability.
- **Balanced dataset** using **Random Over Sampling**.

### **3. Feature Selection**
- **Decision Tree Classifier** identified the most significant factors:
  - **Duration of Call**
  - **Day of Contact**
  - **Account Balance**
  - **Age**
  - **Contact Type (Unknown)**

## **Modeling**
### **1. Random Forest (Best Model)**
- Achieved **96.63% accuracy**.
- Identified **533 false positives**, requiring further fine-tuning.

### **2. Logistic Regression**
- Accuracy: **89.92%**
- Highlighted key influencing factors:
  - **Call duration** had the most significant impact.
  - **Unknown contact type negatively affected purchase rates**.

### **3. K-Nearest Neighbors (KNN)**
- Accuracy: **88.49%**
- Performed well but was **less effective at predicting purchases**.

### **4. Neural Networks**
- Accuracy: **89.72%**
- Captured complex relationships but required **more data for better generalization**.

## **Results & Recommendations**
1. **Marketing Strategies for Higher Conversion**:
   - **Prioritize customers with a history of long call durations**.
   - **Target older, more educated, and financially stable customers**.
   - **Optimize campaign timing (e.g., end-of-month contact was more effective)**.

2. **Future Improvements**:
   - **Improve data collection** (focus on customer interactions, not just demographics).
   - **Perform power analysis** to determine sample size requirements.
   - **Explore alternative balancing techniques** for improved performance.

## **Project Files**
| File | Description |
|------|------------|
| `BA305_T5_Presentation.pdf` | Final project presentation slides |
| `BA305_T5_Project_Report.pdf` | Detailed project report |
| `BA305_Group_Project_Final.ipynb` | Jupyter Notebook with data preprocessing and modeling |
| `train.csv` | Training dataset |
| `test.csv` | Testing dataset |


## **Acknowledgments**
Special thanks to **Dr. Maryam Khanian** for providing the dataset and insights into the **energy sector telemarketing campaign**.
