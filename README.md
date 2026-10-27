# Phishing Website Detection Using SVM

## 📌 Project Overview

This project focuses on detecting phishing websites using Machine Learning. It implements a Support Vector Machine (SVM) classifier trained on the **PhiUSIIL Phishing URL Dataset** to classify websites as phishing or legitimate based on various URL and website-related features.

The model analyzes numerical website features and predicts whether a website is potentially fraudulent or genuine.

## 🎯 Project Objectives

The main objectives of this project are:

- Detect phishing websites using Machine Learning.
- Train an SVM classification model using website-related features.
- Preprocess and prepare the dataset for model training.
- Evaluate the model using classification performance metrics.
- Visualize model performance using a Confusion Matrix and ROC Curve.

## 🛠️ Technologies Used

The following technologies and libraries are used in this project:

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## 📂 Dataset

**Dataset Name:** PhiUSIIL Phishing URL Dataset

The dataset contains various URL and website-related features, along with labels indicating whether a website is phishing or legitimate.

These features are used to train the SVM model to identify potential phishing websites.

## 🧹 Data Preprocessing

The following preprocessing steps are performed:

1. Load the dataset from a CSV file.
2. Remove records with missing target labels.
3. Drop non-numeric and irrelevant columns, including:
   - URL
   - Domain
   - TLD
   - Title
   - Label
4. Convert target labels into binary values.
5. Replace infinite values with NaN.
6. Handle missing numerical values using median imputation.
7. Select numerical features for model training.
8. Split the dataset into training and testing sets.

## 🤖 Machine Learning Model

The classification algorithm used in this project is:

**Linear Support Vector Machine (LinearSVC)**

The model is implemented using a Scikit-learn pipeline consisting of:

- **StandardScaler:** Standardizes numerical features.
- **LinearSVC:** Performs classification using a linear Support Vector Machine.

### Model Parameters

```python
LinearSVC(
    C=1.0,
    class_weight="balanced",
    random_state=42,
    max_iter=5000
)
```

### Dataset Split

The dataset is divided into two parts:

- Training Set: 80%
- Testing Set: 20%

The training data is used to train the model, while the testing data is used to evaluate its performance on unseen data.

## 📊 Evaluation Metrics

The trained model is evaluated using the following metrics:

- **Confusion Matrix:** Displays the number of correctly and incorrectly classified websites.
- **Precision:** Measures how many websites predicted as phishing are actually phishing.
- **Recall:** Measures how many actual phishing websites are correctly identified.
- **F1-Score:** Represents the balance between precision and recall.
- **ROC-AUC Score:** Measures the model's ability to distinguish between phishing and legitimate websites.
- **Classification Report:** Provides precision, recall, F1-score, and support for each class.

## 📈 Visualizations

### Confusion Matrix

The Confusion Matrix visualizes the classification results, showing the number of correctly and incorrectly predicted phishing and legitimate websites.

### ROC Curve

The ROC Curve illustrates the model's ability to distinguish between phishing and legitimate websites at different classification thresholds.

It also helps evaluate the classification performance using the ROC-AUC score.

## 📁 Project Structure

```text
Phishing-Website-Detection-Using-SVM/
│
├── ML task 9.py
├── PhiUSIIL_Phishing_URL_Dataset.csv
└── README.md
```

## ▶️ How to Run the Project

### 1. Install Dependencies

Install the required Python libraries using the following command:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 2. Update the Dataset Path

Make sure the dataset CSV file is available in the project directory.

Update the dataset path in the Python script if necessary:

```python
df = pd.read_csv("PhiUSIIL_Phishing_URL_Dataset.csv")
```

### 3. Execute the Python Script

Run the following command in the terminal or command prompt:

```bash
python "ML task 9.py"
```

## 📌 Expected Output

After executing the program, the following outputs are generated:

- Dataset summary and information.
- Class distribution of phishing and legitimate websites.
- Trained SVM classification model.
- Confusion Matrix visualization.
- Precision, Recall, F1-Score, and ROC-AUC values.
- Classification Report.
- ROC Curve visualization.

## 🎓 Learning Outcomes

Through this project, you will learn:

- Data preprocessing and cleaning techniques.
- Numerical feature selection.
- Machine Learning classification using SVM.
- Model training and testing.
- Evaluation of classification models using performance metrics.
- Data visualization using Matplotlib and Seaborn.
- Application of Machine Learning to phishing website detection.

## 🏁 Conclusion

This project demonstrates how Machine Learning can be used to detect phishing websites using a Support Vector Machine classifier.

By analyzing website-related features and evaluating the model using different classification metrics, the project provides a practical understanding of how Machine Learning can help identify potentially fraudulent websites and improve website security.
