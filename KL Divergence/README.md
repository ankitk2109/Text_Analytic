# Kullback-Leibler(K-L) Divergence for Text Categorization
### Below task are performed to categorize the text.

Task1. Taking a simple sentences and put these into the program and compute the K-L divergence scores for them, in both directions.

Now creating a third story that is very different to the other two, adding it to the program and measuring how its score changes relative to the first two.

Checking whether the scores make sense and explaining the role epsilon and gamma play in the computation of K-L.

Ans. What is K-L Divergence[1]: The KL divergence tells us how well the probability distribution Q approximates the probability distribution P by calculating the cross-entropy minus the entropy. It measures the similarity (or dissimilarity) between two probability distributions.


![image](https://user-images.githubusercontent.com/26432753/72353306-c0e21080-36db-11ea-8da4-7ba4ba44afdb.png)


![image](https://user-images.githubusercontent.com/26432753/72353341-d5260d80-36db-11ea-98d8-963c2b5e2751.png)


The KL divergence is the measure of inefficiency in using the probability distribution Q to approximate the true probability distribution P.

1.Entropy: The entropy tells us the theoretical minimum average encoding size for events that follow a particular probability distribution.
2.Cross Entropy: Cross entropy between two probability distributions p and q over the same underlying set of events measures the average number of bits needed to identify an event drawn from the set if a coding scheme used for the set is optimized for an estimated probability distribution q, rather than the true distribution p.

![image](https://user-images.githubusercontent.com/26432753/72353393-f0911880-36db-11ea-80fd-606560c0c82c.png)


Below are the two documents upon which the K-L Divergence are calculated.

![image](https://user-images.githubusercontent.com/26432753/72353421-f981ea00-36db-11ea-906d-59cfd86c6029.png)

K-L Divergence score between documents in both direction are shown below:

![image](https://user-images.githubusercontent.com/26432753/72353447-0272bb80-36dc-11ea-9cd5-a3c7dfdebd9d.png)


As both documents have common words between them like down, fell, sun etc due to which their probability distribution is quite similar and thus the K-L divergence score.
The third document which has entirely different context than document 1 and document 2.

![image](https://user-images.githubusercontent.com/26432753/72353468-08689c80-36dc-11ea-87ae-8a3b9ccba149.png)

The K-L Divergence score for d1 with d3 and d2 with d3 is high because the number of common term in third document with other two is extremely low. Due to this the probability distribution is extremely diverge. 

![image](https://user-images.githubusercontent.com/26432753/72353488-10284100-36dc-11ea-9ff1-358c1d20dada.png)

Hyper parameters: 

K-L Divergence has two major problems:

1.K-L Divergence is calculated in both directions due to the asymmetry.

2.Only the common terms among both documents are considered.

Brigette Biggi method suggests back off method, to avoid such drawbacks, Instead of using the common terms, it is necessary to consider the entire vocabulary. So smoothing comes into picture, but with Smoothing, the distribution of probability doesn't sum up-to 1. So, back-off smoothing that keeps the sum of the distribution of probability to 1 and consider the entire vocabulary instead of the common ones.
Example

Epsilon: It is known as the probability of a word, not in a text. To avoid the distance to be infinity, it is set to a small value instead of 0. It is a value less than the probability of a minimum term that appears in either documents.

Gamma: It is defined as a normalization coefficient to account of epsilon, so a probability of a term in a category satisfies the properties of a probability (sum to 1).
