# Final Project: Predicting Wine Quality

![wine_image2](https://user-images.githubusercontent.com/85654649/142743285-67f1e617-0ee4-4fcc-b48d-bbdb156a2a68.jpeg)


## Outline of Project

### Team Members
- Danielle Myrick
- Delana Vath
- Jeff Purvis

### Overview of Project
JDD Vineyards, a new business venture, has hired Myrick, Purvis, & Vath Consulting for their "Predicting Wine Quality" project. JDD Vineyards wants the consulting team to determine if their vineyard would produce quality wines, based upon characteristics their wines possess. The consulting team will analyze a dataset with quality scores and use Machine Learning to predict the quality scores JDD Vineyards would produce.

#### Question the data will potentially answer using Machine Learning Technology
Will the wines produced at JDD Vineyards generate high quality scores and be successful?

### Data Source
The data was sourced from Kaggle. The team has included an image of the sample dataset as well as the specific links/files where the data can be obtained. The dataset includes the following attributes:
- fixed acidity
- volatile acidity
- citric acid
- residual sugar
- chlorides
- free sulfur dioxide
- total sulfur dioxide
- density
- pH
- sulphates
- alcohol
- quality score

![data sample screen shot](https://user-images.githubusercontent.com/85654649/142744105-690acf22-5e34-47c4-b336-f64fab2015eb.png)

Raj Parmar. July 2018. Wine Quality, Version 1. [Data file]. Retrieved November 3, 2021 from [Kaggle](https://www.kaggle.com/rajyellow46/wine-quality).

Piyush Agnihotri. September 2020. White Wine Quality, Version 1. [Data file]. Retrieved November 3, 2021 from [Kaggle](https://www.kaggle.com/piyushagni5/white-wine-quality).

UCI Machine Learning. November 2017. Red Wine Quality, Version 2. [Data file]. Retrieved November 3, 2021 from [Kaggle](https://www.kaggle.com/uciml/red-wine-quality-cortez-et-al-2009).

### Google Slides Presentation
This is the [link](https://docs.google.com/presentation/d/1Ak_3XZerrSCkjtl2VdaqQhtaTjbnMLaH8tGpdI0TWM8/edit?usp=sharing) to the current version of the team's Google Slides presentation.

### Tableau Dashboard
This is the [link](https://public.tableau.com/views/Final_Project_16381278221320/Story1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link
) to the current version of the team's Tableau Dashboard.

### Project Flow Chart
This is a draft of the project's initial flow chart, including the mockup of the Machine Learning Model.

![flowchart11-5-21](https://user-images.githubusercontent.com/85654649/140584371-bb98268b-24d8-4aed-962c-efea8a1152ae.png)

### Data Exploration and Analysis
As mentioned above, the consulting team's data was obtained from Kaggle. The initial dataset included over 5,000 different wines that had been tested for their various chemical components (alcohol content, acidity levels, etc.) and a quality score was generated. We took a subset of that dataset to make it more manageable and took two additional files to function as our wine sets to attempt to calculate quality scores, based on the same input values. The team used Pandas and SQL to clean the data and perform the exploratory analysis.

#### Database
PostgreSQL is the database the consulting team used. The database was connected via code contained within the Machine Learning file to AWS. The query schema is included with the GitHub repository. The image below shows the three tables created within the database:

![db_segment2](https://user-images.githubusercontent.com/85654649/142744563-05fc1a94-1cf3-49cb-9838-cc4dfa6a9b6e.png)

This is the ERD for the Database:
![Provisional_DB](https://user-images.githubusercontent.com/85654649/140584483-6d9e690a-5ec0-42c1-a615-2959a8b9c30f.png)

#### Machine Learning
Within the machine learning portion of the code, multiple potential models were considered and attempted prior to ultimately selecting the model that would be used in the final copy of the code. A detailed explanation is listed below:
1. Initial tests included using the LogisticRegression model both with RandomOverSampling and without.  One of the immediate concerns using the LogisticRegression model was a warning message that was generated for both the RandomOverSampling set and regular sampling set.  In both cases, a warning message was generated saying that the solver had reached an iteration limit.  This obviously causes concern because it would not appear as though the full training set is being utilized.  
2. For both of the LogisticRegression models, the resulting accuracy score was deemed unacceptable as the ROS model produced a score of only .25714 and the regular sampling produced .17142, both considered much too low for confidence in the results.  An alternate "solver" was used to see if this had a significant impact (liblinear was used), but the resulting score of .19999 was still deemed unacceptably low.  
3. Three different classifier models were used to see if there would be improved accuracy; specifically, we used BalancedRandomForestClassifier, EasyEnsembleClassifier, and RandomForestClassifier.  While the accuracy scores were significantly improved (.5142857, .342857, .485714 respectively), further consideration of the model brought to our awareness that the "question" we were asking was one of a continuous potential number, not a dichotomous classification.  Therefore, despite the apparently improved accuracy scores, these results were misleading and the models ultimately were determined to be inappropriate.  
4. Since we were looking at a continuous number calculation, we returned to a linear regression model, specifically a multiple linear regression model given the number of factors that we were considering for our calculation. The same training set was loaded into the model, only this time we used the entire dataset, all 5000+ lines.  This model produced an R2 accuracy score of .56121.  Typically, an R2 score of .70 or higher is considered most acceptable, but given the nature of our data, and the sheer number of factors being considered, this was determined to be an acceptable accuracy score.  
5. We took samples of data with known quality scores and ran it through the model to assess the resulting values and predictions and the scores were deemed reasonably close; most were within a .3 to .6 range of variance.  
6. A recommendation had been received to investigate the use of a non-linear regression model.  Unfortunately, a combination of time constraints and lack of familiarity with associated models prevented this option at the time of this project.  However, further investigation of a non-linear regression model is recommended to assess the potential for increased accuracy.  

The code representation of the attempted models can be found in the Machine_Learning_model_tests file:
   
   *  [Machine Code Tests](https://github.com/dcvath/Final_Project/blob/main/Machine_learning_model_tests.ipynb)


An image of the model creation for the applied model is included below:

<img width="1257" alt="linearregressionmodel" src="https://user-images.githubusercontent.com/85654649/143789212-e80a4c1d-c32e-4974-a0b8-706e098c5570.png">


#### Dashboard
The consulting team's interactive elements for the dashboard includes: HTML, JavaScript, and a Tableau Story. The Tableau Story includes two different filters where the quality scores can be filtered by quality rating or wine type (white or red). The [website](https://dmyrick.github.io/Predicting_Wine_Quality/) created for JDD Vineyard showcases the output wine data from the machine learning.

This is an image of one of our dashboards within our Tableau Story.

<img width="598" alt="tableaustoryscreenshot" src="https://user-images.githubusercontent.com/85654649/143789587-bf70788d-989a-432a-bb73-9c5e0fd9f452.png">
