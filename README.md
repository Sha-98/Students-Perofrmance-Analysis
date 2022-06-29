# Students-Perofrmance-Analysis


## Context

There is huge population of a country or a state going to school. And there are numerus factors affecting the performance of students in the examination. 
An educational institution need to monitor the students performance in the examination and various factors influencing the results of students. The main motive of this analysis is to encounter the features supports the good results and affecting them and based on the results take actions to have better results in future.

## Content

The data set consists of the following features influencing the pass/fail examination result of the student.

* Gender *:  Gender of the student
*Race/Ethnicity*: Race or Ethnicity of the student’s family
###Parental level of Education: Education level of parents
###Lunch: Type of lunch consumed by the student out of two categories namely “Standard” and “Free/Reduced”.
###Test Preparation Course: Pre-test course offered by the institution for test preparation taken and completed or not.
###Math Score:  Marks scored by the student in Mathematics out of 100.
###Reading Score: Marks scored by the student in Reading out of 100.
###Writing Score: Marks scored by the student in Writing out of 100.

The dataset has total of 1000 rows and 8 features. Out of these 8 features we have three numerical features and 5 categorical features. 

## Exploratory Data Analysis
Talking about any null or invalid values in our dataset, we have no null or invalid values. The data is cleaned in this manner.
But the draw useful insights and create the data set model ready we need to add some more features to it which we can create using the current features by applying some mathematical conditions on them.

•	Inferential Statistics

 

•	Correlation between numerical features

 

 

After visualizing the data as heatmap we can see that the marks of a student in the three subjects are kind of related stating that if a student is performing well in any one subject there are high chances that he/she will perform well in other two also. 
Though in general cases we replace the features have high correlation coefficient but here we cannot remove the marks of any subject. This correlation was a good insight and will be playing an important role in the prediction too.

•	Score Comparison on Gender

 

From the above pivot table, we can say that there is not much of a gender biased results in any subject. Both the boys and the girls are scoring almost similar except in maths where the minimum score of girls is 0 but for boys its 27.
•	Effect of Lunch on Scores 

 

From the pivot table comparing the scores and lunch of the students we can say that students taking standard lunch are scoring more that those taking free/reduced lunch. Increasing the quality of lunch can improve the result of the students in the examination.

•	Effect of Test Preparation Course on Results

 

From the pivot table comparing the influence of completing the pre-test preparation course or no says that if the student has taken and completed the course he/she is more likely to score more than those students who have not taken the course. Institute must motivate students to take this course in order to improve the results.

•	Features added during analysis
To make the data Model ready and to get information about the results and pass/fail of a student. Following are the features added to our dataset.

o	Total Score: Total score of a student in all the subjects
o	pass_math: 1 if student has passed the maths exam and 0 if he/she has failed in it.
o	pass_reading: 1 if student has passed the reading exam and 0 if he/she has failed in it.
o	pass_writing: 1 if student has passed the writing exam and 0 if he/she has failed in it.
o	Pass/Fail: 1 if student has passed overall and 0 if he/she has failed.
o	Percentage: Percentage of marks scored by the student in all three exams altogether.
o	Status: 1 if student has passed in all three subjects separately and 0 if he/she has failed in any one subject.
o	Grades: Grades based on the percentage scored by the student










Some Important Visualizations 

•	Pair Plot

 

•	Distribution of total scores of students

 


•	Pass/Fail Ratio in Class

 


Encoding Categorical Data 
For encoding the categorical or string data in our data set to make it compatible for training our model I used the “LabelEncoder()” function from sci-kit learn. 
The “LabelEncoder()” function labels the categorical data in the feature/column using numbers. If we have two unique values in a categorical feature, it will be encoded through binary encoding using 0 and 1. Otherwise, the values will be encoded using whole numbers in the increasing order of their sequence. In short, it encodes the categorical features with a value between 0 and n-1 for n being number of distinct labels.

Model Building and Training
Here we have a classification problem as we are predicting the examination results of the student as Pass or Fails. So, for this problem statement I trained 3 ML models and tested them for predicting the results using test dataset. These 3 ML models are 
1.	Logistic Regression
2.	Random Forest Classifier
3.	Decision Tree Classifier
For all these ML model we have printed the Confusion matrix and the classification report. Based on these 2 we have found the Random Forest Classifier model to be the best fit for the data set by AUC = 1.00 and Confusion matric as below.

1.	Logistic Regression

           

       

2.	Random Forest Classifier

 

 

3.	Decision Tree Classifier

 

 


Conclusion
From the analysis we can draw some conclusions which can be stated as below

1. The number of boys and girls in a class are slightly different, number of girls are around 8% more than the number of boys in the class.
2. Around 97% of the class has passed the exam.
3. Students performance is linearly dependent on the type of lunch they take.
4. The mean score of the class in all three subjects are around 65 - 70. 
5. We can observe some outliers in the class from the distribution of scores, they might be students with bad academic background.
6. Around 1.3% of boys population has scored more than 90% in all subjects.
7. Around 3.5% of girls population has scored more than 90% in all three subjects.
