# Methodology
This research adopted a mixed-methods, data-driven approach to investigate the relationship between women’s football, tourism development, and peacebuilding in Iran. The methodology comprised three interconnected stages: 
#### (1) a structured survey for national football players, 
#### (2) an online questionnaire for football experts, academics, and managers, and 
#### (3) semi-structured interviews with football administrators and policy-makers. Each dataset was analyzed separately and then integrated for comparative and complementary insights.
To process and analyze the collected data, three separate Jupyter Notebooks were developed:
- 	Analysis_Footballer_questionnaire.ipynb
- 	online-questions-preprocess.ipynb
- 	interview.ipynb
Below is a detailed, step-by-step account of the methodology — what was done, why it was done, and how.
________________________________________
#### 1-	 Data Collection
#### Why multiple data sources?
To ensure the findings are rich, multidimensional, and grounded in both practice and policy, we gathered data from three distinct, but complementary, respondent groups:
- 	National women footballers (structured questionnaire)
- 	Football experts, managers, and academics (online survey)
- 	Policy-makers and administrators (interview transcripts)
#### Why in this order?
Starting with athletes provided firsthand experiential insights. The online survey extended the scope to decision-makers and experts, while interviews offered policy and administrative perspectives. This sequence ensured that individual, institutional, and systemic views were captured progressively.
________________________________________
#### 2-	 Data Preprocessing and Preparation
####  Tokenization (Interviews)
#### What is this?
Tokenization is the process of breaking text into individual units called tokens (usually words).
#### Why was it necessary?
Interviews were in free-text format. To perform any analysis — from word frequency to topic modeling — the text had to be split into analyzable units.
#### How it was done?
Using Python’s NLTK and transformers libraries to split sentences into words and remove stopwords like “and”, “the”, and “is” which don’t add meaning.
________________________________________
####  Outlier Detection (Interviews)
#### What is this?
Outlier detection identifies data points that differ significantly from others.
#### Why necessary?
Some interview responses were unusually long or short or had extreme sentiment values, which could skew results.
#### How it was done?
Both Z-Score and IQR (Interquartile Range) methods were used to spot outliers.
- 	Z-Score measures how many standard deviations a value is from the mean.
- 	IQR identifies values outside the range between the 25th and 75th percentiles.
________________________________________
#### 	 Feature Encoding (Structured & Online Surveys)
#### What is this?
Converting categorical (text) responses into numerical form.
#### Why?
Machine learning models require numeric inputs.
#### How?
Using Label Encoding and One-Hot Encoding in Python’s pandas and sklearn.
________________________________________
#### 	Scaling
#### What is this?
Adjusting numeric values to a common scale.
#### Why?
To prevent variables with larger scales (like age or years of experience) from dominating those with smaller scales.
#### How?
Using Min-Max Scaling via sklearn.preprocessing.
________________________________________
#### 3-	 Exploratory Data Analysis (EDA)
#### What is this?
Preliminary investigation of data to uncover patterns, spot anomalies, and test assumptions.
#### Why?
To check data distributions, correlations, and variable interactions before modeling.
#### How?
Using Python libraries: matplotlib, seaborn, pandas-profiling.
________________________________________
#### 4-	 Statistical & Machine Learning Models
Models Used:
- 	Logistic Regression (baseline model for binary classification)
- 	Naive Bayes (for small sample sizes and categorical data)
- 	Support Vector Machine (SVM) (handles high-dimensional data well)
- 	Random Forest (captures non-linear relationships and ranks feature importance)
#### Why these?
They complement each other — combining interpretability, robustness, and predictive strength. Referencing (de Menezes et al., 2017; Nishanth & Ravi, 2016; Muriira et al., 2018; Zhou et al., 2023)
#### How?
- 	Train-test split (70:30)
- 	Hyperparameter tuning via Grid Search
- 	Model evaluation using accuracy, precision, recall, F1-score, and 5-fold cross-validation
________________________________________
#### 5-	 Semantic Similarity Analysis (Interviews)
#### What is this?
Measuring how similar two pieces of text are in meaning.
#### Why?
To group similar interview responses and identify dominant discussion topics.
#### How?
Using paraphrase-MiniLM-L6-v2 and all-MiniLM-L6-v2 pre-trained transformer models from HuggingFace, combined with pytorch and sentence-transformers.
________________________________________
#### 6-	 Clustering (Interviews)
#### What is this?
Grouping similar responses into clusters.
#### Why?
To detect thematic patterns and dominant opinions.
#### How?
Using KMeans clustering (n=5 determined via elbow method).
________________________________________
#### 7-	 Dimensionality Reduction
#### What is this?
Simplifying complex, multi-dimensional data for visualization.
#### Why?
To visualize relationships between clusters.
#### How?
Using t-SNE (t-distributed Stochastic Neighbor Embedding)
________________________________________
#### 8-	 Correlation Analysis
#### What is this?
Measuring strength and direction of relationships between variables.
#### Why?
To identify factors most associated with peacebuilding and tourism development outcomes.
#### How?
Using Pearson’s r for numeric variables and Chi-square test for categorical variables.
________________________________________
#### 9-	 Result Integration and Triangulation
#### What is this?
Comparing findings from the three datasets.
#### Why?
To confirm, explain, and complement results for more robust conclusions.
#### How?
Cross-referencing model outputs, cluster themes, and statistical significance results.
________________________________________
#### Conclusion
This methodology combined quantitative and qualitative data analytics, with advanced NLP and machine learning tools, specifically designed to explore the socio-cultural, diplomatic, and economic implications of women’s football in Iran.
By explicitly linking each step to its purpose and integrating complementary techniques, the process ensures scientific rigor, interpretability, and replicability.
________________________________________

#### 	Methodology for Combining Results from Three Questionnaires
In this stage of the study, the objective was to synthesize the findings from three different datasets — one from national women footballers, one from expert interviews, and one from online stakeholders. Combining these diverse data sources was essential for producing a comprehensive and balanced picture of the role of women’s football in tourism and peacebuilding.
#### The analysis was conducted through the following steps
#### 1-	Normalization :
The MinMaxScaler from sklearn.preprocessing  library of python was selected to normalize the importance scores from different datasets to a unified scale (0 to 1).
#### Why normalization?
Because the scores from each source were on different scales — some were feature importances, others were Pearson correlations — and to compare or combine them fairly, they needed to be rescaled
#### 2-	Adding a Source Column :
By adding a 'Source' column, we could later trace each feature's origin. This is useful for identifying whether a feature was emphasized more by players, experts, or online stakeholders.
#### 3-	Combining the Data:
This concatenates the three datasets into one, stacking them vertically while preserving the source information. It allows for comparative and combined analyses of all features across sources
#### 4-	Normalizing the Scores:
To ensure fair comparison between different types of scores (some ranging from -1 to 1, others from 0 to 100), we scaled all scores to a common 0–1 range.
#### 5-	Aggregating and Ranking Features:
This groups scores by feature, calculates their average importance score across all sources, and sorts them in descending order.
#### Why averaging?
Because taking the mean balances out biases from individual sources and highlights consistently important features.


### 	Why This Method Was Important

    Integrates Multiple Perspectives:
    Combining players' insights,expert opinions, and public perceptions ensures the analysis is multidimensional and inclusive.

    Balances Different Scales and Metrics: 
    Normalization resolves inconsistencies in measurement units and scoring systems.

    Supports Evidence-Based Decision-Making: 
    By ranking features across all data, decision-makers can focus on the factors with consistent, high importance.

    Provides Traceability: 
    The 'Source' column allows backtracking results to their origin for more detailed interpretation.


#### Challenge	Solution
- Different score ranges across datasets	Applied MinMax normalization to unify scales
- Inconsistent variable names	Standardized column names
- Merging diverse data sources	Used concatenation with clear source labeling
- Combining subjective (interview) and statistical (survey) results	Used normalization and averaged importance scores

	
	
	
	
	



