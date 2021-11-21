# Final Project: Predicting Wine Quality

![wine_image2](https://user-images.githubusercontent.com/85654649/142743285-67f1e617-0ee4-4fcc-b48d-bbdb156a2a68.jpeg)


## Outline of Project

### Team Members
- Danielle Myrick
- Delana Vath
- Jeff Purvis

### Communication Protocols for Project
We established that our group will communicate via class times, Slack, text, and ad hoc phone and video calls.

### Overview of Project
JDD Vineyards, a new business venture, has hired Myrick, Purvis, & Vath Consulting for their "Predicting Wine Quality" project. JDD Vineyards wants the consulting team to determine if their vineyard would produce quality wines, based upon characteristics their wines possess. The consulting team will analyze a dataset with quality scores and use Machine Learning to predict the quality scores JDD Vineyards would receive.

#### Question the data will potentially answer using Machine Learning Technology
Will the wines produced at JDD Vineyards generate high quality scores and be successful?

### Data Source
The data was sourced from Kaggle. The team has included a screen shot of the sample dataset as well as the specific links/files where the data can be obtained.

![data sample screen shot](https://user-images.githubusercontent.com/85654649/142744105-690acf22-5e34-47c4-b336-f64fab2015eb.png)

Raj Parmar. July 2018. Wine Quality, Version 1. [Data file]. Retrieved November 3, 2021 from https://www.kaggle.com/rajyellow46/wine-quality.
Piyush Agnihotri. September 2020. White Wine Quality, Version 1. [Data file]. Retrieved November 3, 2021 from https://www.kaggle.com/piyushagni5/white-wine-quality.
UCI Machine Learning. November 2017. Red Wine Quality, Version 2. [Data file]. Retrieved
November 3, 2021 from https://www.kaggle.com/uciml/red-wine-quality-cortez-et-al-2009.

### Google Slides Presentation
This is the link to the current verision of the team's Google Slides presentation:
https://docs.google.com/presentation/d/1_syazsfrAmDTk7VxIcM2oDEMwXvgvpArfBdHkG1Xalw/edit?usp=sharing

### Project Flow Chart
This is a draft of our project's initial flow chart, including the mock up of our Machine Learning Model.

![flowchart11-5-21](https://user-images.githubusercontent.com/85654649/140584371-bb98268b-24d8-4aed-962c-efea8a1152ae.png)

### Data Exploration and Analysis
As mentioned above, our data was initially obtained from the Kaggle website. The initial dataset included over 5,000 different wines that had been tested for their various chemical components (alcohol content, acidity levels, etc.) and a quality score was generated. We took a subset of that dataset to make it more manageable and took two additional files to function as our wine sets to attempt to calculate quality scores, based on the same input values. The team used Pandas and SQL to clean the data and perform the exploratory analysis.

Within our Machine Learning code, the team utilized the RandomForestClassifier code, as this produced the most desirable results with calculating outcomes. The team used trained model on new datasets to calculate predicted quality scores, and created a wine_id for each of the tested wines in order to identify each unique entry for analysis.

#### Database
PostgreSQL is the database the team used, and the database will be connected via code contained within the Maching Learning ipynb file. The query schema is included with the Github repository. The screen show below shows the three tables created within the database:

![db_segment2](https://user-images.githubusercontent.com/85654649/142744563-05fc1a94-1cf3-49cb-9838-cc4dfa6a9b6e.png)

This is the ERD for the Database:
![Provisional_DB](https://user-images.githubusercontent.com/85654649/140584483-6d9e690a-5ec0-42c1-a615-2959a8b9c30f.png)

#### Machine Learning
SciKitLearn is the ML library used for training and testing our source data and to create the RandomForestClassifier model. The Machine Learning code is included within the Github repository. Multiple potential models were attempted in order to identify the one that provided the most accurate results and could produce the results in a way that fit with the plan for visualization and the ultimate goal of being able to predict wine quality, based on certain characteristics. Ultimately, RandomForestClassifier produced the most desirable results. A screen show of the model creation is included below:

<img width="551" alt="create_randomforest" src="https://user-images.githubusercontent.com/85654649/142745255-b85ada29-ee1c-498d-8fb9-cb6cee11e032.png">

#### Dashboard
For our dashboard, we built a webpage using HTML and JavaScript, and we plan to embed some visualization from Tableau, in addition to our interactive element. We're looking at a few options for the interactive element, but we believe the our final interactive element will allow the user to select a wine_ID, and the page will display that specific wine_ID's quality score and chemical components.  

This is a screen shot of our draft webpage:

![winedashboard_segment2](https://user-images.githubusercontent.com/85654649/142745605-06e44068-b877-41f7-9db3-164aaa237e77.png)

This is a screen shot of our Storyboard for the Dashboard, but it's also included within our Google Slides presentation:




# Outline of Final Dashboard
We plan to build our dashboard within Tableau and anticipate it will include the following elements:

- Bar chart to display the top quality score wines.
- Column chart to compare wine quality scores.
- Pie chart to display the percentages of the categories, such as alcohol content, residual sugar, etc. of the wines with the highest quality scores and how they are distributed.
- The average quality score for our wine.

This is our initial outline of our dashboard and will progressively elaborate as we analyze our data and outcomes of our analysis. 

