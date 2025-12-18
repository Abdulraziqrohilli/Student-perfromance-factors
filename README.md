# Student Performance Factors Analysis

## Project Overview

This project provides a comprehensive **Exploratory Data Analysis (EDA)** of a dataset on student performance factors. The goal is to analyze various factors affecting students' exam scores and to visualize key relationships using Python and interactive plotting libraries like **Plotly**.

The dataset includes features related to study habits, parental involvement, resources access, extracurricular activities, and more.

---

## Dataset Information

- **Number of Rows:** 6607  
- **Number of Columns:** 20  

### Column Details

**Numerical Columns (7):**  
`Hours_Studied, Attendance, Sleep_Hours, Previous_Scores, Tutoring_Sessions, Physical_Activity, Exam_Score`  

**Categorical Columns (13):**  
`Parental_Involvement, Access_to_Resources, Extracurricular_Activities, Motivation_Level, Internet_Access, Family_Income, Teacher_Quality, School_Type, Peer_Influence, Learning_Disabilities, Parental_Education_Level, Distance_from_Home, Gender`

**Example Data:**

| Hours_Studied | Attendance | Parental_Involvement | Access_to_Resources | Extracurricular_Activities | Sleep_Hours | Previous_Scores | Motivation_Level | Internet_Access | Tutoring_Sessions | Family_Income | Teacher_Quality | School_Type | Peer_Influence | Physical_Activity | Learning_Disabilities | Parental_Education_Level | Distance_from_Home | Gender | Exam_Score |
|---------------|------------|--------------------|-------------------|----------------------------|------------|----------------|-----------------|----------------|-----------------|---------------|----------------|------------|----------------|-----------------|---------------------|-------------------------|------------------|--------|------------|
| 23            | 84         | Low                | High              | No                         | 7          | 73             | Low             | Yes            | 0               | Low           | Medium         | Public     | Positive       | 3               | No                  | High School             | Near             | Male   | 67         |

---

## Libraries Used

- `pandas`, `numpy` – Data manipulation  
- `matplotlib`, `seaborn`, `missingno` – Basic visualization & missing data analysis  
- `plotly.express`, `plotly.graph_objects` – Interactive visualizations  
- `warnings` – To ignore unnecessary warnings  

---

## Exploratory Data Analysis (EDA)

### 1. Missing Values Analysis

- Columns with missing values:  
  - `Parental_Education_Level`: 1.36% missing  
  - `Teacher_Quality`: 1.18% missing  
  - `Distance_from_Home`: 1.01% missing  

**Imputation strategy:**  
- Teacher_Quality → `"Medium"`  
- Parental_Education_Level → `"High School"`  
- Distance_from_Home → `"Near"`  

After imputation, **no missing values remain**.

---

### 2. Numerical Features Distribution

- Visualized with **interactive line and scatter plots**  
- Key features: `Hours_Studied`, `Attendance`, `Sleep_Hours`, `Previous_Scores`, `Tutoring_Sessions`, `Physical_Activity`, `Exam_Score`

---

### 3. Categorical Features Distribution

- Features like `Parental_Involvement`, `Motivation_Level`, `Internet_Access`, `School_Type`, etc.  
- Displayed in **interactive bar plots**  

---

### 4. Relationships Between Features

#### Attendance vs Exam Score
- Students with higher attendance generally perform better.
- Performance difference between lowest and highest attendance groups: **6.2 points**  

#### Parental Involvement & Access to Resources
- Box plots show **higher exam scores** for students with more parental involvement and better resources.

#### Tutoring Sessions vs Family Income
- 3D scatter plot highlights impact of tutoring sessions and family income on exam scores.

#### Motivation Level & Peer Influence
- Treemap and cross-tab analysis show distribution of exam scores based on **motivation** and **peer influence**.
- High motivation + positive peer influence → higher scores.

#### Parental Education & Learning Disabilities
- Box and violin plots reveal exam score trends by parental education and disability status.

#### School Type & Teacher Quality
- Students in schools with higher teacher quality tend to perform better.

#### Physical Activity & Sleep Hours
- Scatter matrices and correlation analysis show minor relationships with exam scores.
- Correlation coefficients:
  - Physical Activity vs Exam Score: `r = 0.03`  
  - Sleep Hours vs Exam Score: `r = -0.02`

---

## Future Improvements

- Convert models or analyses into `.keras` format for ML modeling  
- Apply **data augmentation** for better predictive modeling  
- Integrate **transfer learning models**  
- Include **confidence scores** for predictions  
- Deploy visualizations and predictive models on **cloud platforms**

---
