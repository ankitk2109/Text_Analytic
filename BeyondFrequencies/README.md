# Objective

**Following tasks are performed which includes Preprocessing Tweets, calculating TF score, TF-IDF, PMI score and determining entropy of tweets to classify them as spam or non-spam.

Task1. Find 10 short text-items (20-30 words); they could be emails, short docs, tweets or whatever. Make sure they all deal with some common topic of interest; so they have some of the same words.
a.Remove the standard stopwords from them using some standard list, use nltk.

Ans: Following steps are followed to pre-process the data.
TweetTokenizer(Tokenize the tweets) -> Stop word removal -> Removal of special characters -> Changing words to lower case -> Blank space removal -> Applying WordNetLemmatizer -> Joined elements of multiple list to a single List
After applying the above steps on tweets below is the produced clean corpus.

![image](https://user-images.githubusercontent.com/26432753/72295318-3eac0a80-364f-11ea-83dc-cfc3c060686a.png)

Fig: Preprocessed Tweets

b.Compute the TF scores for all the remaining words in the texts and use R to show the word-cloud for these words. In your answer provide the matix of TF scores and the word-cloud image.

Ans:Term frequency: Measures how frequently a term occurs in a document.
TF(t) = (Number of times term t appears in a document) / (Total number of terms in the document)
To create a word-cloud in python we need CountVectorizer inside the package called as sklearn.feature_extraction.text. 
Created an object of CountVectorizer as cnt_vec. 
Performed cnt_vec.fit_transform(corpus). The fit_transform method calculates the frequency of each word in the entire sets of docs.
Now to represent calculated frequency in a table we use Dataframe. Below is the snapshot of the frequency table.

![image](https://user-images.githubusercontent.com/26432753/72295903-60f25800-3650-11ea-8dda-afa3948506d6.png)

Fig:Snapshot of Frequency table produced after applying TF-score

Below is the word cloud that is produced based on the tweets corpus.

![image](https://user-images.githubusercontent.com/26432753/72295939-736c9180-3650-11ea-8f7e-781da6949c33.png)

Fig: Word Cloud based on Tweets

c.Now, compute the TF-IDF scores for all the same words in the texts. Construct a set of words that represents the TF-IDF scores you have found, for all the words. Use R to show a word-cloud for these words. Also, provide the matrix of TF-IDF scores and the word-cloud image.

Ans: Inverse document frequency(IDF): The specificity of a term can be quantified as an inverse function of the number of documents in which it occurs. Actually it measures how important a term is.
The Formula is defined as: IDF(t) = log_e(Total number of documents / Number of documents with term t in it).
TF-IDF is calculated using

To calculate tf-idf in python we need a module TfidfTransformer inside package sklearn.feature_extraction.text
fit_transform() method of TfidfTransformer is used to calculate the TF-score from pre-processed data.
In the matrix below, left side shows the number of documents and the top column shows the words occuring in each document.

![image](https://user-images.githubusercontent.com/26432753/72295976-854e3480-3650-11ea-9101-1d9781f81a27.png)

Fig: TF-IDF Matrix

Before creating the word cloud, summation of tf-idf of each columns i.e words are calculated and a dictionary is created. Below is the snippet of the dictionary and tf-idf summation .

![image](https://user-images.githubusercontent.com/26432753/72296086-baf31d80-3650-11ea-8052-94ebdaac4b62.png)

![image](https://user-images.githubusercontent.com/26432753/72296107-c9d9d000-3650-11ea-98ae-6228437b1dcd.png)

Below is the word-cloud out of all words

![image](https://user-images.githubusercontent.com/26432753/72296145-db22dc80-3650-11ea-8d1a-93e1cd1afc73.png)

Fig: Word cloud based on TF_IDF-Score

Task2. Using Python or R, compute the PMI scores for all adjacent pairs of words in your 10-doc corpus (ie the texts after stop-word removal).
List the top-10 pairs based on the PMI scores found for the pairs.
Do the results make sense? If not, then introduce a minimal cut-off frequency and re-compute the top-10 until they seem sensible.

Ans: Pointwise Mutual Information (PMI) : The main intuition is that it measures how much more likely the words co-occur than if they were independent. formula is given by:

![image](https://user-images.githubusercontent.com/26432753/72296165-e970f880-3650-11ea-9a2d-0ec7494e3a67.png)

Module required to calculate the PMI in python is nltk.collocations.BigramAssocMeasures()
Corpus of 10 documents id tokenized and bigrams are found using BigramCollocationFinder.
The score is produced using bigram_measures.pmi.
Below is the snippet of bigram with pmi score:

![image](https://user-images.githubusercontent.com/26432753/72296195-f988d800-3650-11ea-8d96-c36dbc2a78e3.png)

Top 10 pairs based on PMI score:

![image](https://user-images.githubusercontent.com/26432753/72296235-0d343e80-3651-11ea-83c9-e9c05a9c2fc5.png)

Looking at the result it can be seen that it doesn’t make much sense. The issue with PMI is that it over-estimates the low frequency events because of how it treats counts.
We can set a frequency filter to narrow down our result. To do so I have used apply_freq_filter(). Below is the output after applying frequency filter=2.

![image](https://user-images.githubusercontent.com/26432753/72296257-19200080-3651-11ea-9673-4d5eb3bf4fa0.png)

Task3.Entropy has been used to determine whether tweet set is interesting (contains variety) or repetitive
(spam). Create two sets of 10 made-up tweets:
a.spam-set: where the 10 tweets are very similar containing an advert for a product. 
b.b. random-set: where the 10 tweets are very different, chosen at random from Twitter. Now, find a Python/R program or package that computes entropy and find the entropy values for (i)
spam-set, (ii) random-set, (iii) the two sets combined. Report the program you used and its source, the tweet data and the entropy values found.

Ans: Two sets are created, 
Twitter Spam set:

![image](https://user-images.githubusercontent.com/26432753/72296284-2a690d00-3651-11ea-8b8f-bae7856dc1d9.png)


Random Set:

![image](https://user-images.githubusercontent.com/26432753/72296325-3c4ab000-3651-11ea-9d33-38ce92e8a6f3.png)


Entropy is defined as the sum of the probability of each label times the log probability of that same label, written as H(A) = -sum(p * log(p), axis=0). It is randomness in words.
FreqDist calculates the frequency distribution for each token and prob generates the probability of each token and entropy is returned(-sum(p*log(p with base 2))) for every probability [1]
Below is the function to calculate the entropy.

![image](https://user-images.githubusercontent.com/26432753/72296356-49679f00-3651-11ea-8432-9f72a83b3a24.png)

i.Entropy is calculated for the spam set is shown below:

![image](https://user-images.githubusercontent.com/26432753/72296401-600df600-3651-11ea-99af-db6415db84bd.png)

ii.Entropy is calculated for the random set is shown below:

![image](https://user-images.githubusercontent.com/26432753/72296406-669c6d80-3651-11ea-9ffd-36313f549da6.png)

iii.Combined entropy is shown below:

![image](https://user-images.githubusercontent.com/26432753/72296424-6e5c1200-3651-11ea-90e8-d52bc9fc65eb.png)
