## Dataset Description

### Goal:

Our main goal in collecting “Depression and anxiety” dataset is to learn more about the number of college students facing difficulties that end them up in having particular disorders , in our case depression and anxiety . We gather information about their school year, depressiveness, anxiousness, and Sleepiness. This kind of data will help collages make generally better decisions about their academic plans to what is more suitable for the students ,and also  help the student affairs deanery improve its services or even add more to fulfill what a college student needs. It could also help mental health hospitals in knowing the importance of how to raise awareness in college students about their mental health sanity which could decrease the risk of college students developing depression/anxiety.


### Here are two specific goals we have for this dataset:

**1. Classification Goal:**

We want to group students into different categories based on their PHQ Score, GAD Score, and EPWORTH Score. By doing this, we can see patterns and trends among different groups. This will help us understand if these specific scores have to do with students developing depression/anxiety. With this information, we can develop strategies that could help ensure lower the risks of developing depression/anxiety.


**2. Defect Prediction Goal:**

We want to use statistical techniques to seek trends that can predict any early symptoms of depression/anxiety. This could include things like, depressiveness, anxiousness, or Sleepiness.  By catching these problems early, we can fix them and make sure students get help and achieve guidance toward the right path. This analysis will help  make students mental health more “considerable”.


## Dataset Details:

**Source of the dataset:** Kaggle

**Dataset Link:** https://www.kaggle.com/datasets/shahzadahmad0402/depression-and-anxiety-data?resource=download

**Number of Attributes:** 19

**Number of Objects:** 783

### Table 1:

| **Attribute Name**  | **Description**             | **Data Type**       | **Possible Values**                               |
|---------------------|-----------------------------|---------------------|----------------------------------------------------|
|ID                   |student id                   |Nominal              |3 values                                            |
|school_year          |student current year         |Numeric              |1-4                                                 |
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



