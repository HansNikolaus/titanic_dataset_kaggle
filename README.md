# Titanic Survival Prediction 🌊🚢

Machine learning from disaster! This repository showcases my efforts in solving the popular [Kaggle Titanic Dataset Challenge](https://www.kaggle.com/c/titanic). This is a classic introductory task for data science and machine learning enthusiasts.

## 📖 Overview

The Titanic dataset challenge involves analyzing data from the tragic Titanic shipwreck to predict the survival status of passengers. By leveraging machine learning techniques, the goal is to build a predictive model for passenger survival based on variables like age, gender, ticket class, and more.

## 🚀 Project Goals

- Perform **exploratory data analysis (EDA)** to uncover insights.
- Clean and preprocess the dataset to handle missing or inconsistent values.
- Build and evaluate machine learning models to predict survival.
- Share key findings and insights for better decision-making.

## ⚙️ Key Steps in the Project

1. **Exploratory Data Analysis (EDA):**
   - Visualize survival rates across various features (e.g., age, class, and gender).
   - Identify relationships and outliers.

2. **Data Preprocessing:**
   - Handle missing values in features like `Age` and `Cabin`.
   - Encode categorical variables (e.g., gender and embarkation port).

3. **Feature Engineering:**
   - Derive additional features, such as family size or title from passenger names.
   - Normalize and scale numerical variables.

4. **Modeling:**
   - Train machine learning models, such as logistic regression, decision trees, random forests, gradient boosting, and Support Vector Machine.
   - Evaluate models using accuracy, precision, recall, and ROC-AUC.

## 📊 Results

**Overall best-performing model? Standard Logistic Regression**
- Overall Accuracy Score of 84.4%
- Its Precision, Recall and F1 Scores for Non-Survivors and Survivors were consistently 87% and 81%.
  
**Best model for identifying Survivors? Class-Weighted Logistic Regression**
- Overall Accuracy Score of 83.8%
- Prescision scores were 89% for Non-Survivors and 78% for Survivors.
- Recall scores were 83% for Non-Survivors and 85% for Survivors.

**Comparison**
- While the Precision Score drops from 81% to 78%, the Recall Score rises from 81% to 85%. Meaning that while there is an increase of false positives, there is also an increase of true positives. Essentially there is a trade off and it depends what we wnt our model to be better at. When it comes to identifying Survivors, the Standard Logistic Regression model has less false positives, those that were wrongly assumed to be survivors, and the Class-Weighted model has a higher percentage chance of identifying True Positives, those that actually survived.

**Why was the Class-Weighted model slightly more effective in identifying Survivors?**
- It helped to address class imbalance in the dataset. Class imbalance occurs when one class is significantly underrepresented compared to the others, which can lead to biased predictions favoring the majority class. In the case of the Titanic dataset, the number of Non-Survivors is significantly more than the number Survivors making it the majority class. While the Standard Logistic Regression model did work well overall, all instances (passengers) contributed equally to the loss function. However, in the Class-Weighted model, "weights" are applied to the loss function based on the class. The weight for each class is typically inversely proportional to its frequency in the training set.

**What is a Loss Function?**
- Its a mathematical formula that measures how well or poorly a model's predictions align with the actual outcomes, quantifying the error between the predicted values, and the actual true values. For the Titanic dataset, you are trying to predict whether a passenger is a Survivor or Non-Survivor which is considered to be a binary classification task. One of the most common loss functions for such a task is called Logarithmic Loss. It is used to measure the probability of each True Label within the dataset, or in our case each instance of a passenger correctly being identified as a Survivor or Non-Survivor. Essentially it penalizes the model for having false negatives and false positives, the more there are the lower the score.

## 🛠️ Tools and Technologies

- **Languages**: Python 🐍
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Imblearn
- **Environment**: Jupyter Notebook
