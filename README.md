# AI_Intern_Challenge
# BBC News Text Classification
This project applies **text classification** to the publicly available [BBC News dataset](https://www.kaggle.com/competitions/learn-ai-bbc/code).   It was selected to **comply with the challenge requirements**

## 📂 Dataset
The dataset consists of BBC news articles labeled into 5 categories:
- **Business**
- **Entertainment**
- **Politics**
- **Sport**
- **Tech**

It is offered in two files:
- `BBC News Train.csv`
- `BBC News Test.csv`

⚠️ The **test file was not used** in this project since it lacks the `Category` label, which is required for supervised learning.

---

## 🔎 Project Workflow

### 1. Data Loading & Inspection
- Loaded the training dataset.
- Explored dataset shape, categories, and their value counts.

### 2. Train/Validation Split
- Performed an **80/20 stratified split** to ensure balanced class representation.

### 3. Text Preprocessing
- Converted all text to lowercase.
- Removed URLs, emails, and non-alphabetic characters.
- Removed single-character tokens and stopwords.
- Result: cleaner text, improving model quality.

### 4. Exploratory Data Analysis (EDA)
- Checked number of samples per category.
- Analyzed **most common words overall** and **per category**.

### 5. Model Training
- **TF-IDF vectorization** was used to convert text into numerical features.
- Two models were trained and evaluated:
  - **Logistic Regression**
    - Validation Accuracy: **0.966**
  - **Naive Bayes (MultinomialNB)**
    - Validation Accuracy: **0.973**

### 6. Interactive Prediction Script
A script was created where the user can input sentences, and both models predict the category.  
Example run:

Prediction Script Test
Type 'exit' to quit.

Enter a sentence: The singer released her latest album, and fans are raving about it.
Logistic Regression predicts: entertainment
Naive Bayes predicts: entertainment

Enter a sentence: The football team won the championship after a thrilling final match.
Logistic Regression predicts: sport
Naive Bayes predicts: sport

---

### 7. Confusion Matrix Visualization
- Confusion matrices for both models show strong performance with high diagonal values (indicating correct predictions across all categories).

