<<<<<<< HEAD
# woman-s_football
Role of women's football in peace through mega sport events and associated tourism using by data science and machine learning
==============
# Women\'s Football

This project have  3 questionnaries:
 - Footballers questionnary
 - Interview
 - Online questionnary


## <font color='darkred'> Footballers: </font>
 This questionnare have two part: 
   - General quetions
   - Specialized questions
   **General** question are multiple choice and 
   **Specialized** questions, while being multiple choice are also related and they must be ranked
- [x] create dataset for *general* questions and named group A
- [x] create dataet for *specialized* questions and named group B
- [x] combine two groups 
- for group A if option is **yes** rank=1 and for other rank=0 
- [x] define topics for each options by **Scientific Experts of this filed**
- [x] preprocess
- prepare the data for analysis
- Convert text columns  to numeric data
- Mapping questions , options and topics
- [x] Calculate the *__Pearson__ correlation coefficient*
- [x] Calculate the *__Chi2-square__  test for categorical data*
- [x] Interpretation of results
- [x] **Machine Learning Models**
- Split data to train and test
- learning data and fit models
- calculate scors to each models
- evaluate models to infer the best model
- extract features based on best  model 






## <font color='purple'> Interview: </font>
- [x] create code system file with MAXQDA 
- [x] create excel file hierarchy based 
- Hierarchies are separated by "/" 
- [x] Hierarchical processing and  Calculate shares
- [x] Statistical analysis and Detecting outliers with combiniation method
- Tokenize codes
- Statistical Methods: Z-Score and IQR
- Identifying outliers with DBSCAN
- Combine the results of the outliers
- Remove outlier codes
- Save clean data
- [x] Identifying the codes that are most relevant to the topics in the topic table
- Semantic Vector Modeling
- Vectorization of codes and topics
- Calculating semantic similarity
- Create a results table
- [x] Identify Common Code Groups
- Separation of codes and frequencies
- Vectorizing codes using language models
- Calculating similarity between codes
- Code clustering using K-Means
- Dimensionality reduction for cluster visualization
- [x] Correlation analysis
- Extract and clean codes
- Using SentenceTransformer to convert codes into numeric vectors:
 - all-MiniLM-L6-v2
- Clustering using KMeans
- Calculating Pearson and Spearman correlation
- Correlation assessment




## <font color='darkcyan'> Online questons: </font>
- [x] create dataset
- translate to english version in excel file
- each column name is question title 
- save to file
###
- [x] preprocess
- Clean and rename columns
- for agree and disagree : *Map ratings to numeric values*
- for categorical text : *Handle and Encode categorical columns with Label Encoding*
- create columns related to these categories
- for log text : *Handle text columns with TF-IDF Vectorization*
- create columns related to log text vectorization
- Handle missing values
- Calculate Correlation
- save to file 
###
- [x] Analysis
- [x] tourism:
- Combine tourism-related columns to create a target
- encode categorical features
- Standardize numerical features
- Split data to train and test
- learning data and fit models
- calculate scors to each models
- evaluate models to infer the best model
- extract features based on best  model 
- [x] Peace:
- Combine Peace-related columns to create a target
- encode categorical features
- Standardize numerical features
- Split data to train and test
- learning data and fit models
- calculate scors to each models
- evaluate models to infer the best model
- extract features based on best  model 
- [x] Media:
- Combine Media-related columns to create a target
- encode categorical features
- Standardize numerical features
- Split data to train and test
- learning data and fit models
- calculate scors to each models
- evaluate models to infer the best model
- extract features based on best  model 
- [x] Challenges:
- Combine Challenges-related columns to create a target
- encode categorical features
- Standardize numerical features
- Split data to train and test
- learning data and fit models
- calculate scors to each models
- evaluate models to infer the best model
- extract features based on best  model 

##

## <font color='darkpink'> Combining and analyzing model features: </font>
 A final review has been conducted on four topics, which are:
### **Tourism** , **Peace** , **Media** , **Challenges**
- [x]  *For each topic, the following steps have been taken to combine and analyze the topics more accurately:*
####
- Load the datasets
- Standardizing column names for consistency
- Combine all data into a single dataframe
- Normalizing the scores to a scale of 0 to 1
- Grouping by feature and calculating the mean normalized score across sources
 
>>>>>>> e5ec577 (Initial commit)
