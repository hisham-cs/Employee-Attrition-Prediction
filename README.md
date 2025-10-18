# Employee-Attrition-Prediction

This project is a dive into machine learning to figure out why employees leave their jobs. Using a classic dataset from Kaggle. 

## 📋 About The Project

The main goal is to build a model that can predict employee attrition (whether an employee will leave or stay). This is a common and important problem for companies to solve, and this project walks through the entire process from cleaning the data to evaluating the final model.

## ⚙️ How It Works

The process is broken down into a few main steps in the Jupyter Notebook:

1.  **Data Prep & Cleaning:** First, I loaded the data and got rid of columns that wouldn't be useful for prediction, like `EmployeeNumber` and `StandardHours` (since everyone has the same value).

2.  **Preprocessing:** Machines only understand numbers, so I had to convert all the text data.
    * For columns with two options (like 'Yes'/'No'), I used `LabelEncoder`.
    * For columns with multiple categories (like 'JobRole' or 'Department'), I used `OneHotEncoder` to create dummy variables. This helps the model understand the categories without assuming one is more important than another.

3.  **Training the Model:** I split the data into a training set (80%) and a testing set (20%). The model learns the patterns from the training data, and then we check its performance on the unseen test data. I also scaled the features using `StandardScaler` to make sure everything was on a level playing field. I chose a **Logistic Regression** model for this classification task.

4.  **Evaluation:** So, how good is the model? I checked a few key metrics:
    * **Accuracy:** The model was about **88%** accurate overall.
    * **Precision & Recall:** I created a confusion matrix and a classification report to see how well it did at identifying employees who actually left. While the overall accuracy is high, the model is better at predicting who will stay than who will leave.

## 💡 Key Findings

The most interesting part! After training, I looked at the model's coefficients to see which features had the biggest impact on its predictions. The notebook includes a bar chart that visualizes the **top 10 factors** that are most strongly correlated with an employee leaving. This gives us a clear idea of what might be driving attrition.

## 🚀 How to Run

To get this running on your own machine:

1.  Make sure you have Python and Jupyter Notebook installed.
2.  Clone this repository.
3.  Install the necessary libraries. You can usually do this by running:
    ```bash
    pip install pandas scikit-learn matplotlib seaborn
    ```
4.  Open and run the `Employee_Attrition_Prediction.ipynb` notebook. The dataset `Employee-Attrition.csv` should be in the same folder.

## 🛠️ Technologies Used

* **Python**
* **Pandas** (for data manipulation)
* **Scikit-learn** (for building the machine learning model)
* **Matplotlib & Seaborn** (for data visualization)
