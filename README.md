# Final Project: Predicting Wine Quality

![wine_image2](https://user-images.githubusercontent.com/85654649/142743285-67f1e617-0ee4-4fcc-b48d-bbdb156a2a68.jpeg)


## Outline of Project

### Team Members
- Danielle Myrick
- Delana Vath
- Jeff Purvis

### Overview of Project
JDD Vineyards, a new business venture, has hired Myrick, Purvis, & Vath Consulting for their "Predicting Wine Quality" project. JDD Vineyards wants the consulting team to determine if their vineyard would produce quality wines, based upon characteristics their wines possess. The consulting team will analyze a dataset with quality scores and use Machine Learning to predict the quality scores JDD Vineyards would receive.

#### Question the data will potentially answer using Machine Learning Technology
Will the wines produced at JDD Vineyards generate high quality scores and be successful?

### Data Source
The data was sourced from Kaggle. The team has included a screen shot of the sample dataset as well as the specific links/files where the data can be obtained. The dataset includes the following attributes:
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

Raj Parmar. July 2018. Wine Quality, Version 1. [Data file]. Retrieved November 3, 2021 from https://www.kaggle.com/rajyellow46/wine-quality.
Piyush Agnihotri. September 2020. White Wine Quality, Version 1. [Data file]. Retrieved November 3, 2021 from https://www.kaggle.com/piyushagni5/white-wine-quality.
UCI Machine Learning. November 2017. Red Wine Quality, Version 2. [Data file]. Retrieved
November 3, 2021 from https://www.kaggle.com/uciml/red-wine-quality-cortez-et-al-2009.

### Google Slides Presentation
This is the link to the current verision of the team's Google Slides presentation:
https://docs.google.com/presentation/d/1_syazsfrAmDTk7VxIcM2oDEMwXvgvpArfBdHkG1Xalw/edit?usp=sharing

### Tableau Dashboard
This is the link to the current verision of the team's Tableau Dashboard:
https://public.tableau.com/views/Final_Project_16381278221320/Story1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link

### Project Flow Chart
This is a draft of our project's initial flow chart, including the mock up of our Machine Learning Model.

![flowchart11-5-21](https://user-images.githubusercontent.com/85654649/140584371-bb98268b-24d8-4aed-962c-efea8a1152ae.png)

### Data Exploration and Analysis
As mentioned above, our data was initially obtained from the Kaggle website. The initial dataset included over 5,000 different wines that had been tested for their various chemical components (alcohol content, acidity levels, etc.) and a quality score was generated. We took a subset of that dataset to make it more manageable and took two additional files to function as our wine sets to attempt to calculate quality scores, based on the same input values. The team used Pandas and SQL to clean the data and perform the exploratory analysis.

#### Database
PostgreSQL is the database the team used, and the database will be connected via code contained within the Maching Learning ipynb file. The query schema is included with the Github repository. The screen show below shows the three tables created within the database:

![db_segment2](https://user-images.githubusercontent.com/85654649/142744563-05fc1a94-1cf3-49cb-9838-cc4dfa6a9b6e.png)

This is the ERD for the Database:
![Provisional_DB](https://user-images.githubusercontent.com/85654649/140584483-6d9e690a-5ec0-42c1-a615-2959a8b9c30f.png)

#### Machine Learning
Within our Machine Learning code, multiple potential models were attempted in order to identify the one that would be most fitting with this dataset. In our last submission, we thought that RandomForestClassifier was the best suited, but upon further review of the resulting data, this was discovered to be in error. The classifier model was not calculating predicted quailty scores correctly. Further testing of various training models was completed and Multiple Linear Regression was determined to produce the highest results.

To accomplish this, we established the features to be used in the Multiple Linear Regression model and trained the model using the uploaded training dataset. The team used trained model on new datasets to calculate predicted quality scores, and created a wine_id for each of the tested wines in order to identify each unique entry for analysis.

A screen shot of the model creation is included below:

<img width="1257" alt="linearregressionmodel" src="https://user-images.githubusercontent.com/85654649/143789212-e80a4c1d-c32e-4974-a0b8-706e098c5570.png">

#### Dashboard
For our dashboard, we built a webpage using HTML and JavaScript, and we plan to embed some visualization from Tableau, in addition to our interactive element. We're looking at a few options for the interactive element, but we believe the our final interactive element will allow the user to select a wine_ID, and the page will display that specific wine_ID's quality score and chemical components.  

This is a screen shot of our draft webpage:

![winedashboard_segment2](https://user-images.githubusercontent.com/85654649/142745605-06e44068-b877-41f7-9db3-164aaa237e77.png)

This is a screen shot of our Storyboard for the Dashboard, but it's also included within our Google Slides presentation:

<img width="1064" alt="storyboard" src="https://user-images.githubusercontent.com/85654649/142746438-a19a25f1-e536-4f3c-b431-4e87136973e1.png">
