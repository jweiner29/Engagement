DS501-E23-E01 
Jennifer Weiner
Homework 6 – Case Study 3

**Data Collected:** 
For this assignment I used a dataset from the organization where I work. I work for a national non-profit organization called The Phoenix, which provides free sober activities for any in recovery from substance use disorder and for those who support them. One of our KPIs at The Phoenix is the number of engaged members. A member is considered to be engaged if they attend their third event within 90 days of their first event. Since this is an important KPI for us, I wanted to use this assignment to see if I could learn anything about what types of things may have an impact on whether someone becomes an engaged member. 
The dataset I looked at included information about members who attended their first event in the month of January in 2023. The features include the following information about the member’s first event: 
 - Attendance Method: was the event attended in person or through live stream
 - Channel: was the event led by a staff member or a volunteer
 - Days: Number of days between enrolling and attending the first event
 - Category: what type of event was the first event
 - New via App: did the member join on our mobile app before attending their first event

My goal with this project was to see if any of the above factors influenced a member’s chance of becoming engaged and to see if we can predict whether someone will become engaged given certain values on the above features. 

**Algorithm: **

Given I wanted to estimate the probability of an event happening (a member becoming engaged) based on a given dataset of independent variables, I chose to model this dataset with a regression algorithm. A logistic regression is used when the dependent variable (a member becoming engaged) is categorical. In this case, I decided to start by fitting my dataset to a logistic regression model. \
After uploading my dataset, I did an initial summary of the logistic regression model on the data as a whole. I wanted to get an understanding of whether the independent variables I had identified were statistically significant. From running the model, I learned that all of the variables are statistically significant, but that attendance method and if the event was a social event had the most significance. Specifically, if an event was held through live stream, it was much more likely that a member would become engaged and if the event was a social event, it was much more likely that the member would not become engaged.  
From here, I wanted to test the model to see if it was a good model for this dataset. I split the dataset into train and test sets, giving the train set 80% of the rows and the test set 20% of the rows.
I fit the logistic regression model to the training set and verified that the summary of the probabilities was still in line with what I saw initially. Then I created a predict variable on the test dataset built from the logistic regression model. To see how accurate my model was, I built a confusion matrix. 293 of 364 rows were correctly identified in my model, giving the model an accuracy rate of .805. This is a good enough accuracy to assume the model can correctly predict the outcome we’re looking at.

**Building the app: **

Once I was confident that the model was capable of accurately predicting engagement based on a member’s first event information, I worked on creating an app so that someone else can easily access the data. My goal was that someone using the app could use the different independent variables to predict whether someone may become engaged, but that eventually we would learn the combination of independent variables that has the highest probability of member engagement. If we can understand that we can then tailor our programming and events so that more people experience a first event in the way that is most likely to create engagement. 
