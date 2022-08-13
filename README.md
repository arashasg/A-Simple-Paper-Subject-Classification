# A-Simple-Paper-Subject-Classification
In this repository, I present a simple way to classify the papers' subjects using only TF-IDF.

##### Dataset
I used Pubmed API, which is an API for access to medical papers. I searched for five queries: Breast Cancer, Heart Rate, EEG, Obesity, and covid-19. For each of these terms, I saved 500 papers for the train set and 150 for the test set. 

##### Preprocessing 
For this stage, I removed stopwords and words with a length of less than two. I normalized all words and sentences, turned the words to lower case, and removed punctuations. 

##### Model
For the model, First, I merged all the papers and found the frequency of each word across all papers. Then, I found the frequency of words in each class of papers and found the words with the highest tf-idf score. I created five vectors for the five classes and stored the top five words of each class in them. Finally, to classify a given paper, I counted these words. The paper will be assigned to the class with the highest number of high-scored words in the paper.

##### evaluation
I used the papers in the test set to evaluate this approach and achieved an accuracy of 76 percent on the test set.
Here I have presented the confusion matrix of the model predictions:

![Confusion Matrix Image](https://github.com/arashasg/A-Simple-Paper-Subject-Classification/blob/main/img/Capture.PNG?raw=true)
