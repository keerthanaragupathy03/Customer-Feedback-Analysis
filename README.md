# Customer Review Analysis using Machine Learning

## 📌 Project Overview

This project analyzes customer reviews and classifies them into **Positive, Neutral, and Negative** sentiments using Natural Language Processing (NLP) and Machine Learning techniques.

The project uses customer review data from the **Cell Phones and Accessories** dataset and applies text preprocessing, TF-IDF feature extraction, and Logistic Regression for sentiment classification.

## 🎯 Objectives

- Analyze customer review data
- Clean and preprocess review text
- Classify reviews based on their ratings
- Convert text data into numerical features using TF-IDF
- Build a Logistic Regression sentiment classification model
- Evaluate the model performance
- Predict the sentiment of a new customer review

## 🛠️ Technologies Used

- **Python**
- **Pandas** – Data loading and manipulation
- **Matplotlib** – Data visualization
- **Seaborn** – Sentiment distribution visualization
- **Regex (re)** – Text preprocessing
- **Scikit-learn** – Machine Learning
- **TF-IDF Vectorization** – Text feature extraction
- **Logistic Regression** – Sentiment classification

## 📂 Dataset

The project uses the **Cell Phones and Accessories** customer review dataset.

The dataset contains customer review information including:

- `reviewText` – Customer review
- `overall` – Customer rating
- `helpful` – Helpful votes information

For analysis, the project mainly uses:

- `reviewText`
- `overall`

## 🔄 Project Workflow

```text
Customer Review Dataset
          ↓
     Data Loading
          ↓
    Data Exploration
          ↓
    Data Cleaning
          ↓
  Select Review & Rating
          ↓
   Sentiment Labeling
          ↓
   Text Preprocessing
          ↓
   TF-IDF Vectorization
          ↓
    Train-Test Split
          ↓
 Logistic Regression Model
          ↓
 Model Prediction
          ↓
 Model Evaluation
          ↓
 New Review Prediction
```

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the JSON review dataset.
2. Converted the data into a Pandas DataFrame.
3. Checked the dataset information and missing values.
4. Removed the `helpful` column.
5. Selected `reviewText` and `overall` columns.
6. Converted ratings into sentiment labels.
7. Converted review text into lowercase.
8. Removed special characters and numbers.
9. Removed extra spaces from the review text.

### Sentiment Classification

The customer rating is converted into three sentiment categories:

| Rating | Sentiment |
|---|---|
| 4–5 | Positive |
| 3 | Neutral |
| 1–2 | Negative |

## 📊 Exploratory Data Analysis

A sentiment distribution visualization is created using **Seaborn** to understand the number of Positive, Neutral, and Negative reviews in the dataset.

## 🔤 TF-IDF Feature Extraction

TF-IDF (**Term Frequency-Inverse Document Frequency**) is used to convert customer review text into numerical features that can be processed by the machine learning model.

```python
TfidfVectorizer()
```

The transformed review text is then used as the input for the classification model.

## 🤖 Machine Learning Model

### Logistic Regression

A **Logistic Regression** model is used to classify customer reviews into:

- Positive
- Neutral
- Negative

The dataset is divided into:

- **80% Training Data**
- **20% Testing Data**

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

## 📈 Model Evaluation

The model is evaluated using:

- **Accuracy Score**
- **Classification Report**
- **Confusion Matrix**

These evaluation techniques help measure how effectively the model predicts customer sentiment.

## 🔮 New Review Prediction

The trained model can also predict the sentiment of a new customer review.

Example:

```text
"The product is good"
```

The review is converted into TF-IDF features and passed to the trained Logistic Regression model to predict its sentiment.

## 📁 Project Structure

```text
Customer-Review-Analysis/
│
├── customer_review_Analysis.ipynb
├── Cell_Phones_and_Accessories_5.json
├── data.csv
└── README.md
```

> **Note:** The dataset file is required to run the notebook because the notebook loads the JSON dataset directly.

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Open the project folder

```bash
cd Customer-Review-Analysis
```

### 3. Install required libraries

```bash
pip install pandas matplotlib seaborn scikit-learn
```

### 4. Open the Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
customer_review_Analysis.ipynb
```

### 5. Run the cells

Run the notebook cells sequentially to perform data analysis, preprocessing, model training, evaluation, and sentiment prediction.

## 💡 Key Learning Outcomes

Through this project, I gained practical experience in:

- Data Cleaning
- Exploratory Data Analysis
- Natural Language Processing
- Text Preprocessing
- TF-IDF Feature Extraction
- Sentiment Analysis
- Machine Learning Classification
- Model Evaluation
- Python Data Analysis using Pandas

## 👩‍💻 Author

**Keerthana Raghupathy**

Computer Science and Engineering Student

---

⭐ If you find this project useful, feel free to star the repository.
