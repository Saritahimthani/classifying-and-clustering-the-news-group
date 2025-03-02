# classifying-and-clustering-the-news-group

I leveraged an algorithmic approach for document classification and document clustering. Various models have been trained for document classification and they all have been evaluated using performance metrics followed by tuning of the model hyper-parameters to reach the most accurate classification. Additionally, a model has been trained for document clustering, which is followed by a dimensionality reduction technique to visualize the document clusters in 2D space.

## Research Questions
Following are the research questions that the project
attempts to answer:
- Does the number of documents and the number of
classes have an impact on the classification accuracy?
- Can a document be classified into one of the available
classes?
- Are there clusters which can group the documents
belonging to the similar topic?

## Dataset
For document classification and clustering, a favorable
dataset is the one that has a huge number of documents
spread across a variety of topics. ‘The 20 newsgroups text
dataset’ is one such dataset that has the following:

- 18846 newsgroups posts
- 20 topics

The entire dataset is already split into two subsets -
a training set and a testing set. The dataset is publicly
available under Real world datasets on scikit-learn.

These newsgroup posts belong to topics such as
graphics, atheism, hardware, baseball, christian, guns, and
so forth. After the thorough analysis of the dataset, it is
observed that there are documents that belong to mac, ibm,
graphics that come under the umbrella topic of computers.
There are posts that belong to hockey, baseball, motorcycle,
and autos that come under the umbrella topic of recreation.
However, three of the topics (atheism, forsale, and christian)
are the most different from the remaining 17 topics. Hence,
in this project, these three topics are not considered for the
purpose of document classification and document clustering,
and eventually, documents from these three topics won’t be
the candidates that would contribute to answering the
research questions.

## Classification Models

Following are
the models that are leveraged for classification:
- K-Nearest Neighbor (KNN) Classifier
- Support Vector Machine (SVM) Classifier
- Multinomial Naive Bayes (MNB) Classifier

## Clustering Model

Following is
the model that is leveraged for finding and allotting documents to clusters:
- K-Means Algorithm

## Dimensionality Reduction

Following is
the technique that is leveraged to visualize the document clusters in 2D space:
- Principal Component Analysis (PCA)

## Results

### Answer to Research Question 1
Does the number of documents and the number of
classes have an impact on the classification accuracy?
Yes, the number of training documents and the number of classes
does impacts the classification accuracy. It is seen that when
the documents belonging to the 17 individual groups are
clubbed to belong to just 4 groups, the classification model’s
accuracy increases. The classification accuracy of MNB
classifier and SVM classifier increases by approximately
19% and the KNN classifier increases by 220%.

### Answer to Research Question 2
Can a document be classified into one of the
available classes? Yes, by using the classification models
such as KNN, SVM, and MNB, it is possible to classify the
document to belong to one of the available classes.
However, all the models overfit the training documents with
KNN classifier overfitting the most and MNB classifier
overfitting the least. SVM classifier’s performance is
comparable to the MNB classifier but MNB classifier is able
to generalize better on the testing set documents. All the
hyper-tuned models classified the documents with higher
accuracy than their vanilla counterparts.

### Answer to Research Question 3
Are there clusters which can group the documents
belonging to the similar topic? Yes, K-Means algorithm
helps finding the clusters and the number of clusters
matches with the 4 clubbed groups i.e. Talk, Computer,
Science, and Recreation. Using PCA, it is possible to
visualize those clusters in the 2D space. Also, words from
the documents in each cluster are visualized through a Word
Cloud and on closely observing the words, it is seen that
words are related to the topic or cluster to which they
belong.