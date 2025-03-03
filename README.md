# 🦠 Malaria Prediction using Machine Learning
## 📌 Project Description
This project aims to predict malaria cases from various clinical symptoms using machine learning models. We explored several algorithms, applied class imbalance management techniques, and interpreted the results using LIME and feature importance.
## 📂 Data
The dataset contains several clinical variables such as age, fever, fatigue, diarrhea, anemia, convulsions, prostration, etc. The objective is to train a model capable of predicting the presence of malaria in a patient based on these symptoms.
## ⚙️ Machine Learning Models Used

We tested several algorithms to evaluate their performance in malaria prediction:

- 🌳 Random Forest
- 🎯 XGBoost
- 🚀 Gradient Boosting
- 🐱 CatBoost
- 🔥 AdaBoost
## 📊 Results before and after Oversampling
### 📉 Before Oversampling (Class Imbalance)
Before applying oversampling to rebalance the classes, the models’ performances were quite limited, especially due to the imbalanced class. Models such as Random Forest and CatBoost showed acceptable performances with respective accuracies around 65% and 64%, but other metrics such as the ROC AUC score (which evaluates the quality of class separation) remained low. For example, XGBoost scored 0.607 in accuracy and 0.523 in ROC AUC, indicating a limited ability to correctly predict positive cases. The AdaBoost model performed particularly poorly, with an accuracy of only 0.637 and a MCC (Matthews Correlation Coefficient) close to zero, indicating a lack of discernment between classes.
### 📈 After Oversampling (Class Rebalancing)
After oversampling, which involves rebalancing the classes by increasing the number of examples from the minority class, the models’ performance improved significantly. XGBoost showed the best improvement, with an accuracy of 0.774 and an ROC AUC score of 0.776. The CatBoost model also showed good results with an accuracy of 0.766 and an ROC AUC score of 0.853. However, AdaBoost did not show much improvement, maintaining an accuracy of 0.556 and a low MCC. Overall, oversampling had a positive impact on most models, especially XGBoost, Gradient Boost, and Random Forest, but was not as effective for AdaBoost.
### 🔍 Interpretability with LIME
To better understand the impact of different features on the model's predictions, we used LIME (Local Interpretable Model-Agnostic Explanations). This method allowed us to identify the most important features that influence the model's decisions.

Age is the most significant feature, with an importance of 0.1753, suggesting that it has a determining effect on the prediction of malaria. Other clinical symptoms such as bitter tongue (0.0667), convulsions (0.0591) and Coca-Cola urine (0.0570) also have a notable influence. These symptoms, often linked to severe forms of the disease, indicate that an effective model must take these clinical signals into account.

Other features such as prostration (0.0561) and headache (0.0397) are also important, but to a lesser extent. Other symptoms, such as anemia (0.0330), rigor (0.0328) and cold (0.0287), although they contribute to the predictions, have a relatively low importance.

LIME analysis thus provides a more detailed understanding of the impact of each feature on the model decisions, which can help to refine the feature selection and better interpret the predictions in a clinical context.
## ✨ Technologies used

- Python (Pandas, NumPy, Scikit-Learn, XGBoost, CatBoost, LightGBM, LIME)
- Jupyter Notebook for exploratory analysis
- Matplotlib & Seaborn for visualization
## 👨‍💻 Auteur

- 📌 Name : ***Ing.Oumar Moussa***
- 📌 E-mail : ***oumar.moussa@aims-cameroon.org***
- 📌 LinkedIn : ***Ing.Oumar Moussa***
