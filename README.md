# email-classifier
Mini-project for SC1015 - Introduction to Data Science and Artificial Intelligence

### **Importing Basic Libraries and cleaning data**:
So we first start by importing some basic libraries: numpy, pandas,  seaborn and matplotlib to help us with plots and graphs in later exploratory analysis. We then imported our dataset of emails which can be found on Kaggle.com. Then we did some basic cleaning of the data frame removing all the useless information such as blocks that are NaN

### **Exploratory Data Analysis:**
We imported the nltk library which contained basic NLP tools such as Lemmatizers, transformers, tokenizers to help us extract the features of the unstructured text data. So getting the most common words out, we found some anomalies, words that are weird but common, such as “Enron”, ”etc” and added them to the stop word list to be removed. Also we made a replace list of tabs and spaces to replace all the stop words.
We removed all the stop words from the data, and counted the most frequently appeared words in spam and non spam emails respectively. Displaying the result, we found that “com”, “please”, and integers are both common in the 2 types. We hypothesized that they don’t tell us much about the type of an email.
Using a correlation matrix, we found our hypothesis is true. So we ignored these 3 kinds of words. After this we found 2 groups of words that are commonly found in spam, and hypothesized about the meaning behind them.

### **Using Machine Learning (ML) to solve our problem:**
We first imported the sklearn library to split the data into train and test datasets. And also the vectorizer to extract features of the text. 







### Contributions:
Gaoyuan: Part1, Part3.1, Part2
PingWee: Part3.2, 3.3, 3.4, Part4
