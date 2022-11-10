
# Software Sentiment Analysis

The objective of the project is to classify the sentiments of software discussions on open source developer platforms - AppReviews, JIRA and Stack Overflow.

Multiple models were built using various Word Embedding techniques and Classification Models and they were evaluated using Accuracy and F1 Score metrics.

The three Datasets used for the project - one each from JIRA, Stack Overflow and AppReviews can be found in the Datasets folder.




## Word Embeddings
Six Word Embedding techniques were applied:
1. CountVec
2. TF-IDF
3. CBOW
4. Skip-Gram
5. Word2Vec
6. GloVe 300d

The codes for each of these word embeddings can be found in the Codes folder.
## Classification Techniques
The predictive ability of the different Word Embedding techniques used are evaluated using 13 different classifiers:
1. Multinomial Naive Bayes
2. Bernoulli’s Naive Bayes
3. Gaussian Naive Bayes
4. Complement Naive Bayes
5. Decision Tree Classifier
6. KNeighbours Classifier with Bagging Classifier
7. RandomForestClassifier
8. ExtraTreesClassifier
9. AdaBoostClassifier
10. GradientBoostingClassifier
11. SVM with Linear Kernel
12. SVM with Polynomial Kernel
13. SVM with RBF Kernel

The codes for each of these classifiers can be found in the 'Models.ipynb' file in the Codes folder.
## Outputs
A total of 18 files (numbered from 1 to 18) are generated as output after applying the classification techniques on the word embedding generated files. These can be found in the Outputs folder.

Each file consists of 14 columns, the first 13 corresponding to the outputs (predictions) of applying the 13 classifiers on the input word embedding generated file and the last column corresponds to the observed output for each data point.

The numbering system for the files is as follows:
* Files 1.csv - 6.csv take input as files generated by applying word-embeddings on the AppReviews Dataset.<br/>
* Files 7.csv - 12.csv take input as files generated by applying word-embeddings on the JIRA Dataset.<br/>
* Files 13.csv - 18.csv take input as files generated by applying word-embeddings on the Stack Overflow Dataset.<br/>

Each set of six files are generated by applying the following word embeddings in given order on the datasets: CountVec, TF-IDF, CBOW, Skip-Gram, Word2Vec, GloVe 300d

## Evaluation Metrics
The generated models (18 word-embedding files * 13 Classifiers) are evaluated using Accuracy, Precision, Recall and F1 Metrics, the codes of which are in the 'Metrics.ipynb' file of the Codes folder.

The output files are generated are as follows:
* 'acc.csv' - Accuracies of all the models
* 'pre.csv' - Precision of all the models
* 'rec.csv' - Recall of all the models
* 'fmea'csv' - F1 Scores of all the models

Each file consists of 18 rows, correspnding to the 18 Dataset - Word Embedding combinations and 13 columns, each corresponding to the 13 classification techniques.

The output files can be found in the Output folder.
