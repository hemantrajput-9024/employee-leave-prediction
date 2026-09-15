# Employee Prediction using Machine Learning

## 📌 Project Overview

This project is a Machine Learning classification project that predicts whether an employee will **leave the company or not** based on different employee-related features.

The project follows a complete Machine Learning workflow including data loading, data preprocessing, exploratory data analysis, feature encoding, model training, prediction, and model evaluation.

## 🎯 Objective

The main objective of this project is to build a Machine Learning model that can predict employee retention using employee information such as education, age, city, payment tier, gender, and experience.

## 📊 Dataset

The dataset contains **4,653 employee records** and **9 columns**.

### Features

* `Education`
* `JoiningYear`
* `City`
* `PaymentTier`
* `Age`
* `Gender`
* `EverBenched`
* `ExperienceInCurrentDomain`
* `LeaveOrNot`

### Target Variable

`LeaveOrNot`

* `0` → Employee stays
* `1` → Employee leaves

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

* Dataset loading using KaggleHub
* Data exploration and analysis
* Checking dataset information
* Missing value analysis
* Exploratory Data Analysis (EDA)
* Categorical feature encoding using `LabelEncoder`

The categorical columns encoded were:

* Education
* City
* Gender
* EverBenched

## 🤖 Machine Learning Model

### Random Forest Classifier

The project uses **Random Forest Classifier** for predicting employee leave status.

Model parameters:

```python
RandomForestClassifier(
    n_estimators=100,
    random_state=42
)
```

## 📂 Train-Test Split

The dataset is divided into:

* **80% Training Data**
* **20% Testing Data**

Stratified splitting is used to maintain the target-class distribution.

## 📈 Model Evaluation

The model performance is evaluated using:

### Accuracy Score

```python
accuracy_score(y_test, y_pred)
```

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* KaggleHub

## 💾 Model Saving

The trained Random Forest model is saved using Joblib:

```python
joblib.dump(rf_model, "rf_model.joblib")
```

The encoder is also saved for future use.

## 📁 Project Structure

```text
employee-prediction-ml/
│
├── employee_dataset(1).ipynb
├── Employee.csv
├── rf_model.joblib
├── LabelEncoder.joblib
└── README.md
```

## 🚀 How to Run

1. Clone this repository.
2. Install the required Python libraries.
3. Open `employee_dataset(1).ipynb` in Jupyter Notebook or Google Colab.
4. Run the notebook cells in order.
5. Train the Random Forest model.
6. Generate predictions.
7. Check the Accuracy Score.

## 🔮 Future Improvements

* Hyperparameter tuning
* Feature selection
* Cross-validation
* Comparison with other classification algorithms
* Streamlit web application
* Improved model deployment

## 👨‍💻 Author

**Hemant Rajput**

⭐ If you like this project, consider giving the repository a Star!
