# Disease-Prediction-Using-ML

The algorithms that are used are 
Linear Regression
K Nearest Neighbours(KNN)
Decision Tree Classifier
Support Vector Machines(SVM)

Description of the Dataset! 
  This Datasets contains 133 different columns which consists of symptoms and diseases.
  Here we have two datasets for our project (training and testing datasets).
  And in the Dataset are having 132 symptoms and 41 diseases where we will be predicting diseases with respective to symptoms.
  In the columns section we are having prognosis and 132 different columns specified for symptoms, and 41 different diseases specified w.r.t. symptoms.
  Symptoms are by 0’s and 1’s in rows
  1 – represents having a symptom 
  0 – represents of not having the symptom.
  We use the training dataset to train the model so that we can predict diseases.
  We used symptoms as dependent variable and diseases/prognosis as independent variable in our datasets.
	Dependent variable    - The data which are used in predicting output.
	Independent variable - The data/the result set that will be predicted using dependent variable/the input of the user.

Flow of the Project and results!

- We first import the required libraries  to our working environment so that we can move on with the project w.r.t. Data Manipulation, Graphical Representation etc…(pandas, matplotlib, numpy & sklearn)
- Here we are having 2 datasets from Kaggle website for disease prediction – training dataset and testing dataset. We will be reading both of them from inbuilt functions available in pandas library.
- Using isnull() method we will be checking whether there are any null values present in our data set. And if the null values are present in prognosis column we will be removing the whole row as the row is of no use when the disease is not mentioned, we will be replacing the null values present in the other columns i.e. symptoms columns with 0 in other cases i.e. we will be mentioning that the symptom is not a part of the particular disease.
- Once after cleaning the dataset we will be dividing the dataset into 4 parts 
- Dependent variables from Training dataset – Type: 2D array (Columns of symptoms)
- Independent variables from Training dataset – Type: 2D array (Column of prognosis)
- Dependent variables from Testing dataset – Type: 2D array (Columns of symptoms)
- Independent variables from Testing dataset – Type: 2D array (Column of prognosis)
- We will be finding that the independent variable column has the data type as string, so we need to convert it into numbers I.e. we will be labelling the diseases using       preprocessing.LabelEncoder() present in sklearn library.
- As we have encoded the data, we have created a dictionary with key as the decoded index number/ value & the value part as the name of the disease. Example: { 0: ‘Fungal Infection’, 1: ‘Allergy’, ….. }.
- Now we will be training our model with 4 different machine learning algorithms that we have learnt (Linear Regression, KNN, Decision Tree Classifier & SVM) and find the accuracy rate of testing/predicting.
- And here we have found that our data model has an 100% accuracy rate using KNN and SVM, 97% accuracy rate using Decision Tree Classifier and 54% accuracy rate using Linear Regression. So we have decided to predict the Disease using KNN and SVM algorithms.
 - To make our project a multi-purpose analyser we have added a user friendly interface so that the user can know the symptoms that a person can have if he/she is having a particular disease.  Similarly, we have added another user friendly interface by which the user can enter the symptom he/she is having and can have the list of diseases that may affect so that the user can have a future prevention of curing the disease as soon as possible.
- Here we have added a graphical analyser by which we can know what are the major and minor symptoms in having a particular disease.

- And in end, using Machine Learning Techniques and basic python we have created a user friendly interface to predict the disease we are having and here the predicted output will be in an encoded format i.e. it will be a number so as to decode it using the dictionary that we have created earlier we will be displaying the output efficiently.

    - As we are having a large size of input range, so as to make it user friendly, we have taken help of the Dictionary datatype by initializing all the value pairs as 0 i.e. assuming that the user is having no symptoms and then using basics of python knowledge we would be asking the user to enter the partial part of the symptom that a user is having(Example: skin which further relates Skin rashes, nodal skin eruptions etc..) and can get a list of related symptoms so that the user can enter the actual symptom he/she having. And this process will be continuing until the user wants to stop entering the symptoms having.
    - We have added a case where the user enters a random data which is irrelevant to any disease, in this case so as to over come the problem, we will be using KNN and SVM algorithm and analysing whether the output/the prediction is correct or wrong i.e. we will be checking accuracy indirectly, if the outputs are same we can conclude that the data entered is relevant to a particular disease and we would be predicting the disease,  and if we get different outputs we can have a conclusion that the data is irrelevant and so as to make the user satisfy, to display some output, our model displays different diseases relevant to the given input/symptoms by the user using all four algorithms.


