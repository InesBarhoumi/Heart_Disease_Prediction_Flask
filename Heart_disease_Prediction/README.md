# Heart Disease Prediction
In this project, I will be applying Machine Learning algorith Random Forests for classifying whether a person is suffering from heart disease or not, using one of the most used dataset [Cleveland Heart Disease dataset](
https://www.kaggle.com/ronitf/heart-disease-uci).

## The Data

The dataset consists of 303 individuals data. There are 14 columns in the dataset, which are described below.
1.  Age: displays the age of the individual.
2.  Sex: displays the gender of the individual using the following format :
1 = male
0 = female
3.  Chest-pain type: displays the type of chest-pain experienced by the individual using the following format :
0 = typical angina
1 = atypical angina
2 = non — anginal pain
3 = asymptotic
4.  Resting Blood Pressure: displays the resting blood pressure value of an individual in mmHg (unit)
5.  Serum Cholestrol: displays the serum cholesterol in mg/dl (unit)
6.  Fasting Blood Sugar: compares the fasting blood sugar value of an individual with 120mg/dl.
If fasting blood sugar > 120mg/dl then : 1 (true)
else : 0 (false)
7.  Resting ECG : displays resting electrocardiographic results
0 = normal
1 = having ST-T wave abnormality
2 = left ventricular hyperthrophy
8.  Max heart rate achieved : displays the max heart rate achieved by an individual.
9.  Exercise induced angina :
1 = yes
0 = no
10. ST depression induced by exercise relative to rest: displays the value which is an integer or float.
11. Peak exercise ST segment :
1 = upsloping
2 = flat
3 = downsloping
12. Number of major vessels (0–3) colored by flourosopy : displays the value as integer or float.
13. Thal : displays the thalassemia :
0 = normal
1 = fixed defect
3 = reversible defect
14. Diagnosis of heart disease : Displays whether the individual is suffering from heart disease or not :
0 = absence
1 = present

### 1.Data Preprocessing 
The ability to learn of a model is highly affected by the quality of data. Thus, it is extremely important that we preprocess it. This step involves framing the imported dataset as a supervised learning problem: Classification. Besides it includes:
<p> - Handling missing values: Missing values are a common issue of any real world datasets, particularly for the medical field. The easiest way to handle this problem would be to drop the corresponding rows. Unfortunately, we can lose some valuable information especially if we are dealing with few samples. An alternative solution would be to impute these holes by the mean or median of the non-missing values. </p>
<p> - Removing duplicates. </p> 

### 2.Modelling 
Referring to the quote « data is the crude oil of the 21st century », then this step is where it gets refined. It addresses the problem of attaining the most informative and compact set of features, to improve the performance of machine learning models.
#### Feature engineering: 
It is the art of converting raw data into useful features. Several techniques can be performed but data scaling is mainly addressed by our application. Since the predictor variables (features) do not necessarily have the same range of values, objective functions of some machine learning algorithms, will not work properly. The model will give more weight to the variables with the highest scale. In order to avoid this issue we perform data scaling.
We can also generate new features using random projections or polynomials.
</p>

#### Feature selection: 
This step is about choosing the relevant information. It is good to add and generate features, but at some point we need to exclude irrelevant features.
Otherwise, we will be penalizing the predictive power of our model. In our application  we considered two approaches. The first one is independent to the ML model while the second depends of the model:
<p> – We select features that represent high correlations with the output variable.
<p> – We select features based on their importances to the model.
 
#### Model selection and hyper-parameter optimization: 
The extracted features were fitted to a Random forests classifier, We used grid search to optimize its hyperparameters.
#### Model Evaluation: 

The predictive performance of the different models is evaluated by comparing predictions on the test dataset with true
values using a performance metric which is the accuracy. 
We also computed the confusion matrix, also known as the error matrix, to evaluate the accuracy of the model.
<p> The confusion matrix displays the correctly predicted as well as incorrectly predicted values by a classifier.
 
![C13314_06_05](https://user-images.githubusercontent.com/58909998/71084388-6b2a4f00-2195-11ea-88bb-ebe57b4fae53.jpg)
![téléchargement](https://user-images.githubusercontent.com/58909998/70910836-d860a780-2010-11ea-9f73-0e0dda76e3c5.jpg)
  
<p> The model achieves above 80% of accuracy. </p> 

![tenor](https://user-images.githubusercontent.com/58909998/70909002-d694e500-200c-11ea-9f2c-9cc96c0c505b.gif)

## Running the web app
### Why Flask?
<p> -Easy to use.
<p>-Built in development server and debugger.
<p>-Integrated unit testing support.
<p> -RESTful request dispatching.
<p> -Extensively documented.

### Project Structure
This project has five parts :
<p> model.py — This contains code for the machine learning model to predict wether a patient has or not a heart disease using random forests.
<p> main_file.py — This contains Flask APIs that receives sales details through GUI or API calls, computes predictions wether the patient has or not a heart disease.
<p> preporcess.py — This conducts the preprocessing necessary tasks.
<p> templates — This contains the HTML template and CSS styling to allow user to login as well as to enter medical information and displays predictions of heart disease diagnosis.
<p> test.py: We  created test cases and code for: 
unit test the model code.
test the application.
<p> The notebook model.ipynb — it contains some data visualations as well as preliminary data preparation.

## Run flask web app
<p> pip install -r requirements.txt
<p> python main_file.py

Check out how the app works in this [video](https://www.youtube.com/watch?v=ym2zjJhA6og&t=10s). 


