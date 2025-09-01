# 🚢 Titanic Survival Prediction  

![Titanic](https://upload.wikimedia.org/wikipedia/commons/f/fd/RMS_Titanic_3.jpg)

---

## 📌 Project Overview  
This project is all about predicting **who survived the Titanic disaster** using the **famous Titanic dataset**.  
We applied different **Machine Learning models** (Decision Tree, Logistic Regression, KNN) and compared their performance.  

The project focuses on:  
- Data Cleaning (handling missing values, datatypes, categorical encoding)  
- Model Training & Evaluation  
- Hyperparameter Tuning with Grid Search  
- Visualizations (Confusion Matrix, Feature Importance)  

---

## 🛠️ Tools & Libraries Used  
- **Numpy** → Numerical calculations  
- **Pandas** → Data handling and cleaning  
- **Matplotlib & Seaborn** → Data visualization  
- **Scikit-Learn (sklearn)** → Machine Learning models & evaluation  

---

## 📂 Dataset  
- Titanic dataset (`train.csv` & `test.csv`) is already included in this repository.  
- Both files were combined into a single dataframe for consistent cleaning and preprocessing.  

---

## 🧹 Data Preprocessing Steps  
✔️ Combined `train` and `test` into one dataframe  
✔️ Filled missing values (e.g., Age, Embarked, Fare)  
✔️ Dropped unnecessary columns (like Ticket & Cabin)  
✔️ Changed datatypes where required  
✔️ Converted categorical features (e.g., Sex, Embarked) into numerical using **mapping**  

---

## 🤖 Models Applied  

### 1️⃣ Decision Tree Classifier  
- Accuracy: **0.72**  
- Confusion Matrix: ✅ (image attached)  
- Feature Importance shows **Sex** is the most influential feature.
- <img width="649" height="547" alt="22-1" src="https://github.com/user-attachments/assets/56e61087-ddf4-4948-80bd-05c23de5a8d0" />


### 2️⃣ Logistic Regression  
- Accuracy: **0.80** 🎯  
- Confusion Matrix: ✅ (image attached)
- <img width="649" height="547" alt="22-2" src="https://github.com/user-attachments/assets/2ee45848-90ca-471a-a8bd-d72d13385996" />
 

### 3️⃣ K-Nearest Neighbors (KNN)  
- Accuracy: **0.71**  
- Confusion Matrix: ✅ (image attached)
- <img width="649" height="547" alt="22-3" src="https://github.com/user-attachments/assets/3742d34a-58ad-42bc-9174-9aadb309da83" />


---

## 🔍 Hyperparameter Tuning  

### 🟢 Grid Search on Decision Tree  

param_grid = {
    'criterion': ['gini', 'entropy'], 
    'splitter': ['best', 'random'],
    'max_depth': [4, 8, 10, 13],
    'max_features': ['sqrt', 'log2', None],
    'min_samples_leaf': [6, 10],
}
- est score: 0.78

- Limited depth gave better generalization.

- Confusion Matrix: ✅ (image attached)
- <img width="649" height="547" alt="22-4" src="https://github.com/user-attachments/assets/a6877493-2396-49ee-9eef-8208a1ba11b6" />


### 🟢 Grid Search on Logistic Regression

- Best score: 0.77

- Confusion Matrix: ✅ (image attached)🟢 Grid Search on Logistic Regression

- Best score: 0.77

- Confusion Matrix: ✅ (image attached)
- <img width="649" height="547" alt="22-5" src="https://github.com/user-attachments/assets/e7f7832b-5af3-4b90-aee6-024b2b1675ac" />


  ### 📊 Results Summary
Model	Accuracy
Decision Tree	0.72
Logistic Regression	0.80 ✅
KNN	0.71
GridSearch (Decision Tree)	0.78
GridSearch (Logistic Regression)	0.77
<img width="649" height="547" alt="22-6" src="https://github.com/user-attachments/assets/321ba3d0-18fb-4c6e-8c68-10d707a784ee" />

👉 Logistic Regression performed the best with 80% accuracy.


### 🌐 Deployment Note

In another project, we also applied Bagging (Ensemble Method) on selected 5 features and achieved 83% accuracy 🎉.
That model has been deployed on Streamlit:

🔗 Live Demo on Streamlit

### 📷 Visuals

Confusion Matrix images are attached in the repository.

Feature importance chart (Decision Tree) is also included.
