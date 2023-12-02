# Data-Mining-326

### Group Members:

**Leader:** Sara  Alzayed | 443203107

Haya Albaker  |  443202868

Sarah Alsaleh  |  443201066

Marya Asaad  |  443200794

-------------------------------------------------------------------------

## Introduction: 
Our study intends to determine the high rate of depression and anxiety among college students, given their notable negative impact on social interactions and academic performance. Physical and mental exhaustion are common signs of anxiety and depression, but these symptoms are usually minor and may go unrecognized, leaving sufferers unaware of their increasing control over their thoughts and feelings. This misinformation raises the possibility of unintentionally delaying crucial therapy, which raises the risk of engaging in risky behaviors like substance abuse.

Students who struggle with depression and anxiety have psychological difficulties related to their academic work, their studies, and their interactions with peers and professors. Both social conduct and academic performance may suffer as a result of these difficulties. 

## Goals: 
To address these issues, our project aims to explore trends, patterns, and factors to predict the likelihood and severity of depression among university students. Our dataset includes information on school year, depressiveness, anxiousness, and sleepiness, offering valuable insights. Students who struggle with depression and anxiety have psychological difficulties related to their academic work, their studies, and their interactions with peers and professors. Both social conduct and academic performance may suffer as a result of these difficulties. 

-------------------------------------------------------------------------

## Summary

### Initial Actions:
1. Describe the task of data mining.
2. Examine and read the dataset.                   
3. Preserve the original dataset
4. Explain the properties and dataset.
5. Display a dataset sample.

### Missing values:
The codes in this section are designed to help you find the missing values in the dataset. Our analysis shows that several attributes in our dataset do, in fact, contain missing values or NULLS.

### Central tendency measures:
In order to understand the distribution and central values of the important variables in our dataset, we used measures of central tendency in this section. We tried to determine the typical or central value that our data points typically cluster around by using metrics like mean, median, and mode. These metrics help identify patterns and tendencies by offering insightful details about the main trends found in our dataset.

### Graph visualization:

### Concept hierarchy generation for nominal data:

### Encoding categorical data  
We encoded categorical values, including those within columns with character types, and simultaneously removed irrelevant attributes like **student id**. This approach aligns with the optimization of machine learning algorithms, as they are typically designed to operate more efficiently with factors data rather than character data. Additionally, this encoding enhances the overall performance and interpretability of the data.

### Feature selection and dimensionality reduction:

### Finding and removing outliers:

### Discretization: 

### Normalization:

## Clustering:
##### Main points:
- K-means algorithm-based unsupervised learning techniques were utilized.
- Removed the class label from the dataset as clustering is an unsupervised learning process.
- A variety of data types were taken into consideration including:
    - Age
    - Gender
    - BMI
    - WHO BMI
    - PHQ score
    - depression severity
    - diagnosis and treatment of depression
    - GAD score
    - Anxiety severity
    - Anxiousness
    - diagnosis and treatment of anxiety
    - Empworth score
    - sleepiness.
- Categorical values were encoded, and unnecessary characteristics like _student IDs_ were deleted.
  
**Continually:**

- Realigned objects and recalculated cluster centers until convergence.
- K=5 was found to be the ideal number of clusters using the **elbow method**.
- Close, overlapping clusters were seen when experimenting with various cluster sizes (k=5, k=4, k=3), indicating similarities between the data objects.
- Across all k values (5, 4, 3), silhouette coefficient values were typically small, and in some cases even negative.
- Analysis of average precision and recall showed that as the number of clusters dropped, recall increased and precision decreased.

Based on an evaluation that compared the clustering outcomes to the actual results, **k=4** was found to have the lowest difference, indicating that it was a better option.

## Classification:
##### Main points:
- Made use of supervised learning strategies with a **decision tree algorithm** as the main focus.
- Objective: Predict the depression class label using two options: _TRUE_ or _FALSE_.
- A variety of data types were taken into consideration including:
    - Age
    - Gender
    - BMI
    - WHO BMI
    - PHQ score
    - depression severity
    - diagnosis and treatment of depression
    - GAD score
    - Anxiety severity
    - Anxiousness
    - diagnosis and treatment of anxiety
    - Empworth score
    - sleepiness.

Split the dataset into: 
- Training and Testing sets with _three_ distinct sizes (10, 7, and 5) using the **Cross-validation method**.
- Created _nine_ trees by applying the three attribute selection techniques:
1. Gain ratio
2. Gini index
3. Information gain

With an accuracy of 90.95%, the **third tree with k=5** and a gain ratio was found to be the most successful model. We also emphasized how this model correctly classified the majority of tuples.
