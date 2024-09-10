# Twitter-Sentiment-analysis
This project involves classifying tweets as fraudulent or non-fraudulent using a dataset of tweets. The model is trained to predict whether a tweet is fraudulent This project is a **Twitter Sentiment Analysis** using Natural Language Processing (NLP) techniques and machine learning models. The goal is to classify tweets as either positive or negative based on their content. The project involves the following steps:

### **Project Overview:**
The dataset contains pre-processed Twitter data with a **`target`** label representing sentiment (0 for negative and 1 for positive), as well as other features like the **`id`**, **`date`**, **`flag`**, **`user`**, and **`text`**.

### **Steps Involved:**

#### **1. Data Loading:**
The dataset is loaded from a CSV file and assigned proper column names for ease of reference.

#### **2. Data Preprocessing:**
- **Handling Missing Values:** There are no missing values in the dataset, ensuring the data is clean for further analysis.
- **Duplicates Removal:** The dataset is checked for duplicate rows, and no duplicates are found.
- **Label Transformation:** The **`target`** column contains values 0 and 4, where 4 represents positive sentiment. This is replaced with 1 to standardize the labels (0 for negative, 1 for positive).
- **Text Cleaning and Tokenization:** The tweet text is processed by removing special characters and converting the text to lowercase. The `PorterStemmer` from NLTK is used to stem the words, reducing them to their root forms. Stopwords are removed to enhance the focus on important words.

#### **3. Feature Engineering:**
The textual data is transformed into numerical data using **TF-IDF Vectorization** (`TfidfVectorizer`). This converts the words in the tweets to vectors based on their importance in the dataset, making it ready for the machine learning model.

#### **4. Data Splitting:**
The dataset is split into training and testing sets, using an 80-20 split with stratification to ensure that both sets maintain the distribution of positive and negative sentiments.

#### **5. Model Training:**
The **Logistic Regression** algorithm is applied to classify the tweets into positive or negative categories based on the vectorized tweet content. Logistic Regression is a commonly used algorithm for binary classification tasks due to its simplicity and efficiency.

#### **6. Model Evaluation:**
- **Accuracy:** The model achieves an accuracy of ~77.73% on the test set.
- **Precision, Recall, and F1-Score:** These metrics are calculated to evaluate the performance of the model in distinguishing between positive and negative tweets. The F1-score is ~78.13%, indicating a good balance between precision and recall.
- **ROC-AUC Score:** The AUC-ROC score is ~77.73%, indicating the model's ability to differentiate between classes.
- **Confusion Matrix and Classification Report:** A confusion matrix is plotted, and a detailed classification report is generated to provide further insights into the performance of the model on the test data.

#### **7. Visualizations:**
- A bar chart is created to compare the actual and predicted counts of positive and negative tweets.
- A pie chart is used to visualize the proportions of accuracy, precision, recall, F1-score, and ROC-AUC scores.

### **Key Features:**
- **Text Cleaning & Preprocessing:** Removing noise and preparing data for machine learning.
- **Binary Classification:** Predicting positive or negative sentiment.
- **Evaluation Metrics:** Comprehensive performance evaluation using accuracy, precision, recall, F1-score, and ROC-AUC.
- **Data Visualizations:** Graphical representations for better understanding of model performance.

This project demonstrates how text-based data can be analyzed and classified using NLP and machine learning techniques, providing valuable insights into sentiment analysis.


Feel free to fork the repository, make changes, or improve the model as you see fit!


