# Clustering (interviews)
## What is this?
### Clustering is an unsupervised machine learning technique used to group similar data points (in this case, interview responses) into distinct categories or "clusters" based on how similar their content is .


## Why?
Because qualitative interview data often contains a variety of themes and ideas expressed in natural language
### By clustering the responses :
- 	We can recognize thought patterns.
- 	Identify dominant or recurring themes
- 	Understand what ideas are commonly associated with women's football tourism and peacebuilding from the perspective of stakeholders .
#### This is a method for transforming subjective, open-ended interview data into structured interpretable insights .


## How?
We use clustering Kmeans. We used clustering, which is a partitioning method in which the data set is divided into a predetermined number of clusters - n clusters - are divided so that the responses within a cluster are as similar as possible and the responses in different clusters are as different as possible .


## Why was n=5 chosen?
The value of  n (the number of clusters) is not random .
determined the best number of clusters using the Elbow method .
### Elbow method  ?
 It is a technique for finding the optimal number of clusters using the following .
#### 1.	Running the clustering algorithm for a range of n values (such as 1 to 10)
#### 2.	Calculate the within-cluster sum of squares (WCSS) for each n
#### 3.	Plot these WCSS values against the number of clusters.
#### 4.	Finding the "elbow" point on the graph - the value at which the WCSS reduction becomes marginal
(i.e. adding more clusters does not reduce the error much)

### In this analysis,  n=5 was obtained 
This means:
 ####  When   n=5 , the clusters were compact enough to have low WCSS .  And at the same time, they avoided excessive fragmentation . Increasing more than  five results in minor improvements but adds unnecessary complexity .

#### Benefits of choosing 
#### n=5
 -  Striking a balance between accurate classification and interpretability
 -  Avoid over-clustering (too many small, similar clusters)
 -  Matching natural thematic patterns from interview data
 -  Maintain a manageable number of topics to discuss in the article

The goal was to see which concepts and keywords in the fields of women, football tourism, and peace the interview participants talked about the most, and in what areas there was common ground .

The numbers you see in this section (e.g. 0.123 or 0.283) are the result of a semantic similarity analysis between the interviewees' text responses and the predefined keywords . This analysis was performed using the paraphrase-MiniLM-L6-v2 model . which is a powerful model in measuring the semantic similarity of sentences .

## Why the numbers? 
#### The numbers are obtained from the output of the semantic similarity analysis between the interviewees' sentences and these words in the embedding vectors model .

#### 1.	Tourism Development and Destination Management
The average semantic similarity for the words Tourism (0.123) , Tourism Development (0.186) , and Destination Management (0.183) means that in the interviewees' responses, these words were repeatedly seen directly or indirectly with related content and had a high semantic consistency with the interview text .
#### 2.	Peacebuilding and Social Cohesion
The high lexical similarity for Peacebuilding (0.252) , Peace (0.159) , and Improving relationships (0.192) means that participants consider football a suitable platform for improving social relations and reducing cultural tensions .

#### 3.	Gender Equality and Empowerment
High scores for Gender Equality (0.283) , Improving attitudes (0.280) , and Women's Empowerment (0.320) indicate that participants believe football is an effective tool for changing attitudes towards women .

#### 4.	Sports Diplomacy

Sports Diplomacy (0.345) and Encouraging sports diplomacy (0.352) had the highest similarities in the entire analysis, indicating that sport, especially women's football, is seen as an effective channel for diplomatic communication in a context where political relations are limited .         

#### 5.	Cultural Exchange and Tourism Impact
Promoting cultural exchange ( 0.223 ) , Cultural Exchange ( 0.224) , and Providing opportunities to interact (0.380) show Gives Football Women Hospitalization Suitable For Interactions Interculturality and Reduction Misunderstandings Regional It is .



#### These five issues collectively show that women's football in Iran is more than just a sport, it is a strategic platform for tourism, peace diplomacy, women's empowerment, and cultural communication .

