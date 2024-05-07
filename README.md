# Horse-Health-Prediction
[PROJECT LINK](https://www.kaggle.com/competitions/playground-series-s3e22/data?select=train.csv).
 BRIEF OVERVIEW-  While reading about this dataset, I found that it is synthetic (created by using algorithms and simulations based on generative artificial intelligence technologies) which explains certain inconsistencies.
The Predict Health Outcomes of Horses project is dedicated to a multi-class classification challenge. The target variable is the horse's outcome, which can fall into different classes.

Dataset Features

Here's a brief overview of the features in the dataset:

surgery: Nominal variable ('yes' or 'no') indicating whether surgery was performed.

age: Nominal variable ('adult' or 'young') representing the age of the horse.

hospital_number: Numeric variable indicating how many times a horse has gone to the hospital.

rectal_temp: Ratio data representing the horse's rectal temperature.

pulse: Ratio data indicating the horse's pulse rate.

respiratory_rate: Ratio data showing the horse's respiratory rate.

temp_of_extremitiess: Nominal data indicating the temperature of extremities.

peripheral_pulse: Nominal data indicating peripheral pulse conditions.

mucous_membrane: Ordinal data representing the condition of mucous membranes.

capillary_refill_time: Ordinal data indicating capillary refill time.

pain: Nominal data indicating the horse's pain level.

peristalsis: Ordinal data indicating the activity in the horse's gut.

abdominal_distention: Ordinal data indicating abdominal distention.

nasogastric_tube: Ordinal data representing nasogastric tube condition.

nasogastric_reflux: Ordinal data indicating nasogastric reflux.

nasogastric_reflux_ph: Ratio data representing nasogastric reflux pH.

rectal_exam_feces: Ordinal data representing rectal examination findings related to feces.

abdomen: Ordinal data representing the condition of the abdomen.

packed_cell_volume: Ratio data representing packed cell volume in the blood.

total_protein: Ratio data representing total protein levels in the blood.

abdomo_appearance: Nominal data representing abdominal appearance.

abdomo_protein: Ratio data indicating abdominal protein levels.

surgical_lesion: Nominal data indicating whether a surgical lesion is present.

lesion_1, lesion_2, lesion_3: Ratio data related to lesions (some of which may be dropped).

cp_data: Nominal data indicating the presence of central nervous system disorders.

outcome: Target variable representing the horse's health outcome( L, E, D).

>DATA DESCRIPTION
- Have both train and test set, total of 29/28 columns and 1235/824 entries.
- Data is 59% categorical cols
- All missing values came from the categorical columns .The categorical columns with missing values: ['temp_of_extremities', 'peripheral_pulse', 'mucous_membrane', 'capillary_refill_time', 'pain', 'peristalsis', 'abdominal_distention', 'nasogastric_tube', 'nasogastric_reflux', 'rectal_exam_feces', 'abdomen', 'abdomo_appearance']
- No significant class imbalance (>20%)

*DATA VISUALIZATION* (Both for the categorical and numerical values)
![image](https://github.com/fs239188/Horse-Health-Prediction/assets/143844308/1e370f1b-bb57-4689-bcff-07607db4db49)
![image](https://github.com/fs239188/Horse-Health-Prediction/assets/143844308/affcd6a6-738b-4d69-8fdc-96282d3baac9)
![image](https://github.com/fs239188/Horse-Health-Prediction/assets/143844308/18cc0dd8-ff7d-49ae-bb97-d49f14cddbc3)

![image](https://github.com/fs239188/Horse-Health-Prediction/assets/143844308/45db8006-d310-4707-8f7e-e09556fca996)

*FEATURE ENGINEERING*
- One-Hot Encoding: I applied one-hot encoding to categorical variables to convert them into a format suitable for the machine learning algorithms.
- Normalized numerical features to bring them to the same scale using MinMaxScaler.
- Dealt with outliers using z score method.
- Dropped ID and Hospital number (not useful with the model), Lesion_1, Lesion_2, Lesion_3(90% null values) and cp_data(non relevant).

*MACHINE LEARNING*
- Split using standard 80-20
- I used both Random Forest(An ensemble learning method that constructs multiple decision trees during training and outputs the mode of the classes for classification tasks. Random forest was selected for its ability to handle non-linear relationships, handle categorical variables, and reduce overfittin and XGBoost(computationally effective and can quickly train models on large datasets) 69% and 66% accuracy respectively.

<The RF feature importance establishes my prior predictions as to which columns contribute the most to the horse outcomes>
 
![image](https://github.com/fs239188/Horse-Health-Prediction/assets/143844308/1ff245c8-cb2a-4b71-bb6a-8152f2fd4036)

- *Future Work*
Model Selection: Experiment with more advanced machine learning algorithms to improve predictive performance.
Feautres: Do more than just dropping certain columns.

#*Overview of files in repository*
FinalPYthon2.ipynb: This notebook contains code for evaluating the performance of the trained models. It includes functions for data cleaning, preprocessing, model training, evaluation, and visualization.
