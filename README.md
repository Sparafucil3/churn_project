# churn_project
<h1>Udacity project.</h1>

To run this project you will need Pything 3.x. You will also need to import the following libraries:
* seaborn
* scikitlearn
* numpy
* pandas
* numpy
* matplotlib

All data used for this is located in the /data directory within this repository. The original data is 
from Kaggle and a link to the data is provided in the notebook. 

<h3>Files</h3>
There is only one file in the project labeled churn_project.ipynb. This file contains all of our Python code, explanations of what considerations and decisions we are making during out work, as well as links to external sources of information and explanations used in the course of this project.

<h3>Summary</h3>

* Based on our work here, we have definitively concluded it is possible to predict if a customer will "churn" with varying degrees of accuracy depending on the machine learning model chosen. 

* From our initial pair-wise comparison, the columns 'SeniorCitizen', 'Partner', 'Dependents', 'tenure', 'Contract', 'PaperlessBilling', 'MonthlyCharges', 'TotalCharges', 'InternetService_Fiber optic', 'InternetService_No', 'OnlineSecurity_No internet service', 'OnlineSecurity_Yes', 'OnlineBackup_No internet service', 'DeviceProtection_No internet service', 'TechSupport_No internet service', 'TechSupport_Yes', 'StreamingTV_No internet service', 'StreamingMovies_No internet service', 'PaymentMethod_Credit card (automatic)', 'PaymentMethod_Electronic check' were determined to be the most meaningful columns in the data. The columns 'tenure' (0.35) and 'Contract' (0.39) were found to be the strongest predictors. 

* Based on the models we implemented here, Logistic Regression provided us with a model that was easy to implement, easy to explain, and produced the best overall results. However, parameters around the original business question could push us towards another model. For instance, if there was little tollerance for losing customers, models with a higher recall rate around churn=true would be favored and Fasle positives might be tolerated more in order to retain valuable customers. Conversely, if customer retention was more expensive than losing customers, a model with a lower precision but higher recall might be favorted with False Negatives being tolerated more. In the end, it comes down to cost True postives + False positives are your cost, either in effort expended or rewards offered to retain those customers. The False negative rate is your risk or implied costs. Ultimately, managements comfort with these tradeoffs will drive model selection. 

<h3>Acknowledgements</h3>
Throughout this project I used articles and resources from several blog posts all available on-line. Those articles which provided the most help are specifically highlighted below. These articles are called out in the churn file where appropriate as well as reproduced here. This is not an exhastive list and there are links to additional information provided for in the churn_project notebook. 

<h4>Data</h4>

The original dataset was taken from <a href="https://www.kaggle.com/radmirzosimov/telecom-users-dataset">Telecom users dataset</a> available on Kaggle. 

<h4>Chosing a model</h4>

* <a href='https://towardsdatascience.com/all-machine-learning-models-explained-in-6-minutes-9fe30ff6776a'>All Machine Learning Models Explained in 6 Minutes</a>: This article served as a primer for determining which models to chose. This blog is available on towards data science.

* <a href='https://towardsdatascience.com/which-machine-learning-model-to-use-db5fdf37f3dd'>Which machine learning model to use?</a>: Another nice article on chosing models to suit the purpose.

* <a href='https://machinelearningmastery.com/types-of-classification-in-machine-learning/'>4 Types of Classification Tasks in Machine Learning</a>: In addition to describing Classification, this article also describes which models are best fit for the differing Classification needs.

* <a href='https://www.datacamp.com/community/tutorials/svm-classification-scikit-learn-python'>Support Vector Machines with Scikit-learn</a> I used this article as a reference for the creation the SVM model. 

<h4>Understanding Model Performance</h4>

* <a href='https://towardsdatascience.com/understanding-the-confusion-matrix-and-how-to-implement-it-in-python-319202e0fe4d'>Understanding the Confusion Matrix and How to Implement it in Python</a>: This article serves as a good primer on how to read and draw conclusions from a Confusion Matrix. In addition, I use an image taken from that article to help readers understand what they are seeing. 

* <a href='https://medium.com/@kohlishivam5522/understanding-a-classification-report-for-your-machine-learning-model-88815e2ce397'>Understanding a Classification Report For Your Machine Learning Model</a> This article serves as a good primer on how to read and draw conclusions from a Classification report. 