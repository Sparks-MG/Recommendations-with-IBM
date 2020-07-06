# Recommendations-with-IBM
A recommendation engine for data from the IBM Watson Studio platform


## Project Overview
This project is part of **Udacity's** Nanodegree in Data Science and has been implemented via Python. The project contains a recommender engine for articles on the IBM Watson Studio platform, test files and the employed dataset. The recommender engine recommends articles to other users based on a popularity which is simply constructed from article interaction with other useres. Different approaches are employed and analyzed.

### The Dataset
The dataset is comprised out two csv files which were scrapped from the IBM Watson Studio platform. The file **user-item-interactions.csv** contains much like the name hints (short) information on an interaction that has happend between a user and an article. This contains the article id, its title as well as an anonymized email-adress of the user. The file articles_community.csv contains more detailed information on the article like its content, description, name and its id.


### Python Libraries required

* Data Wrangling and Processing: **NumPy, pandas**
* Data Visualisation: **matplotlib**

### Included Files

* "data" folder: articles_community.csv
* "data" folder: user-item-interactions.csv
* Recommendations_with_IBM.ipynb: The actual code in a jupyter notebook.
* Recommendations_with_IBM.html: The actual code in an HTML file.
* Recommendations_with_IBM.pdf: The actual code in a pdf file.
* README.md: The readme containing this very line ;)
* project_tests.py: A test file which loads the test data and validates the results of Recommendations_with_IBM.ipynb.
* top_10.p: test data loaded by project_tests.py.
* top_20.p: test data loaded by project_tests.py.
* top_5.p: test data loaded by project_tests.py.

### Structure of the Code - Recommendations_with_IBM.ipynb
<pre>
* Exploratory Data Analysis
* Rank Based Recommendations
* User-User Based Collaborative Filtering
* Matrix Factorization
</pre>

### Eample Screenshots of a potential dashboard based on the recommendation engine
![HOME](example_images/screen-shot-2018-09-17-at-3.40.30-pm.png)
_A glimpse of a potential dashboard based on this recommendation engine_
### Project Conclussion

The training data indicates that atleast 300 latent features are necessary to achieve a high accuracy. More latent features only increase the accuracy marginally. The test data declines with rising number of latent features to a relativly high baseline value. However, only 20 users appear in both training and test data. Thus, the data situation is insufficient for a recommender situation based on collaborative filtering methods like SVD. It is advisable to employ a larger data set with more mutual users.

**In conclussion**, for the established users either a rank-based approach should be employed or a combination of rank-based recommendations and collaborative filtering. Since the latter does not work for new users, here rank-based recommendations should be employed. 

**Further steps** should include testing the effect of <u>content based recommendations</u> (extra section). This might be done via an NLP modell. Wrapping the different parts of the recommender engine in classes would enhance the structure of the code that can be easily used with a web application. Finally, experiments on different user groups should be performed  with the old and the new recommender systems in comparison <u>(A/B-testing)</u> in order to validate the recommender engine.

### Aknowledgement
* IBM for providing the data set employed in this project.
* A multitude of Stackoverflow users whose questions and answers I found, when looking for a specific coding problem.