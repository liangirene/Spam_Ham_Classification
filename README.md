# Spam_Ham_Classification

Spam emails have become a major nuisance, cluttering our inboxes and potentially leading to security risks. The goal of this project was to build an effective filter that can accurately classify emails as spam (junk, commercial, or bulk) or ham (non-spam) based on their content. By accurately identifying spam emails, I aimed to prevent them from reaching users' inboxes and ensure a better email experience.

## Data Source
The dataset consists of email messages and their labels (0 for ham, 1 for spam). The labeled training dataset contains 8348 labeled examples, and the unlabeled test set contains 1000 unlabeled examples.

## Feature Engineering
When classifying emails as ham or spam, the primary challenge lies in that the data is in text format, while logistic regression requires numeric features. To bridge this gap, I employed feature engineering techniques to transform the email text into meaningful numeric representations. By creating a feature matrix 𝑋, with each row corresponding to an email and each column representing a specific feature, I was able to apply logistic regression as a classification algorithm. This approach enabled accurate classification based on the extracted numeric representations.

## Exploratory Data Analysis (EDA)
I identified features that could effectively differentiate between the spam and ham. This involved extracting meaningful features from the email text, such as the presence of specific words, email length, punctuation usage, and other relevant characteristics. Some feature ideas I explored included:

- Number of characters in the subject/body: Longer emails may exhibit distinctive patterns in ham emails
- Number of words in the subject/body: The length of the email can provide insights into its content
- Use of punctuation: The usage of specific punctuation marks, such as exclamation points or dollar signs, is often a characteristic of spam emails
- Number/percentage of capital letters: Excessive capitalization is often a characteristic of spam emails
- Proportion of emails in each class containing a particular set of words: When dealing with binary indicators like the presence of a particular word in the email text, I compared the proportion of spam emails containing the word to the proportion of ham emails containing the same word.

## Visualizations and ROC Curve
Through exploratory data analysis, I gained insights into the characteristics of spam and ham emails, which helped identify relevant features that could distinguish between the two. I analyzed the distribution of features, created visualizations such as histograms and kernel density plots, and explored patterns that aided in feature selection. One important visualization I used was the **Receiver Operating Characteristic (ROC) curve**, which helped assess the performance of the classifier at various thresholds.

## Model Training and Evaluation
The choice of classifier for this project was logistic regression with `scikit-learn`. By training the logistic regression model on the labeled dataset, I learned the underlying patterns and created an effective spam filter. To evaluate the performance of my classifier, I used various evaluation metrics such as precision, recall, and false-alarm rate. The ROC curve aided in selecting an appropriate threshold that balanced the detection of spam emails while minimizing false positives.

## Improvement Strategies
Throughout the project, I strived to improve the accuracy of my spam filter. This involved exploring different strategies, such as finding better features based on the email text, selecting more informative words, and considering additional data processing techniques. I also performed model selection by tuning hyperparameters, such as the regularization parameter, to optimize the classifier's performance.
