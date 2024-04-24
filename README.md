# email-classifier
Mini-project for SC1015 - Introduction to Data Science and Artificial Intelligence

## **Our motivation**
There is an increasing number of scam victims. To combat this, we aim to use AI/ML to help humans flag out spam emails which may contain links to phishing scams, or ransom scams.</br>

## **Preparing the Data**
To train the model, we used a dataset from <a href="https://www.kaggle.com/datasets/gokulraja84/emails-dataset-for-spam-detection">Kaggle</a> containing unstructured email text data, each labeled scam or not scam.</br>
To make sense of the unstructured text, we had explore methods to "clean" it in each case. 
<ul>
  <li>Exploratory Data Analysis : NLP Pre-processing Techniques ("Tokenization", Lemmatization, Removing Stopwords)</li>
  <li>Training Machine Learning Models : NLP Techniques and Vectorization</li>
</ul>
These were done writing our own "Tokenization" function that included lowercasing and removing punctuations ,and using the NLTK library.</br></br>

We also counted the number of words that appeared in each category -- Spam and Not Spam.</br>
We found that there were anomalous amounts of certain words so we added them to our stoplist and refined the "cleaned" data.  
 
## **Exploratory Data Analysis**
In the clean data, we compared the most frequently appeared words in each category.</br>

### Similarities
We found that [“com”, “please”, and integers] commonly appeared in the both categories, and hypothesized that they don’t tell us much about the type of an email.</br>
Using a correlation matrix, we found our hypothesis to be true. The appearance of the words had low correlation with either category. 
### Differences
We found 2 groups of words that are uniquely found in the frequency list of Spam. We highlight them in the notebook as they relate to each other to form meanings.

## **Using Machine Learning (ML) to solve our problem:**
Our problem is a classification problem. We explored 4 other classification models outside the course and compared their accuracies :
<ol>
  <li>Logistic Regression - 98.3%</li>
  <li>Naive Bayes Classification - 91.1%</li>
  <li>Support Vector Machine - 99.2%</li>
  <li>Random Forest Classification - 98.2%</li>
</ol>
Comparing the models, we provide explanation in our <a href="https://youtu.be/6jYIe_tZf1E">video presentation</a> as to why SVM was the most accurate model.

## **Closing Points**
### **Did we solve our problem?**
Support Vector Machine is our model of choice and it provides remarkable accuracy in detecting spam, which effectively solves our problem.
### **Going forward...**
The obseravtions made from our Exploratory Data Analysis show that certain keywords appear more in spam emails. On top of the already effective model, we would advice users to be aware of such keywords, even if emails are not flagged to be spam. This can cover the remaining 0.8%.
</br>
</br>
Contributions:</br>
Gaoyuan: Part 1, Part 2, Part 3.1</br>
Ping Wee: Part 3.2 - 3.4, Part 4
