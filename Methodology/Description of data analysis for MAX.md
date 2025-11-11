### Description of the steps for analyzing coded data with the aim of examining correlations with research topics
#### Main goal :
Examining the relationship and correlation between codes extracted from qualitative data (questionnaire related to women's football) and key research topics, including :
- 	Tourism development
- 	Promoting peace
- 	International relations
________________________________________
#### 1. Reading data and initial preparation
Work done :
- 	Reading the Excel file output from MAXQDA software , which includes two columns: Code System (hierarchical codes) and Frequency (repetition of each code) .
- 	Separating the code hierarchy based on / and determining the depth of each code .
Objective : 
#### Prepare the data structure for processing and recognizing semantic structure between codes .
________________________________________
#### 2. Semantic vectorization using SentenceTransformer
#### Work done :
Using the all-MiniLM-L6-v2 model To convert any code (text) into a numerical vector (semantic vector) .
#### Why was this model used? 
This model is one of the simple, fast, and accurate models in the BERT family that is capable of understanding the meaning of sentences and words and is very suitable for semantic analysis .
________________________________________
#### 3. Semantic clustering using KMeans
#### Work done :
Applying the clustering algorithm KMeans On code vectors to identify similar semantic groups .
#### Objective : 
To identify hidden patterns and common semantic structures between different codes .
________________________________________
#### 4. Calculating statistical correlation
For each research topic , the following were calculated :
#### A ) Pearson Correlation
•	Calculating the correlation coefficient between the code vectors and the topic vector, taking into account the Frequency weight.
#### B ) Spearman Correlation
•	Examining rank correlation to measure possible nonlinear relationships .
#### c ) p- value
•	Checking the significance of statistical correlations .
Objective : 
Statistical analysis of the strength and significance of the relationship between each topic and the qualitative codes .
________________________________________
#### 5. Machine learning to model the relationship between topics and codes
The following two models were used to predict the intensity of the relationship :
#### A ) Linear Regression
•	To model the linear relationship between code vectors and the degree of correlation with each topic .
#### b ) Random Forest
•	For more complex, nonlinear modeling that is more robust to noisy data .
#### Evaluation criteria :
- 	R2 ( coefficient of determination )
- 	MSE ( Mean Squared Error )
#### Objective : 
To identify whether machine learning models can predict the relationship between codes and topics .
________________________________________
#### 6. Analysis of results and ranking of correlations
#### Work done :
#### 	Definition of correlation leveling into three levels :
- 	Weak (low) : Correlation coefficient value less than 0.3
- 	Average : between 0.3 and 0.6
- 	Strong (high) : greater than 0.6
#### 	Add a column to describe the level of correlation for each topic .
#### Objective : 
To better understand the extent to which each topic influences the semantic structure of the codes .
________________________________________
## Advantages of the combined method :
#### 1.	More accurate semantic analysis than purely statistical methods .
#### 2.	Generalizable modeling with machine learning .
#### 3.	Multidimensional evaluation including statistical correlation + predictive accuracy of models .
#### 4.	Ability to interpret and present visually for faculty and better reporting .

