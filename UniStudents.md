## Dataset Description

### Goal:

Our main goal in collecting “Depression and anxiety” dataset is to learn more about the number of college students facing difficulties that end them up in having particular disorders , in our case depression and anxiety . We gather information about their school year, depressiveness, anxiousness, and Sleepiness. This kind of data will help collages make generally better decisions about their academic plans to what is more suitable for the students ,and also  help the student affairs deanery improve its services or even add more to fulfill what a college student needs. It could also help mental health hospitals in knowing the importance of how to raise awareness in college students about their mental health sanity which could decrease the risk of college students developing depression/anxiety.


### Here are three specific goals we have for this dataset:

**1. Classification Goal:**

We want to group students into different categories based on their PHQ Score, GAD Score, and EPWORTH Score. By doing this, we can see patterns and trends among different groups. This will help us understand if these specific scores have to do with students developing depression/anxiety. With this information, we can develop strategies that could help ensure lower the risks of developing depression/anxiety.


**2. Defect Prediction Goal:**

We want to use statistical techniques to seek trends that can predict any early symptoms of depression/anxiety. This could include things like, depressiveness, anxiousness, or Sleepiness.  By catching these problems early, we can fix them and make sure students get help and achieve guidance toward the right path. This analysis will help  make students mental health more “considerable”.

**3. Clustering Goal:**

We're clustering students together based on their similarities to create distinct clusters. Various methods will be utilized to determine the number of clusters that best suit our dataset, followed by evaluation techniques to assess the effectiveness of these clusters in segmenting the data effectively based on their inherent features.


## Dataset Details:

**Source of the dataset:** Kaggle

**Dataset Link:** https://www.kaggle.com/datasets/shahzadahmad0402/depression-and-anxiety-data?resource=download

**Number of Attributes:** 19

**Number of Objects:** 783

### Table :

| **Attribute Name**  | **Description**             | **Data Type**       | **Possible Values**                               |
|---------------------|-----------------------------|---------------------|----------------------------------------------------|
|ID                   |student id                   |Nominal              |3 values                                            |
|school_year          |student current year         |Ordinal              |1-4                                                 |
|Age                  |student age                  |Numeric              |18-24                                               |
|Gender               |student gender               |Binary               |female/male                                         |
|BMI                  |body mass index              |Numerical            |9-50                                                |
|who_bmi              |bmi classification           |Nominal              |Underweight/Normal/Overweight/Obese                 |
|PHQ Score            |Patient Health Questionnaire |Ordinal              |0-27                                                |
|depression_severity  |severity of depression       |Nominal              |Mild/Moderate/Moderately Severe/Severe/None-Minimal |
|depressiveness       |depressiveness               |Binary               |TRUE/FALSE                                          |
|Suicidal             |likely to commit suicide     |Binary               |TRUE/FALSE                                          |  
|depression_diagnosis |depression diagnosis         |Binary               |TRUE/FALSE                                          |
|depression_treatment |treating depression          |Binary               |TRUE/FALSE                                          |
|GAD Score            |Generalized Anxiety Disorder |Ordinal              |0-<15                                               |
|anxiety_severity     |severity of anxiety          |Nominal              |Mild/Moderate/Moderately Severe/Severe/None-Minimal |
|anxiousness          |anxiousness                  |Binary               |TRUE/FALSE                                          |
|anxiety_diagnosis    |anxiety diagnosis            |Binary               |TRUE/FALSE                                          |
|anxiety_treatment    |treating of anxiety          |Binary               |TRUE/FALSE                                          |
|EPWORTH Score        |The Epworth Sleepiness Scale |ordinal              |0-15                                                |
|Sleepiness           |state of being sleepy        |Binary               |TRUE/FALSE                                          |


### findings: 

We employed both supervised and unsupervised learning techniques for our data analysis, specifically focusing on classification and clustering. as we mentioned before, our dataset represents the collage students' data to predict the probability of a university student to develop depressiveness in order to make people have the proper preventive measures that help them to make their lives better. Therefore ,we applied the data mining tasks which are classification and clustering. In the realm of classification, we utilized a decision tree algorithm, which is a recursive method that generates a tree structure with leaf nodes representing final decisions. Our model's primary task was to predict the class label for (depressiveness), with two possible categories: TRUE and FALSE. This prediction is made on the rest attributes , including age, gender, BMI, WHO BMI, PHQ score, depression severity, suicidal, depression diagnosis, depression treatment, GAD score, anxiety severity, anxiousness, anxiety diagnosis, anxiety treatment, Empworth score, and sleepiness. In order to split our dataset into two distinct sets: the Training set and the Testing set. we used the Cross validation method and tried 3 different sizes (10,7,5) and applied 3 attribute selection method for each size (gain ratio, gini index, information gain) which results in 9 trees. First tree, resulting from k=5 and information gain, accuracy=89.42% Second tree, resulting from k=5 and gini index, accuracy=90.85% Third tree, resulting from k=5 and Gain ratio, accuracy=90.95% Fourth tree, resulting from k=7 and information gain, accuracy=88.91% Fifth tree, resulting from k=7 and gini index, accuracy=88.11% Sixth tree, resulting from k=7 and gain ratio, accuracy=89.47% Seventh tree, resulting from k=10 and information gain, accuracy=88.59% eighth tree, resulting from k=10 and gini index, accuracy=86.04% Ninth tree, resulting from k=10 and gain ratio, accuracy=87.37% After calculating the average accuracy for each tree, we found that the third model has the best accuracy which means that most tuples were correctly classified. In the case of clustering, as it is unsupervised learning, we did not use a class label for implementing the cluster. We removed the class label attribute "depressiveness" and used all other attributes in clustering (age, gender, BMI, who_bmo, PHQ score, depression_severity, suicidal, depression_diagnosis, depression_treatment, GAD Score, anxiety_severity, anxiousness, anxiety_diagnosis, anxiety_treatment, EPWORTH Score, and sleepiness), all of which are different data types. We implemented the K-mean algorithm for clustering, which produces K clusters, with each cluster represented by the center point and each object assigned to the nearest cluster. We iteratively recalculated the center and reassigned objects until the center point of each cluster did not change. To implement the clustering technique, We encoded the categorical values we want to use in clustering into numerical values, and removed the attributes that are irrelevant like student id. then we defined functions to calculate the average BCubed precision and recall. we used the elbow method to determine the optimal number of clusters, which gave us a result of k=5. we will experiment clustering with k=5, k=4 ,k=3. From the cluster plot we see that in k=5,4,3 clusters are close and overlapping (there are a lot of similarities between the data objects) The silhouette coefficient measured between all data are very small and some are even negative in all k=5,4,3. The average precision and recall found show that As the number of clusters decrease the precision decreases and recall increases . We also calculated the difference between the actual results and our clustering results ,k=3 had a higher difference than k=4. And k=5 had a higher difference than k=3 . k=4 had the lowest difference thus is a better option than the other models. At the end, we evaluated our models by measuring the average accuracy to choose the most effective model .
