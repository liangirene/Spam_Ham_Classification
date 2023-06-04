# Spam_Ham_Classification

Spam emails have become a major nuisance, cluttering our inboxes and potentially leading to security risks. The goal of this project was to build an effective filter that can accurately classify emails as spam (junk or commercial or bulk) or ham (non-spam) based on their content. By accurately identifying spam emails, I aimed to prevent them from reaching users' inboxes and ensure a better email experience.

## Data Collection
The dataset consists of email messages and their labels (0 for ham, 1 for spam). The labeled training dataset contains 8348 labeled examples, and the unlabeled test set contains 1000 unlabeled examples.

## Feature Engineering
To transform the text data into a format suitable for training a classifier, I employed feature engineering techniques. These techniques involved extracting meaningful features from the email text, such as the presence of specific words, email length, punctuation usage, and other relevant characteristics. By representing emails with numeric features, I enabled the use of machine learning algorithms for classification. Some feature ideas I explored included:

- Number of characters in the subject/body: Longer emails may exhibit distinctive patterns that can aid in classification.
- Number of words in the subject/body: The length of the email can provide insights into its content, allowing me to distinguish spam from legitimate emails.
- Use of punctuation: I examined the usage of specific punctuation marks, such as exclamation points or dollar signs, to help identify spam emails.
- Number/percentage of capital letters: Excessive capitalization is often a characteristic of spam emails and can be utilized as a feature.
- Reply or Forwarded emails: I analyzed whether an email was a reply to or a forwarded message, providing valuable information for spam detection.

## Exploratory Data Analysis (EDA)
I identified features that could effectively differentiate between the spam and ham. One approach I explored was comparing the proportion of emails in each class containing a particular set of words. When dealing with binary indicators like the presence of a particular word in the email text, I compared the proportion of spam emails containing the word to the proportion of ham emails containing the same word. This comparison provided valuable insights into the distinctive characteristics exhibited by each category, aiding in the classification process.

## ROC Curve
Through exploratory data analysis, I gained insights into the characteristics of spam and ham emails, which helped me identify relevant features that could distinguish between the two. I analyzed the distribution of features, created visualizations such as histograms and kernel density plots, and explored patterns that aided in feature selection. One important visualization I used was the Receiver Operating Characteristic (ROC) curve, which helped me assess the performance of the classifier at various thresholds.

## Model Training and Evaluation
The choice of classifier for this project was logistic regression, a popular algorithm for binary classification tasks. By training the logistic regression model on the labeled dataset, I learned the underlying patterns and created an effective spam filter. To evaluate the performance of my classifier, I used various evaluation metrics such as accuracy, precision, and recall. The ROC curve aided in selecting an appropriate threshold that balanced the detection of spam emails while minimizing false positives.

## Improvement Strategies
Throughout the project, I strived to improve the accuracy of my spam filter. This involved exploring different strategies, such as finding better features based on the email text, selecting more informative words, and considering additional data processing techniques. I also performed model selection by tuning hyperparameters, such as the regularization parameter, to optimize the classifier's performance.
