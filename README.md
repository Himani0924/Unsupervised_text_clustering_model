
**Abstract**

A local library wants to implement a categorizing system based on the similarity of the genres and the authors. This text clustering model will enable the librarian to assign the books into groups and subgroups based on their labels. This unsupervised learning model will apply various transformation and clustering techniques to choose the best algorithm to assign the correct labels to the books. Five books, written by different authors and from different genres, were extracted from the Project Gutenberg website. The data was preprocessed and partitioned into 200 partitions and each partition consisted of 150 words. Different text processing and dimension reducing techniques were used to transform the data. Unsupervised clustering algorithms were used on all data transformations to find out the best algorithm.

**Design**

The purpose of the model is to use text clustering techniques to assign books into similar groups or clusters. The model uses the data obtained from the Project Gutenberg website. The data was preprocessed using NLTK library by removing stop words and lemmatizing every word to its origin. BOW, TD-IDF and LDA techniques were used to transform the data. K-means and Hierarchical clustering algorithms were used on all three data transformations, respectively. V-measure score and Silhouette score were used for evaluating the performance of clustering algorithms against the true authors. LDA-transformed data was used to compare different silhouette scores to figure out the optimum number of clusters using K-means algorithm.

**Data**

The data was obtained from the Project Gutenberg website - https://www.gutenberg.org. The following books were extracted from this website using python library – requests: 

1.	Chaldea

2.	A Book About Lawyers

3.	EBook of Darwinism

4.	The Vicomte de Bragelonne

5.	A Popular History of Astronomy During the Nineteenth Century

All the books are by different authors and from different genres. The data was preprocessed using NLTK. The stop words and garbage characters were removed, all the words were converted to lower case and lemmatization was performed to return every word to its origin. The books were randomly partitioned into 200 partitions and each partition consisted of 150 words. The books were labelled as [a,b,c,d,e].


**Algorithms**

•	Data preprocessing:

o	removed stop words, garbage characters, all words converted to lower case, lemmatization performed

o	Unigrams/bigrams and Wordcloud used to find out the frequently used words in all 5 books


•	Feature Engineering:

o	Bag of Words (BOW)

o	TF-IDF

o	LDA 


•	Clustering Algorithms:

o	K-means

o	Hierarchical clustering


•	Evaluation scores:

o	V-measure

o	Silhouette score


**Tools**

•	Requests: For extracting books using their urls.

•	Pandas and Numpy: For cleaning data and preprocessing.

•	NLTK, gensim, scikit-learn: For processing text, topic modeling, clustering and evaluation

•	Matplotlib, Seaborn, Wordcloud, pyLDAvis, scipy : For visualizing the data.


**Communication**

Unigram and bigram techniques were used to show frequently used words in all the five books. One example is shown below:
 
![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/707e2f6b-43cf-43af-825d-7c8e2f320f34)


Wordcloud was used to show 50 frequently used words in all five books. One example is:

![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/4cc2db44-bba2-4b2c-a455-9ad578d98b37)

 
Feature engineering was performed using following techniques:

1.	BOW transformation

![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/0760d606-16b1-4657-b1ad-59b111496578)

 
2.	TF-IDF transformation

![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/abc913f0-ee54-4cec-8b01-cd86cc6458e9)

 
3.	LDA transformation

![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/ef39b464-5ec7-413e-8a30-07c0fa36dd29)

 

**Clustering algorithms on three transformations:**

**1.	BOW and K-Means algorithm:**

![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/9b6ee014-35e2-4c51-b561-d00c4a309f36)

 
**2.	BOW and Hierarchical clustering algorithm**
 
![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/fa53d5d3-5495-4395-b9b2-6da07cfa7c37)


**3.	TF-IDF and K-Means algorithm**


![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/021671c8-1d7e-44a1-aa06-000dbf390660)

 

**4.	TF-IDF and Hierarchical clustering algorithm**
 
![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/b2911e8d-c43b-478c-8353-3074767cb71d)


**5.	LDA and K-Means algorithm**


![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/05d23dcf-262e-4fb1-add8-237db5a22880)

 
**6.	LDA and Hierarchical clustering algorithm**

 
![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/1d4efcd8-a7d0-46c3-926f-4833c1fab0df)


	

**V-Measure for Evaluating Clustering Performance against the true authors**

 
![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/11fe9328-a083-4009-9b16-68570f9de742)



**Silhouette score for Evaluating Clustering Performance against the true authors**


![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/6a811b86-1307-4766-82d0-0ad5a3f98cd8)


 
**Comparison between Silhouette scores using different K numbers on LDA transformed data**
 
 ![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/8b2c27b8-c13e-465b-b9c7-8ad46adf44c4)

 
 ![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/93b9081d-1651-4113-a9b5-596d528e9906)

 ![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/2dc1fb7c-3512-4072-a417-c1d599e04b65)

 ![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/e32b5cf4-fa30-4af3-b682-9d83e257f440)

 ![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/e5f21571-e62b-4c01-b2e3-c4dc5c231320)

 ![image](https://github.com/Himani0924/Unsupervised_text_clustering_model/assets/99743248/5ea42501-95c4-4eda-8574-b2e2f81a82dd)


K = 5 was figured out as the optimum number of clusters as the average score is the highest and all the clusters have the same size and clear clusters.


Hence, K-means algorithm on LDA transformed data where number of clusters is 5 is the best algorithm for the text clustering project.

