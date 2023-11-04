# Heart Failure
project

## 1. Overview
This project is an individual assignment for the "Data Mining" class. This project analyzes one of the most popular data sets in Kaggle, 'Heart failure', by performing various data mining techniques covered in the class. The idea of this project is to apply various data mining techniques to the data to understand how each column is affecting the target variable (in this case, the target variable is the presence of heart disease).  

## 2. Project
There are two pieces of code in the project folder. One is the work I did for midterm presentation, and the other is the work I did for final presentation. I'll introduce the project in two tasks.
- first.ipynb
  - In this task, we first learn about the dataset. What variables are present, and since the data set is about medicine, we'll briefly identify what each variable is called and what it means in its field. Here are the names of the variables as they appear in the dataset.  
    - target variable : HeartDisease  
    - independent variables : Age, RestingBP, Cholesterol, FastingBS, MaxHR, ExerciseAngina, ECG, Oldpeak, ST_Slope, ChestPainType  
  - We then look at the distribution and correlation of each column. This is a simple way to see how each column relates to the target variable and how the columns relate to each other.  
  - coverage homogeneity : These are a measure of the quality of a rule, and the weighted accuracy of the two is a measure of the quality of a rule, so a rule with a high weighted accuracy is a good rule. We looked at what category or range each variable should fall into to have a high weighted accuracy.
  - Based on our work on the interim announcement, we were able to anticipate what the analysis would look like going forward, and our final announcement work confirmed that the analysis was the same.
 
- final.ipynb
  - CRI(concise rule induction) & stableDT :
    - The above method is a demo version provided by a research assistant on the project, so I haven't published the code (I don't have permission to do so, so I'm attaching a link to a related paper on CRI instead).  
    - https://www.sciencedirect.com/science/article/pii/S0957417423018675?casa_token=X5XxmGpulg4AAAAA:m3ssyLSEaZoKWpL-eC7T53cd7mYvMhJ-3KovLsgpgGhNZR12IZkC9Z8bSUAdGpRb7UAxqEZTVzA
    - There are two ways to derive rules from each model, and we compared them based on coverage and homogeneity to analyze which model is better.
    - I also performed a chi-square test to see if the rules had a dependent or independent relationship.
  - I've also tried tree-based techniques : Random Forest, Gradient Boost
    - I used gridserch to find the optimal parameters for each classifier. I plotted the confusion matrix of each model and compared the results.
  - I performed KNN with the features with high importance via feature importance in random forest.
  - I found the posterior probabilities through random forest, replaced the values with the target variables of the dataset, performed a regression tree, and applied the regression with the data of each leaf node classified by the model.
 
- conclusion of project
  - The rules determined by the CRI were dominated by variables with high importance based on the feature importance of the random forest.
  - We could tell from the EDA that people with that condition have heart disease, and when we ran logistic-reg with RI's rules or the leaf nodes of the regression tree, we could see that the results were similar to the EDA results.
 

## 3. Conclusion
This project allowed me to apply a variety of data mining techniques to analyze and interpret data. I was able to learn more about each technique and get experience in analyzing based on rules for a given data set.  
The code is copyrighted by me. This code was created with Jupyter Notebook.  
***  
Utilize the following data sets "heart failure.csv".
There are two pieces of code in the project folder. One is the work I did for midterm presentation, and the other is the work I did for final presentation.  

If you have any questions, you can email here.  
dsekdls725@seoultech.ac.kr  

