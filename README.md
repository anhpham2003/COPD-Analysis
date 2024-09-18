# **COPD Analysis**

## Introduction
   Chronic Obstructive Pulmonary Disease (COPD) is a group of diseases that 
   cause airflow blockage and respiratory problems. According to CDC, COPD 
   was the fourth leading cause of death in the United States in 2018. 
   Additionally, more than 50% of adults whose pulmonary functions decreased 
   were not aware that they were diagnosed with COPD (COPD, CDC). 
   Given its high prevalence in our population, understanding factors influencing COPD 
   progression is significant in improving community health and developing preventative measures. 
   This study aimed to analyze the relationship between forced expiratory volume in one second (FEV1) and various variables in the dataset, 
   with the ultimate goal of establishing a predictive model for patients’ FEV1 five years into the future.

   As part of a data science class project, I conducted an extensive analysis of [COPDGene study dataset](https://copdgene.org/) 
   to investigate the relationship between FEV1 at follow-up FEV1_phase2 and various demographic, clinical, and genetic factors. 
   This project aimed to identify significant predictors of FEV1 decline, 
   providing insights that cold inform clinical interventions for COPD patients.

   As for my personal goal in this project, I aim to practice and showcase my ability to build machine learning model 
   and visualize data to provide meaningful insights for real-world problem.

## Variables and Methods
   The analysis utilized a combination of approaches, incorporating inferential statistical methods, data visualization techniques, 
   regression modeling, and random forest algorithm. The dataset was divided into two subsets: dat1 for training and validation, 
   and dat2 for final prediction and analysis. Variables were investigated individually and comparatively to explore the variables' 
   relationship with FEV1.

   Some critical measures in the dataset:

*  **`FEV1`** (forced expiratory volume) - volume of air exhaled in 1 second
*  **`FCV`** (forced vital capacity) - total volume of air exhaled after a full breath
*  **`FEV1_FCV_ratio`**: ratio between FEV1 and FCV
*  **`FEV1_phase2`**: FEV1 of researched participants after 5 years

For this project, I aimed to only predict FEV1_phase2 values. All other missing values are ignored.

# Model Development
Using the overall findings, I developed a random forest model for predicting FEV1 after five years, 
which is heavily influenced by variables such as initial FEV1 measure, forced vital capacity (FVC), 
ratio between FEV1 and FVC and other variables. The random forest model yieled a MSE of 0.00022, 
indicating that on average, the squared difference between the actual and predicted FEV1 values is 0.00022 liters.
This suggests that the model's predictions are close to the true values, effectively capturing the underlying relationships 
between the predictor variables and FEV1 outcomes.

## Findings
### Smoking Status and Lung Function
Patients who never smoked exhibited the best lung function, as evidenced by higher FEV1 values, 
while former smokers displayed the worst lung function among all groups. The study revealed a 
signigicant different in FEV1 between former and current smokers. This can be explained by the 
cumulative damage former smokers experienced over years of smoking compared to patients who are 
currently smoking, as well as other factors such as age and other underlying environmental factors.

### Duration of Smoking
I found a moderately negative correlation between the duration of smoking and patients' FEV1 after five years, 
suggesting that prolonged smoking aggrevates lung function. This emphasizes the importance of early smoking 
cesstion intervations in preventing COPD progression.

### Gender Differences
Female patients exhibited significantly lower FEV1 values after five years compared to their counterparts. 
This difference underscores the need for gender-specific approaches in COPD treatment and preventative care.

### Baseline FEV1 (Initial FEV1)
A positive correlation exists between baseline FEV1 and FEV1 after years, with most female patients clustered 
at the lower end of this correlation. This finding indicates that patients with higher initial lung function are likely to maintain 
higher lung function over time, further highlighting the importance of a gender-focused approach in studying COPD progression.

### Ethnic Disparities
White patients demonstrated markedly higher FEV1 after five years compared to African American patients. The significant differences 
between these two ethnic groups suggest possible socioeconomic risks affecting the health of minority ethnic groups, emphasizing 
the African American community in this study.

### Emphysema and Lung Function
A strong negative correlation was found between the percentage of emphysema and FEV1 after five years, suggesting that increasing 
emphysema is associated with a significant deadline in lung function. Addressing underlying diseases such as emphysema is crucial in 
developing effective preventative and treatment strategies for COPD patients.

## Conclusion
The study emphasizes the multifactorial nature of COPD progression and underscores the importance of group-focused, multidisciplinary 
approaches in COPD treatment and prevention. Targeted interventions, including smoking cessation, addressing gender-specific disparities,
recognizing ethnic variations, and managing coexisting diseases such as emphysema, are significant for optimizing clinical outcomes, 
improving the quality of life for COPD patients, and ultimately establishing better preventative measures for COPD.

