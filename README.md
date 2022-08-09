# Classification-Prediction-Capstone-Project

The term heart disease is often used interchangeably with the term cardiovascular disease. Cardiovascular disease generally refers to conditions that involve narrowed or blocked blood vessels that can lead to a heart attack, chest pain (angina) or stroke.
The most common cause of heart disease is narrowing or blockage of the coronary arteries, the blood vessels that supply blood to the heart itself. This is called coronary artery disease and happens slowly over time.


 **The dataset is from an ongoing cardiovascular study on residents of the town of Framingham,
Massachusetts. The classification goal is to predict whether the patient has a 10-year risk of
future coronary heart disease (CHD). The dataset provides the patients’ information. It includes
over 4,000 records and 15 attributes.
Variables
Each attribute is a potential risk factor. There are both demographic, behavioral, and medical risk
factors.**
# Column description:-
* **Sex**: male or female("M" or "F")
* **Age**: Age of the patient;(Continuous - Although the recorded ages have been truncated to
whole numbers, the concept of age is continuous)
Behavioral
* **is_smoking**: whether or not the patient is a current smoker ("YES" or "NO")
* **Cigs Per Day**: the number of cigarettes that the person smoked on average in one day.(can be
considered continuous as one can have any number of cigarettes, even half a cigarette.)
Medical( history)
* **BP Meds**: whether or not the patient was on blood pressure medication (Nominal)
* **Prevalent Stroke**: whether or not the patient had previously had a stroke (Nominal)
* **Prevalent Hyp**: whether or not the patient was hypertensive (Nominal)
* **Diabetes**: whether or not the patient had diabetes (Nominal)
Medical(current)
* **Tot Chol**: total cholesterol level (Continuous)
* **Sys BP**: systolic blood pressure (Continuous)
* **Dia BP**: diastolic blood pressure (Continuous)
* **BMI**: Body Mass Index (Continuous)
* **Heart Rate**: heart rate (Continuous - In medical research, variables such as heart rate though in
fact discrete, yet are considered continuous because of large number of possible values.)
* **Glucose**: glucose level (Continuous)
Predict variable (desired target)
* **10-year risk of coronary heart disease CHD** 
(binary: “1”, means “Yes”, “0” means “No”) -
DV


# **Approach**
Following steps were followed to build the model:

Dataset was cleaned off the null values.
Outliers were replaced with upper limit and lower limit values as applicable. 3. Imbalances in the classes were fixed using SMOTE.
Categorical features were encoded
Feature selection was done by inspecting correlation between features and aforementioned features were finalised.
The data was split to train and test and scaled using MinMaxScaler. 7. Following 4 models were implemented on the training set:
Logistic Regression
Random Forest Classifier
K Nearest Neighbours
Naive Bayes Classifier.

# **Result**
The task was to determine if a given patient is under the risk of CHD in the coming 10 years. To do this, following features were at our disposal: 'id','age','education','sex','cigsPerDay','BPMeds','prevalentStroke','prevalentHyp','diabe tes','totChol','sysBP','BMI','glucose'. 'is_smoking','heartRate','diaBP','TenYearCHD'. Logistic Regression, Random Forest Classifier, K Nearest Neighbours, Naive Bayes Classifier were used Of which, the Random Forest classifier yielded best results. Using Shapley analysis it was found that education, age, cigsPerDay, sysBP, and totChol were top 5 most influential factors in determination of whether the patient is facing the risk of CHD or not.
