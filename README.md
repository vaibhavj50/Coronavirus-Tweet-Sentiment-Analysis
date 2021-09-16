# Coronavirus-Tweet-Sentiment-Analysis

# Index
1. Introduction
2. Exploratory Data Analysis./Reviwing Our Dataset
3. Data Preprocessing.
4. Model Training- MULTICLASS AND BINARY.
5. Evaluation.
6. Conclusion

# 1. Introduction
Our objective is to build a classification model to predict the sentiment of COVID-19 tweets.The tweets have been pulled from Twitter and manual tagging has been done then. The names and usernames have been given codes to avoid any privacy concerns.

![image](https://user-images.githubusercontent.com/84126197/133555061-d39d739f-ae0a-42ea-9389-72acadcb4397.png)

We are given the following information:
Username: Unique user-IDs of the users
Location: Location of the user
Tweet At: Date at which the tweet was made
Original Tweet: The exact tweet
Sentiment: Sentiment of the tweet

# Workflow in this Project

![image](https://user-images.githubusercontent.com/84126197/133555175-1476781e-cf97-472d-a815-ef75edc57b88.png)

# 2. Exploratory Data Analysis
The original dataset has 6 columns and 41157 rows.

There are five types of sentiments- Extremely Negative, Negative, Neutral, Positive and Extremely Positive.

![image](https://user-images.githubusercontent.com/84126197/133555221-2067da31-9610-44b2-b719-c05a26871e5f.png)

All tweets data collected from the months of March and April 2020. Bar plot shows us the number of unique values in each column.
![image](https://user-images.githubusercontent.com/84126197/133555271-9eed4b85-7a21-44b9-a4fc-0a904120e97f.png)


The columns such as “UserName” and “ScreenName” does not give any meaningful insights for our analysis.

There are 20.87%(8567) null values in various places of location column.

Most of the tweets came from London followed by U.S. 
![image](https://user-images.githubusercontent.com/84126197/133555299-736a3dfe-f88c-4262-b7a0-d8abac0cd3ba.png)


# 3. Data Preprocessing
The preprocessing of the text data is an essential step as it makes the raw text ready for mining.

The objective of this step is to clean noise those are less relevant to find the sentiment of tweets such as punctuation, special characters, numbers, and terms which don’t carry much weightage in context to the text.

Stop words are those words in natural language that have a very little meaning, such as "is", "an", "the", etc.To remove stop words from a sentence, you can divide your text into words and then remove the word if it exits in the list of stop words provided by NLTK.

Stemming is a rule-based process of stripping the suffixes (“ing”, “ly”, “es”, “ed”, “s” etc) from a word. For example – “play”, “player”, “played”, “plays” and “playing” are the different variations of the word – “play”.

Lemmatization is a more powerful operation, and it takes into consideration morphological analysis of the words. It returns the lemma which is the base form of all its inflectional forms.

In tokenization we convert group of sentence into token . It is also called text segmentation or lexical analysis. It is basically splitting data into small chunk of words. Tokenization in python can be done by python NLTK library’s word_tokenize() function

After cleaning text we also create wordblog
![image](https://user-images.githubusercontent.com/84126197/133555338-8c819e2e-d4fe-4a27-913a-cdf743e699af.png)

4. Model Training- MULTICLASS AND BINARY.
Trained 7 different algorithms for each Multiclass and Binary classification. In Multiclass we have 5 different classes but in binary we have only two class i.e. Positive and Negative. The algorithms that were used -

Logistic Regression
Support Vector Machine
Random Forest
Naive Bayes
Stochastic Gradient Descent
XGBosst
CatBoost
5. Evaluation
For Multiclass Classification we got accuracy as -
![image](https://user-images.githubusercontent.com/84126197/133555368-3a30e55a-af35-4c4d-9e10-36c4c63733aa.png)

For Binary Classification we got accuracy as -
![image](https://user-images.githubusercontent.com/84126197/133555379-064ba285-a6bb-495d-89fc-1a08a46412dd.png)

Also Confusion Matrix for Binary Classification -
![image](https://user-images.githubusercontent.com/84126197/133555385-f877269c-675f-4e86-aaee-fc6eed50fa1e.png)


