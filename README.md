#Sentiment Analysis of Amazon Customer Reviews using Web Scraping and NLP

Modeled a Support Vector Machine (SVM) in Python to classify whether a review represents a positive or negative sentiment. Trained model on word embeddings created using TF-IDF Bigrams on the Amazon Online Customer Reviews Data from Kaggle. Tested the model on new test data from Amazon.com obtained by using web crawling and web scraping techniques.

## Abstract 
The idea of the project is to do web crawling and to scrape the live Amazon customer reviews data of the different 
laptop manufactures and to perform sentiment analysis on the scraped dataset. After the sentiment analysis is done, the results for each and individual customer reviews are categorised into
 **pos - Positive**
 **neg - Negative**
for each individual customer’s review and is saved in a different CSV file for performing data visualisation. The bar
plots are drawn to visualise the number of people gave positive comments. 

## Implementation

The live Amazon customer reviews are scraped from the amazon.com for the different laptops using the scrapy library and the scraped reviews are
stored in a CSV File. To predict the reviews correctly, the language model needs a training dataset which was taken from the Kaggle.

https://www.kaggle.com/datafiniti/consumer-reviews-of-amazonproducts#1429_1.csv

This Kaggle dataset is taken for the training which is carried out using the Support Vector Machine. The scraped data which is talen as a different CSV files for different manufacturers is then preprocessed for error free text for which the prediction is made.
In order for the machine to understand the contextual language the documents needs to be vectorised. These vectorisation is carried away using the famous word vectorisation concept in Natural Language Processing called **Term Frequency-Inverse Document Frequency (TF-IDF)**. After the TF-IDF is done each individual documents(customer reviews ) are changed to the numerical value which will be used for prediction. Later it is made to fit to the classifier and the sentences polarity is predicted. These polarities after being acquired is saved to the same CSV file in
which a separate column named “sentiment” is created. 
