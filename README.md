# Industrial-Copper-Modeling
## Problem Statement:
- The copper industry deals with less complex data related to sales and pricing. However, this data may suffer from issues such as skewness and noisy data, which can affect the accuracy of manual predictions. Dealing with these challenges manually can be time-consuming and may not result in optimal pricing decisions. A machine learning regression model can address these issues by utilizing advanced techniques such as data normalization, feature scaling, and outlier detection, and leveraging algorithms that are robust to skewed and noisy data. Another area where the copper industry faces challenges is in capturing the leads. A lead classification model is a system for evaluating and classifying leads based on how likely they are to become a customer . You can use the STATUS variable with WON being considered as Success and LOST being considered as Failure and remove data points other than WON, LOST STATUS values.
- The solution must include the following steps:
Exploring skewness and outliers in the dataset.
Transform the data into a suitable format and perform any necessary cleaning and pre-processing steps.
ML Regression model which predicts continuous variable ‘Selling_Price’.
ML Classification model which predicts Status: WON or LOST.
Creating a streamlit page where you can insert each column value and you will get the Selling_Price predicted value or Status(Won/Lost)
_______________________________________________________________________________________________
# Demo video(linkedIn):

__________________________________________________________________________________________

# Workflow
- Importing basic liabries and import others if need at instance
- loading dataset from excel to dataframe using pandas
- Some rubbish values are present in ‘Material_Ref’ which starts with ‘00000’ value which are converted into NaN
- found 'e' in quality tons so replacing it with NaN
- filling NaN values using fillna, divinding catogorigal(mode) and continuous(mean) valued columns
- Changing dtypes in df(if any found) date,float to int etc
- finding outliers and skewness using box plot and other
- finding with IQR
- using winsorize method to reduce outliers
- doing Label encoding
- making new feature delivery period by subtraction order date and delivery date
- Checking accuracy with ML MODEls
- Checking for best accuracy models for selling price prediction.
- checking correlation using heatmap
- using train_test_split to split dataset
- using standard scaler to normalize and saving it in pickle file
- using models like 'LinearRegression','ElasticNet','LassoLars','KNeighborsRegressor','DecisionTreeRegressor','ExtraTreesRegressor'
- to check which gives best accuracy like r2 score
- fixing best model and saving it in pickle file
- as per problem statement filtering data points other than WON & LOST STATUS values, since STATUS variable with WON being considered as Success and LOST being considered as Failure.
- understanding correlation with feautures and target
- train and split
- checking whether it is imbalanced
- if yes should go for over sampling or under sampling
- here used Oversampling with smote(Synthetic Minority Over-sampling TEchnique)
- next scaling and saving it in pickle file
- here classification models like 'LogisticRegression','KNeighborsClassifier','AdaBoostClassifier','Decision Tree','GaussianNB','RandomForestClassifier' were used
- after checking for best accuracy score choosing best model and saving it in pickle file
- also checking with confusion matrix, f1 score, auc_roc score, accuracy score
- Now with streamlite making 3 tabs
- one for price prediction and another for status predicton 
- with some text box and drop down boxes and submit button will show the predicted value
- in backgroung values got are transformed to scaler using saved scaler pickle file
- and predicted with saved pickle model file
- tab3 is just a small basic manual to use the web app.
![Capture1](https://github.com/kalinharikumar/Industrial-Copper-Modeling/assets/127252539/4a546c3c-32e7-4f91-9ebc-a8756d06d56f)
![Capture2](https://github.com/kalinharikumar/Industrial-Copper-Modeling/assets/127252539/784c6237-92c8-40ce-a3da-022d9d9534b9)
![Capture](https://github.com/kalinharikumar/Industrial-Copper-Modeling/assets/127252539/3f8c4f4c-9339-499b-8081-b0e62b6ba9fd)
![Capture4](https://github.com/kalinharikumar/Industrial-Copper-Modeling/assets/127252539/b9faad97-4b6a-4b8a-bda2-d03206a34552)
![Capture5](https://github.com/kalinharikumar/Industrial-Copper-Modeling/assets/127252539/323735f5-7eef-4974-a0e5-af0b83551a3e)




