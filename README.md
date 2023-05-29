# Prediction(binary classification)
A model for predicting the performance of a client's target action on the “SberAvtopodpiska”. 
# Basic Steps in EDA: 
 - Duplicate check
 - Omission or non-informative values check
 - Conversion of values to the desired data type
 - Checking for abnormal values and correcting them
 - Data visualization using graphs
# Basic actions
After that, a pipeline was built that applied StandartScaler to digital features and OneHotEncoder to categorical ones, but before that the missing values had been replaced with SimpleImputer. Since binary classification models are applicable to our task, logistic regression was used. After that, ROC-AUC =0.65 metric was calculated for the model.
To get a prediction of the client's target action, it is necessary to develop a service.
I used Postman for these purposes.

In the command line, we will start our server with the command: 
```shell
uvicorn main:app --reload
```
After that, I send a request to Postman, for this you will need a json file, after that we get a prediction.


# Install dependencies
Requires Python 3.7+.
```shell
pip install -r requirements.txt
```
